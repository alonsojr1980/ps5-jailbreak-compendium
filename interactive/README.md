# ⚡ Interactive PS5 Jailbreak & Exploit Wizard
### *by ALONSOJR1980*

<div align="center">

[![PS5 Firmware](https://img.shields.io/badge/Interactive%20Wizard-FW%201.00%20--%2013.60-success?style=for-the-badge&logo=playstation&logoColor=white)](#)
[![Exploit](https://img.shields.io/badge/Custom%20Generator-Relapse%20%7C%20UMTX-blueviolet?style=for-the-badge&logo=codeforces&logoColor=white)](#)
[![Payloads](https://img.shields.io/badge/Payloads-etaHEN%20%7C%20ps5--kstuff-ff69b4?style=for-the-badge&logo=coffeescript&logoColor=white)](#)

**Languages / Idiomas:**
[🇺🇸 English](README.md) | [🇧🇷 Versão em Português](i18n/pt/README.md) | [🇪🇸 Versión en Español](i18n/es/README.md)

</div>

Select your PlayStation 5 hardware model and firmware version below to instantly generate a tailored, zero-fluff deployment guide, pre-configured DNS settings, and customized terminal payload injection commands.

---

<!-- INTERACTIVE WIZARD COMPONENT -->
<div class="ps-wizard-container" id="psWizard">
<div class="ps-wizard-header">
<div class="ps-wizard-badge">⚡ INTERACTIVE FIRMWARE WIZARD</div>
<h2 class="ps-wizard-title">Tailor-Made Jailbreak & Exploit Generator</h2>
<p class="ps-wizard-subtitle">Select your PS5 hardware model and firmware version to generate custom deployment instructions.</p>
</div>
<div class="ps-wizard-controls">
<!-- Model Selection -->
<div class="ps-wizard-field">
<label class="ps-wizard-label">1. SELECT YOUR HARDWARE MODEL:</label>
<div class="ps-model-buttons">
<button type="button" class="ps-model-btn active" data-model="fat" onclick="setWizardModel('fat')">
<span class="model-icon">🕹️</span>
<span class="model-name">PS5 Fat</span>
<span class="model-sub">CFI-1000 / 1100 / 1200</span>
</button>
<button type="button" class="ps-model-btn" data-model="slim" onclick="setWizardModel('slim')">
<span class="model-icon">🕹️</span>
<span class="model-name">PS5 Slim</span>
<span class="model-sub">CFI-2000 (Detachable Drive)</span>
</button>
<button type="button" class="ps-model-btn" data-model="pro" onclick="setWizardModel('pro')">
<span class="model-icon">🚀</span>
<span class="model-name">PS5 Pro</span>
<span class="model-sub">CFI-7000 (Detachable Drive)</span>
</button>
</div>
</div>
<!-- Firmware Selection -->
<div class="ps-wizard-field">
<label class="ps-wizard-label">2. SELECT OR ENTER YOUR FIRMWARE:</label>
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
<label for="customFwInput">Or type specific firmware:</label>
<input type="text" id="customFwInput" class="ps-input" value="13.60" placeholder="e.g. 08.00 or 04.03" oninput="onCustomFwInput(this.value)">
</div>
<div class="ps-input-field">
<label for="customIpInput">Console IP (optional for payload commands):</label>
<input type="text" id="customIpInput" class="ps-input" value="192.168.1.150" placeholder="192.168.1.xxx" oninput="onCustomIpInput(this.value)">
</div>
</div>
</div>
</div>
<!-- Dynamic Result Card -->
<div id="psWizardResult" class="ps-wizard-result"></div>
</div>

---

## 🛡️ Global Pre-Jailbreak Hardening Checklist

Regardless of your hardware model or firmware bracket, always execute these anti-update steps before connecting to any Wi-Fi or LAN network:

1. **System Software Settings**:
   - Navigate to **Settings ➔ System ➔ System Software ➔ System Software Updates and Settings**.
   - Turn **OFF** *Download Update Files Automatically*.
   - Turn **OFF** *Install Update Files Automatically*.
2. **Power Saving in Rest Mode**:
   - Navigate to **Settings ➔ System ➔ Power Saving ➔ Features Available in Rest Mode**.
   - Turn **OFF** *Stay Connected to the Internet*.
3. **Automatic Game & App Downloads**:
   - Navigate to **Settings ➔ Saved Data and Game/App Settings ➔ Automatic Updates**.
   - Turn **OFF** *Auto-Download* and *Auto-Install in Rest Mode*.

---

## ⚠️ Detachable Disc Drive Critical Reminder

> [!CAUTION]
> If your console is a **PS5 Slim (CFI-2000)** or **PS5 Pro (CFI-7000)**:
> - The detachable disc drive requires a one-time cryptographic **Handshake** with Sony servers to pair with the motherboard.
> - **Never connect to PSN to pair the drive on an exploitable firmware (<= 13.60)**, as it will **force an irreversible update to the latest patched firmware**.
> - Games, digital dumps, emulators, homebrew, and internal M.2 SSD storage work 100% without the physical disc drive paired.

---

<p align="center">
  <b>🤖 Interactive Firmware Wizard for the PS5 Community</b><br>
  <i>Select your hardware and firmware to generate custom offline jailbreak instructions.</i>
</p>
