# ⚡ Asistente Interactivo de Jailbreak & Exploit para PS5
### *by ALONSOJR1980*

<div align="center">

[![Firmwares Soportados](https://img.shields.io/badge/Asistente%20Interactivo-FW%201.00%20--%2013.60-success?style=for-the-badge&logo=playstation&logoColor=white)](https://github.com/alonsojr1980/ps5-jailbreak-compendium)
[![Exploit](https://img.shields.io/badge/Generador%20Personalizado-Relapse%20%7C%20UMTX-blueviolet?style=for-the-badge&logo=codeforces&logoColor=white)](../../../i18n/es/jailbreak_tech_info.md)
[![Sitio Web Online](https://img.shields.io/badge/Sitio%20Web-GitHub%20Pages-00d2ff?style=for-the-badge&logo=githubpages&logoColor=white)](https://alonsojr1980.github.io/ps5-jailbreak-compendium/#/interactive/i18n/es/)
[![Payloads](https://img.shields.io/badge/Payloads-etaHEN%20%7C%20ps5--kstuff-ff69b4?style=for-the-badge&logo=coffeescript&logoColor=white)](../../../i18n/es/jailbreak_tech_info.md#4-ingenier%C3%ADa-de-payloads--frameworks-del-sistema)

**Navegación / Navigation:**
[🚀 Guía Práctica Paso a Paso](../../../i18n/es/jailbreak_how_to.md) | [🔬 Análisis Técnico Detallado](../../../i18n/es/jailbreak_tech_info.md) | [🇺🇸 English Version](../en/README.md) | [🇧🇷 Versão em Português](../pt/README.md) | [🌐 Portal Principal](../../../README.md)

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
      <label class="ps-wizard-label">2. SELECCIONA O ESCRIBE TU FIRMWARE:</label>
      <div class="ps-fw-quick-picks">
        <button type="button" class="ps-fw-btn active" data-fw="13.60" onclick="setWizardFw('13.60')">13.60</button>
        <button type="button" class="ps-fw-btn" data-fw="9.60" onclick="setWizardFw('9.60')">9.60</button>
        <button type="button" class="ps-fw-btn" data-fw="8.20" onclick="setWizardFw('8.20')">8.20</button>
        <button type="button" class="ps-fw-btn" data-fw="7.61" onclick="setWizardFw('7.61')">7.61</button>
        <button type="button" class="ps-fw-btn" data-fw="5.50" onclick="setWizardFw('5.50')">5.50</button>
        <button type="button" class="ps-fw-btn" data-fw="4.51" onclick="setWizardFw('4.51')">4.51</button>
        <button type="button" class="ps-fw-btn" data-fw="2.50" onclick="setWizardFw('2.50')">2.50</button>
        <button type="button" class="ps-fw-btn" data-fw="1.00" onclick="setWizardFw('1.00')">1.00</button>
      </div>
      <div class="ps-fw-custom-wrap">
        <div class="ps-input-field">
          <label for="customFwInput">O escribe el firmware exacto:</label>
          <input type="text" id="customFwInput" class="ps-input" value="13.60" placeholder="ej. 08.00 o 04.03" oninput="onCustomFwInput(this.value)">
        </div>
        <div class="ps-input-field">
          <label for="customIpInput">IP de la Consola (opcional para scripts):</label>
          <input type="text" id="customIpInput" class="ps-input" value="192.168.1.150" placeholder="192.168.1.xxx" oninput="onCustomIpInput(this.value)">
        </div>
      </div>
    </div>
  </div>

  <!-- Resultado Dinámico -->
  <div id="psWizardResult" class="ps-wizard-result">
    <!-- Rellenado dinámicamente por window.initJailbreakWizard() -->
  </div>
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
  <b>¿Buscas el tutorial paso a paso o el análisis técnico a bajo nivel?</b><br>
  👉 <a href="../../../i18n/es/jailbreak_how_to.md"><b>Guía Práctica Paso a Paso</b></a> &bull; <a href="../../../i18n/es/jailbreak_tech_info.md"><b>Análisis Técnico Detallado</b></a>
</p>
