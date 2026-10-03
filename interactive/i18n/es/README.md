<h1 align="center" class="ps-main-header">⚡ Interactive PS5<br>Jailbreak & Exploit Wizard ⚡</h1>
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
<label class="ps-wizard-label">2. ELIGE EL RANGO DE FIRMWARE:</label>
<div class="ps-exploit-grid">
<button type="button" class="ps-exploit-btn active" data-fw="9.60 - 13.60" onclick="setWizardFw('9.60 - 13.60')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 9.60–13.60</span>
<span class="ps-exploit-badge ready">PASOS DISPONIBLES</span>
</div>
<div class="ps-exploit-range">Firmware 9.60 – 13.60</div>
<div class="ps-exploit-sub">Sigue los pasos que aparecen para este rango de firmware.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="14.00+" onclick="setWizardFw('14.00+')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 14.00 o superior</span>
<span class="ps-exploit-badge wip">SIN PASOS</span>
</div>
<div class="ps-exploit-range">Firmware 14.00+</div>
<div class="ps-exploit-sub">Este asistente no tiene una ruta para esta versión. Mantén la consola sin conexión.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="7.00 - 8.20" onclick="setWizardFw('7.00 - 8.20')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 7.00–8.20</span>
<span class="ps-exploit-badge wip">VERIFICA LA RUTA</span>
</div>
<div class="ps-exploit-range">Firmware 7.00 – 8.20</div>
<div class="ps-exploit-sub">Este asistente aún no incluye todos los pasos para este rango.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="6.00 - 6.50" onclick="setWizardFw('6.00 - 6.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 6.00–6.50</span>
<span class="ps-exploit-badge wip">AÚN NO LISTO</span>
</div>
<div class="ps-exploit-range">Firmware 6.00 – 6.50</div>
<div class="ps-exploit-sub">Aún no hay instrucciones paso a paso para este rango.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="5.00 - 5.50" onclick="setWizardFw('5.00 - 5.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 5.00–5.50</span>
<span class="ps-exploit-badge ready">PASOS DISPONIBLES</span>
</div>
<div class="ps-exploit-range">Firmware 5.00 – 5.50</div>
<div class="ps-exploit-sub">Sigue los pasos que aparecen para este rango de firmware.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="3.00 - 4.51" onclick="setWizardFw('3.00 - 4.51')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 3.00–4.51</span>
<span class="ps-exploit-badge ready">PASOS DISPONIBLES</span>
</div>
<div class="ps-exploit-range">Firmware 3.00 – 4.51</div>
<div class="ps-exploit-sub">Sigue los pasos que aparecen para este rango de firmware.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 1.00–2.50</span>
<span class="ps-exploit-badge wip">VERIFICA LA RUTA</span>
</div>
<div class="ps-exploit-range">Firmware 1.00 – 2.50</div>
<div class="ps-exploit-sub">Este asistente aún no incluye todos los pasos para este rango.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="8.21 - 9.59" onclick="setWizardFw('8.21 - 9.59')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Verificar compatibilidad</span>
<span class="ps-exploit-badge wip">SIN PASOS</span>
</div>
<div class="ps-exploit-range">Firmware 8.21 – 9.59</div>
<div class="ps-exploit-sub">Este asistente no tiene una ruta verificada para este rango.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="unlisted" onclick="setWizardFw('unlisted')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Mi firmware no aparece en la lista</span>
<span class="ps-exploit-badge wip">VERIFICA PRIMERO</span>
</div>
<div class="ps-exploit-range">Otra versión de firmware</div>
<div class="ps-exploit-sub">No elijas un rango cercano; verifica primero la compatibilidad.</div>
</button>
</div>
<div class="ps-ip-wrap">
<label for="customIpInput" class="ps-ip-label">
<span class="ps-ip-title">Dirección IP de la Consola (opcional):</span>
<span class="ps-ip-desc">Se usa para completar los comandos si eliges el método con ordenador o teléfono.</span>
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
> - El lector de discos extraíble necesita un registro en línea único con Sony para vincularse a la consola.
> - **Nunca te conectes a PSN para registrar el lector si la consola está en un firmware vulnerable (<= 13.60)**, ya que esto **forzará una actualización irreversible al firmware más reciente**.
> - Backups digitales, emuladores, homebrew y almacenamiento en SSD M.2 funcionan al 100% sin el lector físico emparejado.

---

<p align="center">
  <b>🤖 Asistente Interactivo de Firmware para la Comunidad PS5</b><br>
  <i>Selecciona tu modelo y firmware para generar instrucciones personalizadas y seguras de jailbreak.</i>
</p>
