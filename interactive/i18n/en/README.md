# ⚡ Interactive PS5 Jailbreak & Exploit Wizard
### *by ALONSOJR1980*

<div align="center">

[![PS5 Firmware](https://img.shields.io/badge/Interactive%20Wizard-FW%201.00%20--%2013.60-success?style=for-the-badge&logo=playstation&logoColor=white)](#)
[![Exploit](https://img.shields.io/badge/Custom%20Generator-Relapse%20%7C%20UMTX-blueviolet?style=for-the-badge&logo=codeforces&logoColor=white)](#)
[![Payloads](https://img.shields.io/badge/Payloads-etaHEN%20%7C%20ps5--kstuff-ff69b4?style=for-the-badge&logo=coffeescript&logoColor=white)](#)

**Languages / Idiomas:**
[🇺🇸 English](README.md) | [🇧🇷 Versão em Português](../pt/README.md) | [🇪🇸 Versión en Español](../es/README.md)

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
<label class="ps-wizard-label">2. SELECT YOUR FIRMWARE:</label>
<div class="ps-fw-sections">
<div class="ps-fw-group" data-group="9.60 - 13.60">
<div class="ps-fw-group-header">
<span class="ps-fw-group-title">9.60 – 13.60</span>
<span class="ps-fw-group-badge ready">WebKit + Relapse</span>
</div>
<div class="ps-fw-pills">
<button type="button" class="ps-fw-btn active" data-fw="9.60 - 13.60" onclick="setWizardFw('9.60 - 13.60')">All (9.60 – 13.60)</button>
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
<button type="button" class="ps-fw-btn" data-fw="7.00 - 8.20" onclick="setWizardFw('7.00 - 8.20')">All (7.00 – 8.20)</button>
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
<button type="button" class="ps-fw-btn" data-fw="6.00 - 6.50" onclick="setWizardFw('6.00 - 6.50')">All (6.00 – 6.50)</button>
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
<button type="button" class="ps-fw-btn" data-fw="5.00 - 5.50" onclick="setWizardFw('5.00 - 5.50')">All (5.00 – 5.50)</button>
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
<button type="button" class="ps-fw-btn" data-fw="3.00 - 4.51" onclick="setWizardFw('3.00 - 4.51')">All (3.00 – 4.51)</button>
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
<button type="button" class="ps-fw-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">All (1.00 – 2.50)</button>
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
<span class="ps-ip-title">Console IP Address (optional):</span>
<span class="ps-ip-desc">Tailors netcat commands in the execution checklist below to your console.</span>
</label>
<input type="text" id="customIpInput" class="ps-input" value="192.168.1.150" placeholder="192.168.1.xxx" oninput="onCustomIpInput(this.value)">
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
