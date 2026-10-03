# ⚡ Asistente Interactivo de Jailbreak & Exploit para PS5
### *by ALONSOJR1980*

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
<label class="ps-wizard-label">2. SELECCIONA TU FIRMWARE:</label>
<div class="ps-fw-sections">
<div class="ps-fw-group" data-group="9.60 - 13.60">
<div class="ps-fw-group-header">
<span class="ps-fw-group-title">9.60 – 13.60</span>
<span class="ps-fw-group-badge ready">WebKit + Relapse</span>
</div>
<div class="ps-fw-pills">
<button type="button" class="ps-fw-btn active" data-fw="9.60 - 13.60" onclick="setWizardFw('9.60 - 13.60')">Todos (9.60 – 13.60)</button>
<button type="button" class="ps-fw-btn" data-fw="13.60" onclick="setWizardFw('13.60')">13.60</button>
<button type="button" class="ps-fw-btn" data-fw="13.00" onclick="setWizardFw('13.00')">13.00</button>
<button type="button" class="ps-fw-btn" data-fw="12.00" onclick="setWizardFw('12.00')">12.00</button>
<button type="button" class="ps-fw-btn" data-fw="11.50" onclick="setWizardFw('11.50')">11.50</button>
<button type="button" class="ps-fw-btn" data-fw="11.00" onclick="setWizardFw('11.00')">11.00</button>
<button type="button" class="ps-fw-btn" data-fw="10.50" onclick="setWizardFw('10.50')">10.50</button>
<button type="button" class="ps-fw-btn" data-fw="10.01" onclick="setWizardFw('10.01')">10.01</button>
<button type="button" class="ps-fw-btn" data-fw="10.00" onclick="setWizardFw('10.00')">10.00</button>
<button type="button" class="ps-fw-btn" data-fw="9.60" onclick="setWizardFw('9.60')">9.60</button>
<button type="button" class="ps-fw-btn" data-fw="9.00 - 9.40" onclick="setWizardFw('9.00 - 9.40')">9.00 – 9.40</button>
<button type="button" class="ps-fw-btn" data-fw="8.40 - 8.60" onclick="setWizardFw('8.40 - 8.60')">8.40 – 8.60</button>
</div>
</div>
<div class="ps-fw-group" data-group="7.00 - 8.20">
<div class="ps-fw-group-header">
<span class="ps-fw-group-title">7.00 – 8.20</span>
<span class="ps-fw-group-badge ready">BD-JB / Mast1c0re</span>
</div>
<div class="ps-fw-pills">
<button type="button" class="ps-fw-btn" data-fw="7.00 - 8.20" onclick="setWizardFw('7.00 - 8.20')">Todos (7.00 – 8.20)</button>
<button type="button" class="ps-fw-btn" data-fw="8.20" onclick="setWizardFw('8.20')">8.20</button>
<button type="button" class="ps-fw-btn" data-fw="8.00" onclick="setWizardFw('8.00')">8.00</button>
<button type="button" class="ps-fw-btn" data-fw="7.61" onclick="setWizardFw('7.61')">7.61</button>
<button type="button" class="ps-fw-btn" data-fw="7.60" onclick="setWizardFw('7.60')">7.60</button>
<button type="button" class="ps-fw-btn" data-fw="7.40" onclick="setWizardFw('7.40')">7.40</button>
<button type="button" class="ps-fw-btn" data-fw="7.20" onclick="setWizardFw('7.20')">7.20</button>
<button type="button" class="ps-fw-btn" data-fw="7.01" onclick="setWizardFw('7.01')">7.01</button>
<button type="button" class="ps-fw-btn" data-fw="7.00" onclick="setWizardFw('7.00')">7.00</button>
</div>
</div>
<div class="ps-fw-group" data-group="6.00 - 6.50">
<div class="ps-fw-group-header">
<span class="ps-fw-group-title">6.00 – 6.50</span>
<span class="ps-fw-group-badge wip">UMTX2 / Mast1c0re</span>
</div>
<div class="ps-fw-pills">
<button type="button" class="ps-fw-btn" data-fw="6.00 - 6.50" onclick="setWizardFw('6.00 - 6.50')">Todos (6.00 – 6.50)</button>
<button type="button" class="ps-fw-btn" data-fw="6.50" onclick="setWizardFw('6.50')">6.50</button>
<button type="button" class="ps-fw-btn" data-fw="6.02" onclick="setWizardFw('6.02')">6.02</button>
<button type="button" class="ps-fw-btn" data-fw="6.00" onclick="setWizardFw('6.00')">6.00</button>
</div>
</div>
<div class="ps-fw-group" data-group="5.00 - 5.50">
<div class="ps-fw-group-header">
<span class="ps-fw-group-title">5.00 – 5.50</span>
<span class="ps-fw-group-badge ready">UMTX Exploit</span>
</div>
<div class="ps-fw-pills">
<button type="button" class="ps-fw-btn" data-fw="5.00 - 5.50" onclick="setWizardFw('5.00 - 5.50')">Todos (5.00 – 5.50)</button>
<button type="button" class="ps-fw-btn" data-fw="5.50" onclick="setWizardFw('5.50')">5.50</button>
<button type="button" class="ps-fw-btn" data-fw="5.10" onclick="setWizardFw('5.10')">5.10</button>
<button type="button" class="ps-fw-btn" data-fw="5.02" onclick="setWizardFw('5.02')">5.02</button>
<button type="button" class="ps-fw-btn" data-fw="5.00" onclick="setWizardFw('5.00')">5.00</button>
</div>
</div>
<div class="ps-fw-group" data-group="3.00 - 4.51">
<div class="ps-fw-group-header">
<span class="ps-fw-group-title">3.00 – 4.51</span>
<span class="ps-fw-group-badge ready">IPv6 UAF / UMTX</span>
</div>
<div class="ps-fw-pills">
<button type="button" class="ps-fw-btn" data-fw="3.00 - 4.51" onclick="setWizardFw('3.00 - 4.51')">Todos (3.00 – 4.51)</button>
<button type="button" class="ps-fw-btn" data-fw="4.51" onclick="setWizardFw('4.51')">4.51</button>
<button type="button" class="ps-fw-btn" data-fw="4.50" onclick="setWizardFw('4.50')">4.50</button>
<button type="button" class="ps-fw-btn" data-fw="4.03" onclick="setWizardFw('4.03')">4.03</button>
<button type="button" class="ps-fw-btn" data-fw="4.02" onclick="setWizardFw('4.02')">4.02</button>
<button type="button" class="ps-fw-btn" data-fw="4.00" onclick="setWizardFw('4.00')">4.00</button>
<button type="button" class="ps-fw-btn" data-fw="3.21" onclick="setWizardFw('3.21')">3.21</button>
<button type="button" class="ps-fw-btn" data-fw="3.20" onclick="setWizardFw('3.20')">3.20</button>
<button type="button" class="ps-fw-btn" data-fw="3.10" onclick="setWizardFw('3.10')">3.10</button>
<button type="button" class="ps-fw-btn" data-fw="3.00" onclick="setWizardFw('3.00')">3.00</button>
</div>
</div>
<div class="ps-fw-group" data-group="1.00 - 2.50">
<div class="ps-fw-group-header">
<span class="ps-fw-group-title">1.00 – 2.50</span>
<span class="ps-fw-group-badge special">Byepervisor • Ring -1</span>
</div>
<div class="ps-fw-pills">
<button type="button" class="ps-fw-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">Todos (1.00 – 2.50)</button>
<button type="button" class="ps-fw-btn" data-fw="2.50" onclick="setWizardFw('2.50')">2.50</button>
<button type="button" class="ps-fw-btn" data-fw="2.30" onclick="setWizardFw('2.30')">2.30</button>
<button type="button" class="ps-fw-btn" data-fw="2.26" onclick="setWizardFw('2.26')">2.26</button>
<button type="button" class="ps-fw-btn" data-fw="2.25" onclick="setWizardFw('2.25')">2.25</button>
<button type="button" class="ps-fw-btn" data-fw="2.20" onclick="setWizardFw('2.20')">2.20</button>
<button type="button" class="ps-fw-btn" data-fw="2.00" onclick="setWizardFw('2.00')">2.00</button>
<button type="button" class="ps-fw-btn" data-fw="1.14" onclick="setWizardFw('1.14')">1.14</button>
<button type="button" class="ps-fw-btn" data-fw="1.12" onclick="setWizardFw('1.12')">1.12</button>
<button type="button" class="ps-fw-btn" data-fw="1.11" onclick="setWizardFw('1.11')">1.11</button>
<button type="button" class="ps-fw-btn" data-fw="1.02" onclick="setWizardFw('1.02')">1.02</button>
<button type="button" class="ps-fw-btn" data-fw="1.01" onclick="setWizardFw('1.01')">1.01</button>
<button type="button" class="ps-fw-btn" data-fw="1.00" onclick="setWizardFw('1.00')">1.00</button>
</div>
</div>
</div>
<div class="ps-ip-wrap">
<label for="customIpInput" class="ps-ip-label">
<span class="ps-ip-title">Dirección IP de la Consola (opcional):</span>
<span class="ps-ip-desc">Personaliza los comandos netcat en la lista de ejecución inferior para tu consola.</span>
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
