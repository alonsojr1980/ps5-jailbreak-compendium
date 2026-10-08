<h1 align="center" class="ps-main-header">Interactive PS5<br>⚡ Jailbreak & Exploit Wizard ⚡</h1>
<p align="center" class="ps-header-author">by ALONSOJR1980</p>

<div align="center">

[![Firmwares](https://img.shields.io/badge/Asistente%20Interactivo-Rutas%20de%20Firmware-success?style=for-the-badge&logo=playstation&logoColor=white)](#)
[![Guía](https://img.shields.io/badge/Guía-Paso%20a%20Paso-blueviolet?style=for-the-badge&logo=playstation&logoColor=white)](#)

**Idiomas / Languages:**
[🇪🇸 Español](README.md) | [🇺🇸 English](../en/README.md) | [🇧🇷 Versão em Português](../pt/README.md)

</div>

Selecciona el modelo de tu PS5 y el rango de firmware para ver instrucciones adecuadas para tu consola. Sigue los pasos que aparecen abajo; no necesitas aprender cómo funciona el software.

---

<!-- COMPONENTE DEL WIZARD INTERACTIVO -->
<div class="ps-wizard-container" id="psWizard">
<div class="ps-wizard-header">
<div class="ps-wizard-badge">⚡ ASISTENTE INTERACTIVO DE FIRMWARE</div>
<h2 class="ps-wizard-title">Configuración de PS5 paso a paso</h2>
<p class="ps-wizard-subtitle">Elige el modelo de tu consola y el rango de firmware para ver los pasos correspondientes.</p>
</div>
<div class="ps-wizard-controls">
<!-- Paso 1: Selección de Modelo -->
<div class="ps-wizard-step" id="wizardStep1">
<div class="ps-wizard-bookmark" aria-hidden="true">
<span class="ps-bm-num">01</span>
<span class="ps-bm-text">MODELO</span>
</div>
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
</div>
<!-- Paso 2: Selección de Firmware -->
<div class="ps-wizard-step" id="wizardStep2">
<div class="ps-wizard-bookmark" aria-hidden="true">
<span class="ps-bm-num">02</span>
<span class="ps-bm-text">FIRMWARE</span>
</div>
<div class="ps-wizard-field">
<label class="ps-wizard-label">2. ELIGE EL RANGO DE FIRMWARE:</label>
<div class="ps-exploit-grid">
<button type="button" class="ps-exploit-btn active" data-fw="7.00 - 13.60" onclick="setWizardFw('7.00 - 13.60')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 7.00–13.60</span>
<span class="ps-exploit-badge ready">PASOS DISPONIBLES</span>
</div>
<div class="ps-exploit-sub">Exploit WebKit + aio_multi_wait en kernel (Relapse). Configuración directa en navegador.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="3.00 - 6.50" onclick="setWizardFw('3.00 - 6.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 3.00–6.50</span>
<span class="ps-exploit-badge ready">PASOS DISPONIBLES</span>
</div>
<div class="ps-exploit-sub">Exploits de kernel UMTX y Socket IPv6 UAF. Requiere memoria USB para los payloads.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 1.00–2.50</span>
<span class="ps-exploit-badge ready">PASOS DISPONIBLES</span>
</div>
<div class="ps-exploit-sub">Acceso total Byepervisor a Hypervisor (Ring -1) y lectura/escritura de kernel.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="14.00+" onclick="setWizardFw('14.00+')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 14.00 o superior</span>
<span class="ps-exploit-badge patched">NO EXPLOITABLE</span>
</div>
<div class="ps-exploit-sub">Parcheado por Sony. Sin exploit público. Mantén la consola estrictamente offline.</div>
</button>
</div>
<div class="ps-ip-wrap">
<label for="customIpInput" class="ps-ip-label">
<span class="ps-ip-title">Dirección IP de la Consola (opcional):</span>
<span class="ps-ip-desc">Se usa para completar los comandos si eliges el método con ordenador o teléfono.</span>
</label>
<input type="text" id="customIpInput" class="ps-input" inputmode="decimal" autocomplete="off" aria-describedby="customIpError" value="192.168.1.150" placeholder="192.168.1.xxx" oninput="onCustomIpInput(this.value)">
<span id="customIpError" class="ps-ip-error" role="alert">Introduce una dirección IP válida, por ejemplo 192.168.1.150.</span>
</div>
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
> - El lector de discos extraíble necesita un registro en línea único con Sony para vincularse a la consola.
> - **Nunca te conectes a PSN para registrar el lector si la consola está en un firmware vulnerable (<= 13.60)**, ya que esto **forzará una actualización irreversible al firmware más reciente**.
> - Backups digitales, emuladores, homebrew y almacenamiento en SSD M.2 funcionan al 100% sin el lector físico emparejado.

---

<p align="center">
  <b>🤖 Asistente Interactivo de Firmware para la Comunidad PS5</b><br>
  <i>Selecciona tu modelo y firmware para generar instrucciones personalizadas y seguras de jailbreak.</i>
</p>
