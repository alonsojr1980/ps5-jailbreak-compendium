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

## 📋 Panel Interactivo Paso a Paso

Haz clic en cualquiera de los bloques a continuación para expandir y consultar las instrucciones detalladas, listas de verificación y comandos.

<div class="step-toolbar">
  <button class="step-toolbar-btn" onclick="toggleAllSteps(true)"><span>📂</span> Expandir Todos los Pasos</button>
  <button class="step-toolbar-btn" onclick="toggleAllSteps(false)"><span>📁</span> Contraer Todos los Pasos</button>
</div>

<!-- PASO 0 -->
<details class="step-tile" open>
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASO 0</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🔍 Comprobar el Firmware de tu Consola</span>
      <span class="step-tile-desc">Identifica la versión exacta del software del sistema (1.00 – 13.60) y comprueba la compatibilidad</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">COMPATIBILIDAD</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

### 🔍 Cómo Identificar el Firmware
1. Enciende tu PS5 y abre **Ajustes ➔ Sistema ➔ Software del sistema ➔ Información de la consola**.
2. Observa la línea **Software del sistema**:
   - Formato: `XX.XX-XX.XX.XX.XX-XX.XX` (Los 4 primeros dígitos representan tu firmware, ej. `07.61`, `04.50` o `13.60`).

### Verificación Rápida de Compatibilidad

