<h1 align="center" class="ps-main-header">⚡ Interactive PS5<br>Jailbreak & Exploit Wizard ⚡</h1>
<p align="center" class="ps-header-author">by ALONSOJR1980</p>

<div align="center">

[![Firmwares Soportados](https://img.shields.io/badge/Asistente%20Interactivo-FW%201.00%20--%2013.60-success?style=for-the-badge&logo=playstation&logoColor=white)](#)
[![Exploit](https://img.shields.io/badge/Generador%20Personalizado-Relapse%20%7C%20UMTX-blueviolet?style=for-the-badge&logo=codeforces&logoColor=white)](#)
[![Payloads](https://img.shields.io/badge/Payloads-etaHEN%20%7C%20ps5--kstuff-ff69b4?style=for-the-badge&logo=coffeescript&logoColor=white)](#)

**Idiomas / Languages:**
[🇪🇸 Español](README.md) | [🇺🇸 English](../en/README.md) | [🇧🇷 Versão em Português](../pt/README.md)

</div>

Selecciona el modelo de tu consola PlayStation 5 y la versión de tu firmware a continuación para generar al instante una guía de despliegue personalizada, configuraciones de DNS recomendadas y comandos de inyección de payload para la terminal.

---

<!-- COMPONENTE DEL WIZARD INTERACTIVO -->
<div class="ps-wizard-container" id="psWizard">
<div class="ps-wizard-header">
<div class="ps-wizard-badge">⚡ ASISTENTE INTERACTIVO DE FIRMWARE</div>
<h2 class="ps-wizard-title">Generador a Medida de Jailbreak & Exploit</h2>
<p class="ps-wizard-subtitle">Selecciona el modelo de hardware de tu PS5 y la versión del firmware para obtener instrucciones personalizadas.</p>
</div>
<div class="ps-wizard-controls">
<!-- Selección de Modelo -->
<div class="ps-wizard-field">
<label class="ps-wizard-label">1. SELECCIONA EL MODELO DE CONSOLA:</label>
<div class="ps-model-buttons">
<button type="button" class="ps-model-btn active" data-model="fat" onclick="setWizardModel('fat')">
<span class="model-icon">🕹️</span>
<span class="model-name">PS5 Fat</span>
<span class="model-sub">CFI-1000 / 1100 / 1200</span>
</button>
<button type="button" class="ps-model-btn" data-model="slim" onclick="setWizardModel('slim')">
<span class="model-icon">🕹️</span>
<span class="model-name">PS5 Slim</span>
<span class="model-sub">CFI-2000 (Lector Extraíble)</span>
</button>
<button type="button" class="ps-model-btn" data-model="pro" onclick="setWizardModel('pro')">
<span class="model-icon">🚀</span>
<span class="model-name">PS5 Pro</span>
<span class="model-sub">CFI-7000 (Lector Extraíble)</span>
</button>
</div>
</div>
<!-- Selección de Firmware -->
<div class="ps-wizard-field">
<label class="ps-wizard-label">2. SELECCIONA EL TIPO DE EXPLOIT Y RANGO DE FIRMWARE:</label>
<div class="ps-exploit-grid">
<button type="button" class="ps-exploit-btn active" data-fw="9.60 - 13.60" onclick="setWizardFw('9.60 - 13.60')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Relapse Exploit</span>
<span class="ps-exploit-badge ready">WebKit</span>
</div>
<div class="ps-exploit-range">Firmware 9.60 – 13.60</div>
<div class="ps-exploit-sub">WebKit (JSC) + Exploit de Kernel aio_multi_wait</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="7.00 - 8.20" onclick="setWizardFw('7.00 - 8.20')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">BD-JB / Mast1c0re</span>
<span class="ps-exploit-badge ready">Disco / PS2</span>
</div>
<div class="ps-exploit-range">Firmware 7.00 – 8.20</div>
<div class="ps-exploit-sub">Disco Blu-ray BD-J / Savegame PS2 + aio_multi_wait</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="6.00 - 6.50" onclick="setWizardFw('6.00 - 6.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">UMTX2 / Mast1c0re</span>
<span class="ps-exploit-badge wip">En Progreso</span>
</div>
<div class="ps-exploit-range">Firmware 6.00 – 6.50</div>
<div class="ps-exploit-sub">Primitivas UMTX2 y Savegame PS2 (Porting en Progreso)</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="5.00 - 5.50" onclick="setWizardFw('5.00 - 5.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">UMTX Exploit</span>
<span class="ps-exploit-badge ready">Kernel UAF</span>
</div>
<div class="ps-exploit-range">Firmware 5.00 – 5.50</div>
<div class="ps-exploit-sub">Primitivas Mutex libthr FreeBSD (CVE-2024-43102)</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="3.00 - 4.51" onclick="setWizardFw('3.00 - 4.51')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">IPv6 Socket UAF</span>
<span class="ps-exploit-badge ready">Era Dorada</span>
</div>
<div class="ps-exploit-range">Firmware 3.00 – 4.51</div>
<div class="ps-exploit-sub">Socket UAF netinet6 FreeBSD / UMTX</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Byepervisor</span>
<span class="ps-exploit-badge special">Ring -1 Root</span>
</div>
<div class="ps-exploit-range">Firmware 1.00 – 2.50</div>
<div class="ps-exploit-sub">Control Total del Hypervisor (Santo Grial)</div>
</button>
</div>
<div class="ps-ip-wrap">
<label for="customIpInput" class="ps-ip-label">
<span class="ps-ip-title">Dirección IP de la Consola (opcional):</span>
<span class="ps-ip-desc">Personaliza los comandos netcat en la pestaña "CON PC/TELÉFONO" inferior para tu consola.</span>
</label>
<input type="text" id="customIpInput" class="ps-input" value="192.168.1.150" placeholder="192.168.1.xxx" oninput="onCustomIpInput(this.value)">
</div>
</div>
</div>
<!-- Resultado Dinámico -->
<div id="psWizardResult" class="ps-wizard-result"></div>
</div>

---

## 🛡️ Lista Global de Blindaje Pre-Jailbreak

Sin importar el modelo o rango de firmware, aplica estas configuraciones antes de conectar la consola a la red:

1. **Ajustes del Software del Sistema**:
   - Ve a **Ajustes ➔ Sistema ➔ Software del sistema ➔ Ajustes y actualizaciones del software del sistema**.
   - Desactiva **Descargar archivos de actualización automáticamente**.
   - Desactiva **Instalar archivos de actualización automáticamente**.
2. **Ahorro de Energía en Modo de Reposo (Rest Mode)**:
   - Ve a **Ajustes ➔ Sistema ➔ Ahorro de energía ➔ Funciones disponibles en modo de reposo**.
   - Desactiva **Mantenerse conectado a Internet**.
3. **Descargas Automáticas de Juegos y Aplicaciones**:
   - Ve a **Ajustes ➔ Datos guardados y ajustes de juegos/aplicaciones ➔ Actualizaciones automáticas**.
   - Desactiva **Descarga automática** e **Instalación automática en Rest Mode**.

---

## ⚠️ Recordatorio Crítico sobre el Lector Extraíble

> [!CAUTION]
> Si tu consola es una **PS5 Slim (CFI-2000)** o **PS5 Pro (CFI-7000)**:
> - El lector de discos extraíble requiere un **Handshake** criptográfico con los servidores de Sony para autenticarse por primera vez.
> - **Nunca te conectes a PSN para registrar el lector si la consola está en un firmware vulnerable (<= 13.60)**, ya que esto **forzará una actualización irreversible al firmware más reciente**.
> - Backups digitales, emuladores, homebrew y almacenamiento en SSD M.2 funcionan al 100% sin el lector físico emparejado.

---

<p align="center">
  <b>🤖 Asistente Interactivo de Firmware para la Comunidad PS5</b><br>
  <i>Selecciona tu modelo y firmware para generar instrucciones personalizadas y seguras de jailbreak.</i>
</p>
