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

Una guía táctica, directa y gamificada para realizar el jailbreak en tu PlayStation 5 en las versiones 1.00 hasta 13.60, blindar defensas anti-actualizaciones y ejecutar payloads.

---

<!-- GAMIFIED QUEST HUD -->
<div class="ps-quest-hud" id="psQuestHud">
  <div class="ps-hud-header">
    <div class="ps-hud-title-wrap">
      <div class="ps-hud-rank-icon" id="psRankIcon">🎮</div>
      <div>
        <div class="ps-hud-title">Campaña: Protocolo Jailbreak PS5</div>
        <div class="ps-hud-subtitle">Completa las misiones para liberar el firmware y reclamar Trofeos de PlayStation</div>
      </div>
    </div>
    <div class="ps-hud-stats">
      <div class="ps-hud-stat-pill">
        <span>🏆 TROFEOS:</span>
        <span id="psTrophiesCount">0 / 5</span>
      </div>
      <div class="ps-hud-stat-pill">
        <span>⚡ XP:</span>
        <span id="psProgressPct">0%</span>
      </div>
    </div>
  </div>

  <div class="ps-progress-bar-container">
    <div class="ps-progress-bar-fill" id="psProgressFill"></div>
  </div>

  <div class="ps-hud-footer">
    <div><span>△</span> Inspeccionar misión &bull; <span>◯</span> Completar y Reclamar Trofeo &bull; <span>✕</span> Ejecutar</div>
    <div class="ps-hud-controls">
      <button class="ps-btn-hud" onclick="toggleAllSteps(true)">📂 Expandir Todo</button>
      <button class="ps-btn-hud" onclick="toggleAllSteps(false)">📁 Contraer Todo</button>
      <button class="ps-btn-hud" onclick="resetAllQuests()">🔄 Reiniciar Campaña</button>
    </div>
  </div>
</div>

<!-- MISIÓN 0 -->
<details class="step-tile" data-quest="quest-step-0" open>
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISIÓN 0</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🎯 Reconocimiento del Objetivo: Identificación de Firmware</span>
      <span class="step-tile-desc">Identifica la versión del software del sistema (1.00 – 13.60) y confirma vulnerabilidad</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">RECON</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DE LA MISIÓN:</strong> Localizar la versión exacta del software del sistema en la consola y verificar el nivel de compatibilidad del exploit.
</div>

### 🎒 Equipamiento Necesario
- Consola PS5 y Mando DualSense
- Pantalla / Televisor

### ⚡ Ejecución Táctica
1. Enciende tu consola y abre **Ajustes ➔ Sistema ➔ Software del sistema ➔ Información de la consola**.
2. Observa la línea **Software del sistema**:
   - Formato: `XX.XX-XX.XX.XX.XX-XX.XX` (Los primeros 4 dígitos indican tu firmware: ej. `07.61`, `04.50`, `13.60`).

### 📊 Matriz de Compatibilidad de Firmware