| Firmware | ¿Se puede hacer Jailbreak? | Método de Exploit Recomendado |
| :---: | :---: | :--- |
| **1.00 – 2.50** | ✅ **SÍ** (Acceso Root a Hypervisor) | [Byepervisor / IPv6 UAF](#método-c-firmwares-iniciales-100--250-byepervisor) |
| **3.00 – 4.51** | ✅ **SÍ** (Máxima Estabilidad) | [IPv6 Socket UAF / UMTX](#método-b-firmwares-estables-300--451-y-500--550-umtx--ipv6) |
| **5.00 – 5.50** | ✅ **SÍ** (Alta Estabilidad) | [Exploit UMTX](#método-b-firmwares-estables-300--451-y-500--550-umtx--ipv6) |
| **6.00 – 6.50** | ⚠️ **SÍ** (Port en Desarrollo) | [UMTX2 / Mast1c0re](#método-b-firmwares-estables-300--451-y-500--550-umtx--ipv6) |
| **7.00 – 13.60** | ✅ **SÍ** (Era Moderna) | [Exploit Relapse (aio_multi_wait)](#método-a-firmwares-modernos-700--1360-exploit-relapse) |
| **14.00+** | ❌ **NO** (Parcheado) | Mantén la consola **estrictamente offline** y espera. **¡No actualices!** |

</details>

<!-- PASO 1 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASO 1</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🛡️ Blindaje Pre-Jailbreak y Firewall Anti-Actualizaciones</span>
      <span class="step-tile-desc">Bloquea las actualizaciones automáticas en los ajustes del sistema y en el DNS/Router</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">OBLIGATORIO</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

Una actualización accidental en segundo plano destruye permanentemente la capacidad de jailbreak. Aplica estas configuraciones inmediatamente antes de conectar la consola a cualquier red:

### 1. Lista de Verificación en la Consola
- [x] **Ajustes ➔ Sistema ➔ Software del sistema ➔ Ajustes y actualizaciones del software del sistema**:
  - Desactiva **Descargar archivos de actualización automáticamente**.
  - Desactiva **Instalar archivos de actualización automáticamente**.
- [x] **Ajustes ➔ Sistema ➔ Ahorro de energía ➔ Funciones disponibles en modo de reposo (Rest Mode)**:
  - Desactiva **Mantenerse conectado a Internet**.
- [x] **Ajustes ➔ Datos guardados y ajustes de juegos/aplicaciones ➔ Actualizaciones automáticas**:
  - Desactiva **Descarga automática**.
  - Desactiva **Instalación automática en Rest Mode**.

### 2. Lista de Dominios a Bloquear en Router / Pi-hole / AdGuard
Añade estos dominios de Sony a la lista de bloqueo de tu router o servidor DNS local:

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

</details>

<!-- ADVISORY CRÍTICO -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number warning">AVISO</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚠️ Advertencia Crítica para Lectores Extraíbles de PS5 Slim y Pro</span>
      <span class="step-tile-desc">NO actualices la consola para realizar el emparejamiento del lector de discos</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag warning">AVISO CRÍTICO</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

> [!CAUTION]
> Si tu consola es una **PS5 Slim (CFI-2000)** o **PS5 Pro (CFI-7000)** con lector de discos extraíble:
> - El lector requiere un **Handshake** criptográfico único con los servidores de Sony para vincularse con la placa base.
> - **La Trampa**: Si la consola está en un firmware vulnerable (<= 13.60), conectarse a PSN para registrar el lector **forzará una actualización irreversible al firmware más reciente**.
> - **Regla**: Si el lector no ha sido emparejado previamente, **no actualices**. Los backups digitales, homebrew, emuladores y almacenamiento SSD M.2 funcionan al 100% sin el lector físico emparejado.

</details>

<!-- PASSO 2 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASO 2</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🎮 Ejecución del Jailbreak por Rango de Firmware</span>
      <span class="step-tile-desc">Ejecuta el exploit para 7.00–13.60 (Relapse), 3.00–5.50 (UMTX) o 1.00–2.50</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">TRIGGER EXPLOIT</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

Selecciona el procedimiento correspondiente a la versión de firmware de tu consola:

### Método A: Firmwares Modernos 7.00 – 13.60 (Exploit Relapse)

Compatible con todos los modelos de PS5 (Fat, Slim y Pro) en firmwares 7.00 hasta 13.60.

#### 1. Configurar Conexión con DNS Personalizado
1. Ve a **Ajustes ➔ Red ➔ Ajustes ➔ Configurar conexión a Internet**.
2. Selecciona tu red Wi-Fi o cable LAN, presiona **Opciones (☰)** ➔ **Ajustes avanzados**.
3. Configura los siguientes parámetros:
   - **Ajustes de dirección IP**: `Automático`
   - **Nombre de host DHCP**: `No especificar`
   - **Ajustes de DNS**: `Manual`
     - **DNS Primario**: `45.56.67.85`
     - **DNS Secundario**: `0.0.0.0` (o `62.210.38.117`)
   - **Servidor proxy**: `No usar`
   - **Ajustes de MTU**: `Automático`
4. Guarda y ejecuta la prueba de conexión. *Conexión a Internet: Correcta*; *PlayStation Network: Error* (Esperado y seguro).

#### 2. Disparar el Exploit
1. Abre **Ajustes ➔ Sistema ➔ Guía del usuario, seguridad y salud ➔ Guía del usuario**.
2. El navegador interno se redirigirá al host del exploit Relapse.
3. El exploit WebKit se ejecutará automáticamente (realizando heap spray en la memoria de JavaScriptCore).
4. El exploit de kernel se disparará mediante la race condition de `aio_multi_wait`.
5. Espera al mensaje de confirmación:
   `[+] Kernel RW Obtained! elfldr listening on port 9021...`

> [!TIP]
> Si la consola se congela o se apaga abruptamente con pantalla negra, se ha producido un **Kernel Panic**. Espera 30 segundos, enciende la consola desde el botón físico de encendido, espera a que finalice la comprobación del almacenamiento e inténtalo de nuevo.

---

### Método B: Firmwares Estables 3.00 – 4.51 y 5.00 – 5.50 (UMTX / IPv6)

Rango con máxima estabilidad (tasa de éxito cercana al 100%).

1. Configura el **DNS Primario** de la PS5 a `62.210.38.117` (EchoStretch) o `165.227.83.145` (Al-Azif).
2. Abre **Ajustes ➔ Sistema ➔ Guía del usuario**.
3. Selecciona el exploit adecuado:
   - Para **3.00 – 4.51**: Selecciona **IPv6 UAF** o **UMTX**.
   - Para **5.00 – 5.50**: Selecciona **UMTX Exploit**.
4. El exploit finaliza en pocos segundos e inicia el daemon `elfldr` en el puerto 9021.

---

### Método C: Firmwares Iniciales 1.00 – 2.50 (Byepervisor)

El rango más privilegiado de todo el ecosistema, con control total del Hypervisor (Ring -1).

1. Accede a la página del exploit mediante la Guía del usuario o a través de disco Blu-ray con BD-JB.
2. Dispara el exploit de kernel y carga el payload **Byepervisor**.
3. Byepervisor asume el control del Hypervisor de la PS5, permitiendo lectura y escritura arbitraria en el hypervisor, bypass de validación de firmas de código y descifrado de memoria RAM.

</details>

<!-- PASO 3 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASO 3</span>
    <span class="step-tile-text">
      <span class="step-tile-title">📦 Inyección de Payloads (etaHEN y ps5-kstuff)</span>
      <span class="step-tile-desc">Carga el framework de homebrew mediante autoloader USB o Netcat en el puerto 9021</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">INYECCIÓN DE PAYLOADS</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

Una vez que el daemon `elfldr` esté a la escucha en el **puerto 9021**, inyecta los payloads:

### Opción 1: Carga Automática por USB (Recomendada)

1. Formatea una memoria USB en formato **exFAT** (tabla de particiones MBR).
2. Crea una carpeta llamada `payloads` en la raíz de la unidad USB:
   ```text
   Memoria USB (exFAT):
   └── payloads/
       ├── etaHEN.bin
       └── ps5-kstuff.bin
   ```
3. Conecta la memoria USB en uno de los puertos USB 3.0 traseros de tu PS5.
4. Al activar el exploit en el navegador, ¡el cargador detecta y ejecuta automáticamente los payloads de la unidad USB!

---

### Opción 2: Inyección por Red mediante Terminal (Netcat)

Si envías los payloads desde tu ordenador a través de la red local:

#### En Linux / macOS / WSL:
```bash
# Inyectar etaHEN (Framework All-In-One para Homebrew)
nc -w 3 <IP_DE_LA_PS5> 9021 < etaHEN.bin

# Inyectar ps5-kstuff (si no está incluido en etaHEN)
nc -w 3 <IP_DE_LA_PS5> 9021 < ps5-kstuff.bin
```

#### En Windows (PowerShell):
```powershell
$ps5_ip = "192.168.1.150"
$bytes = [System.IO.File]::ReadAllBytes("etaHEN.bin")
$client = New-Object System.Net.Sockets.TcpClient($ps5_ip, 9021)
$stream = $client.GetStream()
$stream.Write($bytes, 0, $bytes.Length)
$stream.Close(); $client.Close()
Write-Host "[ÉXITO] etaHEN enviado a la PS5!"
```

</details>

<!-- PASO 4 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASO 4</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🕹️ Instalación de Homebrew y Ejecución de Backups de Juegos</span>
      <span class="step-tile-desc">Configuración de etaHEN Toolbox, servidor FTP puerto 1337, Itemzflow y Apollo Save Tool</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">APPS Y HOMEBREW</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

Tras inyectar **etaHEN**:

1. **Verificar etaHEN Toolbox**:
   - Abre **Ajustes ➔ Sistema**.
   - Aparecerá la nueva entrada de menú **etaHEN Toolbox**.
2. **Acceder por Servidor FTP**:
   - etaHEN inicia automáticamente un servidor FTP en el **puerto 1337**.
   - Conéctate con FileZilla / WinSCP usando la IP de tu PS5 y el puerto `1337` (inicio de sesión anónimo).
3. **Instalar Itemzflow (Gestor de Juegos)**:
   - Instala `Itemzflow.pkg` desde el instalador de paquetes en Ajustes o inícialo directamente.
   - Realiza un dump de tus discos físicos o compras digitales hacia un disco duro externo USB o un SSD NVMe M.2 interno.
   - Inicia juegos directamente desde el almacenamiento USB sin necesidad de copiarlos al disco interno.
4. **Gestionar Partidas con Apollo Save Tool**:
   - Exporta, importa y refirma partidas guardadas entre distintas cuentas de PSN de forma totalmente offline.

</details>

<!-- PASO 5 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASO 5</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🔧 Resolución Rápida de Problemas y Recuperación de Kernel Panics</span>
      <span class="step-tile-desc">Soluciones para pantalla negra, errores de memoria WebKit, desincronización de DNS y errores CE-xxxx</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">RECUPERACIÓN</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

| Síntoma | Causa Raíz | Solución Práctica |
| :--- | :--- | :--- |
| **Pantalla negra instantánea / Apagado** | Kernel Panic durante la sincronización de la race condition | Espera 30 segundos. Pulsa el botón físico de encendido. Deja que termine la reparación de almacenamiento y reinicia el exploit. |
| **"Memoria del sistema insuficiente"** | Desbordamiento en heap grooming de WebKit | Pulsa `Aceptar`, recarga la página o borra las cookies del navegador en los ajustes. |
| **La Guía del usuario abre la web de Sony** | Desincronización de DNS o el router omite el DNS manual | Revisa los Ajustes de red; asegúrate de que el DNS Primario sea `45.56.67.85` y el Secundario sea `0.0.0.0`. |
| **Conexión rechazada en puerto 9021** | La Fase 2 falló o `elfldr` se cerró inesperadamente | Vuelve a abrir la Guía del usuario hasta que aparezca el aviso de escucha en el puerto 9021. |
| **Los juegos no inician con error CE-xxxx** | El payload `ps5-kstuff` no está cargado | Asegúrate de cargar `kstuff` o `etaHEN` antes de ejecutar juegos. |

</details>

---

<p align="center">
  <b>¿Necesitas detalles técnicos profundos, primitivas de memoria, syscalls o puertos de red?</b><br>
  👉 Consulta la guía complementaria: <b><a href="jailbreak_tech_info.md">PS5 Jailbreak: Análisis Técnico Detallado (Tech Info)</a></b>
</p>
