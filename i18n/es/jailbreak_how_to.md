# 🚀 Cómo Hacer Jailbreak en PS5: Guía Práctica Paso a Paso
### *by ALONSOJR1980*

<div align="center">

[![Firmwares Soportados](https://img.shields.io/badge/Firmwares%20Soportados-1.00%20--%2013.60-success?style=for-the-badge&logo=playstation&logoColor=white)](https://github.com/alonsojr1980/ps5-jailbreak-compendium)
[![Exploit](https://img.shields.io/badge/Exploit%20Principal-Relapse%20%7C%20UMTX-blueviolet?style=for-the-badge&logo=codeforces&logoColor=white)](jailbreak_tech_info.md)
[![Sitio Web Online](https://img.shields.io/badge/Sitio%20Web-GitHub%20Pages-00d2ff?style=for-the-badge&logo=githubpages&logoColor=white)](https://alonsojr1980.github.io/ps5-jailbreak-compendium/)
[![Payloads](https://img.shields.io/badge/Payloads-etaHEN%20%7C%20ps5--kstuff-ff69b4?style=for-the-badge&logo=coffeescript&logoColor=white)](jailbreak_tech_info.md#4-ingenier%C3%ADa-de-payloads--frameworks-del-sistema)

**Navegación / Navigation:**
[🔬 Análisis Técnico Detallado (Tech Info)](jailbreak_tech_info.md) | [🇺🇸 English Version](../en/jailbreak_how_to.md) | [🇧🇷 Versão em Português](../pt/jailbreak_how_to.md) | [🌐 Portal Principal](../../README.md)

</div>

Una guía directa, práctica y concisa para realizar el jailbreak en tu PlayStation 5 en las diferentes versiones de firmware, configurar el firewall anti-actualizaciones e inyectar los payloads esenciales.

---

## 📑 Índice de Contenidos

1. [🔍 Paso 0: Comprobar el Firmware de tu Consola](#-paso-0-comprobar-el-firmware-de-tu-consola)
2. [🛡️ Paso 1: Blindaje Pre-Jailbreak y Firewall Anti-Actualizaciones](#️-paso-1-blindaje-pre-jailbreak-y-firewall-anti-actualizaciones)
3. [⚠️ Advertencia Crítica para Lectores Extraíbles de PS5 Slim y Pro](#️-advertencia-cr%C3%ADtica-para-lectores-extra%C3%ADbles-de-ps5-slim-y-pro)
4. [🎮 Paso 2: Procedimiento de Jailbreak por Rango de Firmware](#-paso-2-procedimiento-de-jailbreak-por-rango-de-firmware)
   - [Método A: Firmwares Modernos 7.00 – 13.60 (Exploit Relapse)](#m%C3%A9todo-a-firmwares-modernos-700--1360-exploit-relapse)
   - [Método B: Firmwares Estables 3.00 – 4.51 y 5.00 – 5.50 (UMTX / IPv6)](#m%C3%A9todo-b-firmwares-estables-300--451-y-500--550-umtx--ipv6)
   - [Método C: Firmwares Iniciales 1.00 – 2.50 (Byepervisor)](#m%C3%A9todo-c-firmwares-iniciales-100--250-byepervisor)
5. [📦 Paso 3: Inyección de Payloads (etaHEN y ps5-kstuff)](#-paso-3-inyecci%C3%B3n-de-payloads-etahen-y-ps5-kstuff)
   - [Opción 1: Carga Automática por USB (Recomendada)](#opci%C3%B3n-1-carga-autom%C3%A1tica-por-usb-recomendada)
   - [Opción 2: Inyección por Red mediante Terminal (Netcat)](#opci%C3%B3n-2-inyecci%C3%B3n-por-red-mediante-terminal-netcat)
6. [🕹️ Paso 4: Instalación de Homebrew y Ejecución de Backups de Juegos](#️-paso-4-instalaci%C3%B3n-de-homebrew-y-ejecuci%C3%B3n-de-backups-de-juegos)
7. [🔧 Resolución Rápida de Problemas y Recuperación de Kernel Panics](#-resoluci%C3%B3n-r%C3%A1pida-de-problemas-y-recuperaci%C3%B3n-de-kernel-panics)

---

## 🔍 Paso 0: Comprobar el Firmware de tu Consola

Antes de comenzar cualquier procedimiento, identifica la versión exacta del software del sistema de tu PS5:

1. Enciende tu PS5 y abre **Ajustes ➔ Sistema ➔ Software del sistema ➔ Información de la consola**.
2. Observa la línea **Software del sistema**:
   - Formato: `XX.XX-XX.XX.XX.XX-XX.XX` (Los 4 primeros dígitos representan tu firmware, ej. `07.61`, `04.50` o `13.60`).

### Verificación Rápida de Compatibilidad

| Firmware | ¿Se puede hacer Jailbreak? | Método de Exploit Recomendado |
| :---: | :---: | :--- |
| **1.00 – 2.50** | ✅ **SÍ** (Acceso Root a Hypervisor) | [Byepervisor / IPv6 UAF](#m%C3%A9todo-c-firmwares-iniciales-100--250-byepervisor) |
| **3.00 – 4.51** | ✅ **SÍ** (Máxima Estabilidad) | [IPv6 Socket UAF / UMTX](#m%C3%A9todo-b-firmwares-estables-300--451-y-500--550-umtx--ipv6) |
| **5.00 – 5.50** | ✅ **SÍ** (Alta Estabilidad) | [Exploit UMTX](#m%C3%A9todo-b-firmwares-estables-300--451-y-500--550-umtx--ipv6) |
| **6.00 – 6.50** | ⚠️ **SÍ** (Port en Desarrollo) | [UMTX2 / Mast1c0re](#m%C3%A9todo-b-firmwares-estables-300--451-y-500--550-umtx--ipv6) |
| **7.00 – 13.60** | ✅ **SÍ** (Era Moderna) | [Exploit Relapse (aio_multi_wait)](#m%C3%A9todo-a-firmwares-modernos-700--1360-exploit-relapse) |
| **14.00+** | ❌ **NO** (Parcheado) | Mantén la consola **estrictamente offline** y espera. **¡No actualices!** |

---

## 🛡️ Paso 1: Blindaje Pre-Jailbreak y Firewall Anti-Actualizaciones

Una actualización accidental en segundo plano destruye permanentemente la capacidad de jailbreak. Aplica estas configuraciones inmediatamente antes de conectar la consola a cualquier red:

### 1. Lista de Ajustes en la Consola
- [x] **Ajustes ➔ Sistema ➔ Software del sistema ➔ Ajustes y actualizaciones del software del sistema**:
  - Desactiva **Descargar archivos de actualización automáticamente**.
  - Desactiva **Instalar archivos de actualización automáticamente**.
- [x] **Ajustes ➔ Sistema ➔ Ahorro de energía ➔ Funciones disponibles en modo de reposo**:
  - Desactiva **Mantenerse conectado a Internet**.
- [x] **Ajustes ➔ Datos guardados y ajustes de juegos/aplicaciones ➔ Actualizaciones automáticas**:
  - Desactiva **Descarga automática**.
  - Desactiva **Instalación automática en modo de reposo**.

### 2. Bloqueo de Dominios en Router / Pi-hole / AdGuard Home
Agrega los siguientes dominios de telemetría y actualización de Sony a la lista negra (blacklist) de tu firewall:

```text
fus01.ps5.update.playstation.net
fuk01.ps5.update.playstation.net
feu01.ps5.update.playstation.net
fjp01.ps5.update.playstation.net
fkr01.ps5.update.playstation.net
fcn01.ps5.update.playstation.net
ps5.update.playstation.net
telemetry.api.playstation.com
telemetry-ingest.api.playstation.com
```

---

## ⚠️ Advertencia Crítica para Lectores Extraíbles de PS5 Slim y Pro

> [!CAUTION]
> Si tu consola es una **PS5 Slim (CFI-2000)** o **PS5 Pro (CFI-7000)** con unidad lectora de discos extraíble:
> - El lector requiere un **Handshake** criptográfico inicial con los servidores de Sony para vincularse con la placa base.
> - **La Trampa**: Si tu consola está en un firmware vulnerable (<= 13.60), conectarte a PSN para emparejar el lector **forzará una actualización irreversible del sistema a la versión más reciente**.
> - **Regla Fundamental**: Si tu lector no fue emparejado previamente, **no actualices**. Los backups digitales, homebrew, emuladores y el almacenamiento SSD M.2 funcionan al 100% sin necesidad de registrar la unidad física de disco.

---

## 🎮 Paso 2: Procedimiento de Jailbreak por Rango de Firmware

### Método A: Firmwares Modernos 7.00 – 13.60 (Exploit Relapse)

Este método cubre todos los modelos de PS5 (Fat, Slim y Pro) que ejecutan versiones de firmware desde la 7.00 hasta la 13.60.

#### 1. Configuración de Conexión DNS Personalizada
1. Ve a **Ajustes ➔ Red ➔ Configuración ➔ Configurar conexión a Internet**.
2. Selecciona tu conexión Wi-Fi o Cable LAN, presiona el botón **Opciones (☰)** ➔ **Ajustes avanzados**.
3. Configura los siguientes parámetros:
   - **Ajustes de dirección IP**: `Automático`
   - **Nombre de host DHCP**: `No especificar`
   - **Ajustes de DNS**: `Manual`
     - **DNS primario**: `45.56.67.85`
     - **DNS secundario**: `0.0.0.0` (o `62.210.38.117`)
   - **Servidor proxy**: `No usar`
   - **Ajustes de MTU**: `Automático`
4. Guarda y ejecuta la prueba de conexión: *Conexión a Internet: Correcta*; *PlayStation Network: Con error* (Comportamiento totalmente normal y seguro).

#### 2. Ejecución del Exploit
1. Abre **Ajustes ➔ Sistema ➔ Guía del usuario, seguridad y otra información ➔ Guía del usuario**.
2. El navegador interno redirigirá automáticamente al host del Exploit Relapse.
3. El exploit de WebKit se ejecutará automáticamente (realizando un heap spray en la memoria de JavaScriptCore).
4. El exploit de kernel se activará mediante la condición de carrera en `aio_multi_wait`.
5. Espera a recibir el mensaje de confirmación:
   `[+] Kernel RW Obtained! elfldr listening on port 9021...`

> [!TIP]
> Si la consola se congela o se apaga abruptamente con la pantalla en negro, se ha producido un **Kernel Panic**. Espera 30 segundos, enciende la consola desde el botón físico frontal, deja que finalice la comprobación del almacenamiento y vuelve a intentarlo.

---

### Método B: Firmwares Estables 3.00 – 4.51 y 5.00 – 5.50 (UMTX / IPv6)

Estas versiones gozan de una estabilidad excepcional (tasa de éxito cercana al 100%).

1. Configura el **DNS primario** de tu PS5 con `62.210.38.117` (EchoStretch) o `165.227.83.145` (Al-Azif).
2. Abre **Ajustes ➔ Sistema ➔ Guía del usuario**.
3. Selecciona el exploit correspondiente a tu versión:
   - Para **3.00 – 4.51**: Selecciona **IPv6 UAF** o **UMTX**.
   - Para **5.00 – 5.50**: Selecciona **UMTX Exploit**.
4. El exploit se ejecutará en cuestión de segundos, iniciando `elfldr` en el puerto 9021.

---

### Método C: Firmwares Iniciales 1.00 – 2.50 (Byepervisor)

El rango de firmware más privilegiado, con control absoluto sobre el Hypervisor (Ring -1).

1. Accede al host del exploit a través de la Guía del usuario o mediante un disco Blu-ray con BD-JB.
2. Ejecuta el exploit de kernel y carga el payload **Byepervisor**.
3. Byepervisor neutraliza el Hypervisor de Prospero, permitiendo lectura/escritura arbitraria en memoria hipervisora, bypass total de firma de código y desencriptación de RAM en tiempo real.

---

## 📦 Paso 3: Inyección de Payloads (etaHEN y ps5-kstuff)

Una vez que `elfldr` esté escuchando activamente en el **Puerto 9021**, procede a inyectar los payloads esenciales:

### Opción 1: Carga Automática por USB (Recomendada)

1. Formatea una memoria USB en **exFAT** (esquema de particiones MBR).
2. Crea una carpeta llamada `payloads` en la raíz de la unidad USB:
   ```text
   Unidad USB (exFAT):
   └── payloads/
       ├── etaHEN.bin
       └── ps5-kstuff.bin
   ```
3. Conecta el pendrive a uno de los puertos USB 3.0 traseros de tu PS5.
4. Al ejecutar el exploit, ¡el cargador detectará y ejecutará automáticamente los payloads desde el USB sin necesidad de un ordenador!

---

### Opción 2: Inyección por Red mediante Terminal (Netcat)

Si deseas enviar los payloads directamente desde tu ordenador a través de la red local:

#### En Linux / macOS / WSL:
```bash
# Inyectar etaHEN (Activador All-In-One de Homebrew)
nc -w 3 <IP_DE_TU_PS5> 9021 < etaHEN.bin

# Inyectar ps5-kstuff (si no viene integrado en el paquete de etaHEN)
nc -w 3 <IP_DE_TU_PS5> 9021 < ps5-kstuff.bin
```

#### En Windows (PowerShell):
```powershell
$ps5_ip = "192.168.1.150"
$bytes = [System.IO.File]::ReadAllBytes("etaHEN.bin")
$client = New-Object System.Net.Sockets.TcpClient($ps5_ip, 9021)
$stream = $client.GetStream()
$stream.Write($bytes, 0, $bytes.Length)
$stream.Close(); $client.Close()
Write-Host "[SUCCESS] ¡etaHEN enviado con éxito a la PS5!"
```

---

## 🕹️ Paso 4: Instalación de Homebrew y Ejecución de Backups de Juegos

Una vez inyectado **etaHEN**:

1. **Verificar etaHEN Toolbox**:
   - Ve a **Ajustes ➔ Sistema**.
   - Verás el nuevo menú **etaHEN Toolbox**.
2. **Acceso al Servidor FTP**:
   - etaHEN levanta automáticamente un servidor FTP en el **Puerto 1337**.
   - Conéctate mediante FileZilla o WinSCP ingresando la IP de tu consola y el puerto `1337` (inicio de sesión Anónimo).
3. **Ejecutar Itemzflow (Administrador de Juegos)**:
   - Instala `Itemzflow.pkg` mediante el instalador de paquetes (Package Installer) en Ajustes o ábrelo directamente.
   - Realiza el Dump de tus discos físicos o títulos digitales a un disco duro externo USB o al SSD interno M.2 NVMe.
   - Ejecuta juegos directamente desde el almacenamiento USB sin necesidad de copiarlos al almacenamiento interno.
4. **Gestionar Partidas Guardadas con Apollo Save Tool**:
   - Exporta, importa y reasigna partidas guardadas (savegames) entre diferentes cuentas de PSN de forma 100% offline.

---

## 🔧 Resolución Rápida de Problemas y Recuperación de Kernel Panics

| Problema | Causa Raíz | Solución |
| :--- | :--- | :--- |
| **Pantalla negra instantánea / Apagado** | Kernel Panic durante la condición de carrera | Espera 30 segundos. Presiona el botón físico de encendido. Deja que termine la reparación del almacenamiento y vuelve a ejecutar el exploit. |
| **"No hay suficiente memoria libre del sistema"** | Desbordamiento en el heap grooming de WebKit | Pulsa `Aceptar`, actualiza la página o borra los datos de navegación/cookies en ajustes. |
| **La Guía del usuario carga la página oficial de Sony** | Desincronización de DNS o router ignorando DNS manual | Revisa la configuración de red; confirma que el DNS primario sea `45.56.67.85` y el secundario `0.0.0.0`. |
| **Conexión rechazada en el Puerto 9021 (Connection Refused)** | La Etapa 2 falló o `elfldr` se cerró inesperadamente | Vuelve a abrir la Guía del usuario hasta ver la notificación "Listening on 9021". |
| **Los juegos no inician y muestran error CE-xxxx** | Payload `ps5-kstuff` no cargado en memoria | Asegúrate de haber inyectado `ps5-kstuff` o `etaHEN` antes de abrir los juegos. |

---

<p align="center">
  <b>¿Necesitas detalles técnicos a bajo nivel, primitivas de memoria, llamadas al sistema (syscalls) o especificaciones de puertos?</b><br>
  👉 Consulta la guía avanzada: <b><a href="jailbreak_tech_info.md">Jailbreak de PS5: Análisis Técnico Detallado (Tech Info)</a></b>
</p>