| Rango de Firmware | Estado del Exploit | Vector Táctico Recomendado |
| :---: | :---: | :--- |
| **1.00 – 2.50** | ✅ **Acceso Root Hypervisor** | [Byepervisor / IPv6 UAF](#método-c-firmwares-iniciales-100--250-byepervisor) |
| **3.00 – 4.51** | ✅ **Máxima Estabilidad** | [IPv6 Socket UAF / UMTX](#método-b-firmwares-estables-300--451-y-500--550-umtx--ipv6) |
| **5.00 – 5.50** | ✅ **Alta Estabilidad** | [Exploit UMTX](#método-b-firmwares-estables-300--451-y-500--550-umtx--ipv6) |
| **6.00 – 6.50** | ⚠️ **Port en Desarrollo** | [UMTX2 / Mast1c0re](#método-b-firmwares-estables-300--451-y-500--550-umtx--ipv6) |
| **7.00 – 13.60** | ✅ **Era Moderna** | [Exploit Relapse (aio_multi_wait)](#método-a-firmwares-modernos-700--1360-exploit-relapse) |
| **14.00+** | ❌ **Parcheado** | Mantén la consola **estrictamente offline**. **¡No actualices!** |

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🥉 Trofeo de Bronce &bull; <em>"Especialista en Reconocimiento"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-0" data-todo-text="Marcar Completada" data-done-text="Misión Completada" onclick="toggleQuest('quest-step-0', 'Especialista en Reconocimiento', 'Trofeo de Bronce', '🎯')">
    <span>◯</span> Marcar Completada
  </button>
</div>

</details>

<!-- MISIÓN 1 -->
<details class="step-tile" data-quest="quest-step-1">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISIÓN 1</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🛡️ Protocolo de Defensa: Blindaje Anti-Actualizaciones</span>
      <span class="step-tile-desc">Bloquea la telemetría de Sony y activa el firewall antes de conectar la consola</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">OBLIGATORIO</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DE LA MISIÓN:</strong> Inmunizar tu consola contra descargas silenciosas de actualizaciones en segundo plano para preservar permanentemente la capacidad de jailbreak.
</div>

### 🎒 Equipamiento Necesario
- Ajustes del Sistema de la Consola
- Router / Pi-hole / AdGuard (Capa de defensa adicional recomendada)

### ⚡ Ejecución Táctica: Blindaje en la Consola
- [x] **Ajustes ➔ Sistema ➔ Software del sistema ➔ Ajustes y actualizaciones del software del sistema**:
  - Desactiva **Descargar archivos de actualización automáticamente**.
  - Desactiva **Instalar archivos de actualización automáticamente**.
- [x] **Ajustes ➔ Sistema ➔ Ahorro de energía ➔ Funciones disponibles en modo de reposo (Rest Mode)**:
  - Desactiva **Mantenerse conectado a Internet**.
- [x] **Ajustes ➔ Datos guardados y ajustes de juegos/aplicaciones ➔ Actualizaciones automáticas**:
  - Desactiva **Descarga automática**.
  - Desactiva **Instalación automática en Rest Mode**.

### 🌐 Lista de Dominios Bloqueados para Router / Pi-hole
Añade estos dominios de Sony a la lista negra de tu red doméstica:

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

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🥉 Trofeo de Bronce &bull; <em>"Centinela de Red"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-1" data-todo-text="Marcar Completada" data-done-text="Misión Completada" onclick="toggleQuest('quest-step-1', 'Centinela de Red', 'Trofeo de Bronce', '🛡️')">
    <span>◯</span> Marcar Completada
  </button>
</div>

</details>

<!-- PELIGRO DE JEFE / TRAMPA -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number warning">PELIGRO</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚠️ Trampa del Lector Extraíble de PS5 Slim y Pro</span>
      <span class="step-tile-desc">NO te conectes a PSN para registrar el lector en firmware vulnerable</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag warning">TRAMPA MORTAL</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>⚠️ INTEL DE PELIGRO:</strong> El lector de discos extraíble requiere un <strong>Handshake</strong> criptográfico único con los servidores de Sony para vincularse a la placa base.
</div>

> [!CAUTION]
> - **La Trampa**: Si la consola está en un firmware vulnerable (<= 13.60), conectarse a PSN para registrar el lector **forzará una actualización irreversible al firmware más reciente**, eliminando por completo la posibilidad de jailbreak.
> - **Regla Operativa**: Si el lector no ha sido emparejado previamente, **no actualices**. Los backups digitales, homebrew, emuladores y almacenamiento en SSD M.2 funcionan al 100% sin el lector emparejado.

</details>

<!-- MISIÓN 2 -->
<details class="step-tile" data-quest="quest-step-2">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISIÓN 2</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚔️ Infiltración: Disparo del Exploit y Kernel RW</span>
      <span class="step-tile-desc">Dispara el spray de WebKit y la race de aio_multi_wait para abrir el Puerto 9021</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">KERNEL BREACH</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DE LA MISIÓN:</strong> Obtener lectura/escritura arbitraria en el Kernel e iniciar el listener de <code>elfldr</code> en el <strong>Puerto 9021</strong>.
</div>

### 🎒 Equipamiento Necesario
- DNS del Exploit: `45.56.67.85` (Relapse) o `62.210.38.117` (UMTX)
- Navegador de la Guía del usuario en la PS5

### ⚡ Ejecución Táctica: Selecciona el Vector de tu Firmware

#### Método A: Firmwares Modernos 7.00 – 13.60 (Exploit Relapse)
1. Ve a **Ajustes ➔ Red ➔ Ajustes ➔ Configurar conexión a Internet**.
2. Selecciona tu red, pulsa **Opciones (☰)** ➔ **Ajustes avanzados**:
   - **Ajustes de DNS**: `Manual`
   - **DNS Primario**: `45.56.67.85`
   - **DNS Secundario**: `0.0.0.0` (o `62.210.38.117`)
3. Guarda y realiza la prueba de conexión (*Internet: Correcta*; *PSN: Error* — esperado y seguro).
4. Abre **Ajustes ➔ Sistema ➔ Guía del usuario, seguridad y salud ➔ Guía del usuario**.
5. El host Relapse ejecuta el heap spray en WebKit y a continuación la race condition en `aio_multi_wait`.
6. Espera la confirmación en pantalla:
   `[+] Kernel RW Obtained! elfldr listening on port 9021...`

> [!TIP]
> Si la consola se apaga repentinamente, ha ocurrido un **Kernel Panic**. Espera 30 segundos, enciende con el botón físico de encendido, espera a que termine la comprobación del almacenamiento y repite el procedimiento.

---

#### Método B: Firmwares Estables 3.00 – 4.51 y 5.00 – 5.50 (UMTX / IPv6)
1. Configura el **DNS Primario** a `62.210.38.117` o `165.227.83.145`.
2. Abre **Ajustes ➔ Sistema ➔ Guía del usuario**.
3. Selecciona **IPv6 UAF** (para 3.00–4.51) o **UMTX Exploit** (para 5.00–5.50).
4. El exploit se completa en segundos e inicializa `elfldr` en el Puerto 9021.

---

#### Método C: Firmwares Iniciales 1.00 – 2.50 (Byepervisor)
1. Carga el exploit mediante la Guía del usuario o a través de disco Blu-ray con BD-JB.
2. Inyecta **Byepervisor** para asumir el control absoluto del Hypervisor (Ring -1).

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🥈 Trofeo de Plata &bull; <em>"Perímetro Vulnerado"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-2" data-todo-text="Marcar Completada" data-done-text="Misión Completada" onclick="toggleQuest('quest-step-2', 'Perímetro Vulnerado', 'Trofeo de Plata', '⚔️')">
    <span>◯</span> Marcar Completada
  </button>
</div>

</details>

<!-- MISIÓN 3 -->
<details class="step-tile" data-quest="quest-step-3">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISIÓN 3</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚡ Sobrecarga de Energía: Inyección de Payloads</span>
      <span class="step-tile-desc">Inyecta etaHEN y ps5-kstuff mediante autoloader USB o Netcat en el puerto 9021</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">INYECCIÓN DE PAYLOADS</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DE LA MISIÓN:</strong> Enviar y ejecutar los payloads fundamentales (<code>etaHEN</code> y <code>ps5-kstuff</code>) para deshabilitar las protecciones del sistema y habilitar homebrew.
</div>

### 🎒 Equipamiento Necesario
- Memoria USB formateada en **exFAT** (Opción 1) O Terminal de PC con Netcat / PowerShell (Opción 2)
- Binarios de Payloads: `etaHEN.bin`, `ps5-kstuff.bin`

### ⚡ Ejecución Táctica: Opciones de Inyección

#### Opción 1: Carga Automática por USB (Recomendada)
1. Formatea una memoria USB en **exFAT** con tabla de particiones MBR.
2. Crea una carpeta llamada `payloads` en la raíz de la memoria USB:
   ```text
   Memoria USB (exFAT):
   └── payloads/
       ├── etaHEN.bin
       └── ps5-kstuff.bin
   ```
3. Conecta la memoria USB en uno de los **puertos USB 3.0 traseros** de la consola.
4. Al activar el exploit en el navegador, ¡el cargador detecta y ejecuta automáticamente los payloads de la unidad USB!

---

#### Opción 2: Inyección por Red mediante Terminal (Netcat)
Envía los payloads desde tu ordenador hacia la IP de tu PS5 en el **Puerto 9021**:

```bash
# En Linux / macOS / WSL:
nc -w 3 <IP_DE_LA_PS5> 9021 < etaHEN.bin
nc -w 3 <IP_DE_LA_PS5> 9021 < ps5-kstuff.bin
```

```powershell
# En Windows (PowerShell):
$ps5_ip = "192.168.1.150"
$bytes = [System.IO.File]::ReadAllBytes("etaHEN.bin")
$client = New-Object System.Net.Sockets.TcpClient($ps5_ip, 9021)
$stream = $client.GetStream()
$stream.Write($bytes, 0, $bytes.Length)
$stream.Close(); $client.Close()
Write-Host "[ÉXITO] etaHEN desplegado en la PS5!"
```

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🥇 Trofeo de Oro &bull; <em>"Soberano del Kernel"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-3" data-todo-text="Marcar Completada" data-done-text="Misión Completada" onclick="toggleQuest('quest-step-3', 'Soberano del Kernel', 'Trofeo de Oro', '⚡')">
    <span>◯</span> Marcar Completada
  </button>
</div>

</details>

<!-- MISIÓN 4 -->
<details class="step-tile" data-quest="quest-step-4">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISIÓN 4</span>
    <span class="step-tile-text">
      <span class="step-tile-title">👑 Liberación Total: Homebrew y Backups</span>
      <span class="step-tile-desc">Despliega etaHEN Toolbox, servidor FTP puerto 1337, Itemzflow y Apollo Save Tool</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">ROOT LIBERADO</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DE LA MISIÓN:</strong> Establecer el ecosistema integral de homebrew y gestión de backups de juegos en tu PlayStation 5 liberada.
</div>

### 🎒 Equipamiento Necesario
- Cliente FTP (FileZilla / WinSCP)
- Paquetes Homebrew: `Itemzflow.pkg`, `Apollo.pkg`

### ⚡ Ejecución Táctica
1. **Verificar etaHEN Toolbox**:
   - Abre **Ajustes ➔ Sistema**.
   - Confirma la presencia del nuevo menú **etaHEN Toolbox**.
2. **Acceder al Servidor FTP de Alta Velocidad**:
   - etaHEN inicializa automáticamente un daemon FTP en el **Puerto 1337**.
   - Conéctate mediante FileZilla / WinSCP con credenciales anónimas.
3. **Ejecutar el Gestor de Juegos Itemzflow**:
   - Instala `Itemzflow.pkg` y ábrelo desde la pantalla de inicio.
   - Realiza un dump de tus discos físicos y compras digitales hacia un disco duro externo USB o un SSD NVMe M.2 interno.
   - Inicia backups de juegos directamente desde el almacenamiento USB sin necesidad de copiarlos al disco interno.
4. **Gestionar Partidas con Apollo Save Tool**:
   - Exporta, importa y refirma partidas guardadas entre diferentes cuentas de PSN de forma totalmente offline.

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🏆 Trofeo de Platino &bull; <em>"Maestro Absoluto del Root"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-4" data-todo-text="Marcar Completada" data-done-text="Misión Completada" onclick="toggleQuest('quest-step-4', 'Maestro Absoluto del Root', 'Trofeo de Platino', '👑')">
    <span>◯</span> Marcar Completada
  </button>
</div>

</details>

<!-- RESPAWN / RECUPERACIÓN -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number warning">RESPAWN</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🚑 Diagnóstico y Punto de Recuperación de Panics</span>
      <span class="step-tile-desc">Recuperación de Kernel Panics, desbordamientos de memoria, desync de DNS y errores CE-xxxx</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag warning">CHECKPOINT</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🚑 INTEL DE RESPAWN:</strong> Las disputas de temporización (race conditions) en el exploit pueden provocar Kernel Panics inofensivos. Consulta esta tabla de campo para retomar el control de inmediato.
</div>

| Anomalía / Síntoma | Causa Raíz | Solución Inmediata |
| :--- | :--- | :--- |
| **Pantalla negra instantánea / Apagado** | Kernel Panic durante la sincronización de la race condition | Espera 30s. Pulsa el botón físico de encendido. Deja que termine la reparación de almacenamiento y reinicia el exploit. |
| **"Memoria del sistema insuficiente"** | Desbordamiento en heap grooming de WebKit | Pulsa `Aceptar`, recarga la página o borra las cookies del navegador en los ajustes. |
| **La Guía del usuario abre la web de Sony** | Desincronización de DNS o el router omite el DNS manual | Revisa los Ajustes de red; asegúrate de que el DNS Primario sea `45.56.67.85` y el Secundario sea `0.0.0.0`. |
| **Conexión rechazada en puerto 9021** | La Fase 2 falló o `elfldr` se cerró inesperadamente | Vuelve a abrir la Guía del usuario hasta que aparezca el aviso de escucha en el puerto 9021. |
| **Los juegos no inician con error CE-xxxx** | El payload `ps5-kstuff` no está cargado en memoria | Asegúrate de cargar `kstuff` o `etaHEN` antes de ejecutar juegos. |

</details>

---

<p align="center">
  <b>¿Necesitas detalles técnicos profundos, primitivas de memoria, syscalls o puertos de red?</b><br>
  👉 Consulta la guía complementaria: <b><a href="jailbreak_tech_info.md">PS5 Jailbreak: Análisis Técnico Detallado (Tech Info)</a></b>
</p>
