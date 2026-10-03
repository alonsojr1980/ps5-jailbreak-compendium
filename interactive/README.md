<h1 align="center" class="ps-main-header">⚡ Interactive PS5<br>Jailbreak & Exploit Wizard ⚡</h1>
<p align="center" class="ps-header-author">by ALONSOJR1980</p>

<div align="center">

[![PS5 Firmware](https://img.shields.io/badge/Interactive%20Wizard-Firmware%20Routes-success?style=for-the-badge&logo=playstation&logoColor=white)](#)
[![Guidance](https://img.shields.io/badge/Guide-Step--by--Step-blueviolet?style=for-the-badge&logo=playstation&logoColor=white)](#)

**Languages / Idiomas:**
[🇺🇸 English](README.md) | [🇧🇷 Versão em Português](i18n/pt/README.md) | [🇪🇸 Versión en Español](i18n/es/README.md)

</div>

Select your PS5 model and firmware range to get instructions for your console. Follow the steps shown below; you do not need to learn how the software works.

---

<!-- INTERACTIVE WIZARD COMPONENT -->
<div class="ps-wizard-container" id="psWizard">
<div class="ps-wizard-header">
<div class="ps-wizard-badge">⚡ INTERACTIVE FIRMWARE WIZARD</div>
<h2 class="ps-wizard-title">Step-by-Step PS5 Setup</h2>
<p class="ps-wizard-subtitle">Choose your console model and firmware range to see the matching steps.</p>
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
<label class="ps-wizard-label">2. CHOOSE YOUR FIRMWARE RANGE:</label>
<div class="ps-exploit-grid">
<button type="button" class="ps-exploit-btn active" data-fw="9.60 - 13.60" onclick="setWizardFw('9.60 - 13.60')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 9.60–13.60</span>
<span class="ps-exploit-badge ready">STEPS AVAILABLE</span>
</div>
<div class="ps-exploit-range">Firmware 9.60 – 13.60</div>
<div class="ps-exploit-sub">Follow the on-screen steps for this firmware range.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="14.00+" onclick="setWizardFw('14.00+')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 14.00 or higher</span>
<span class="ps-exploit-badge wip">NO STEPS</span>
</div>
<div class="ps-exploit-range">Firmware 14.00+</div>
<div class="ps-exploit-sub">This wizard has no route for this version. Keep the console offline.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="7.00 - 8.20" onclick="setWizardFw('7.00 - 8.20')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 7.00–8.20</span>
<span class="ps-exploit-badge wip">CHECK ROUTE</span>
</div>
<div class="ps-exploit-range">Firmware 7.00 – 8.20</div>
<div class="ps-exploit-sub">This wizard does not include complete steps for this range.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="6.00 - 6.50" onclick="setWizardFw('6.00 - 6.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 6.00–6.50</span>
<span class="ps-exploit-badge wip">NOT READY</span>
</div>
<div class="ps-exploit-range">Firmware 6.00 – 6.50</div>
<div class="ps-exploit-sub">Step-by-step instructions are not available for this range.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="5.00 - 5.50" onclick="setWizardFw('5.00 - 5.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 5.00–5.50</span>
<span class="ps-exploit-badge ready">STEPS AVAILABLE</span>
</div>
<div class="ps-exploit-range">Firmware 5.00 – 5.50</div>
<div class="ps-exploit-sub">Follow the on-screen steps for this firmware range.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="3.00 - 4.51" onclick="setWizardFw('3.00 - 4.51')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 3.00–4.51</span>
<span class="ps-exploit-badge ready">STEPS AVAILABLE</span>
</div>
<div class="ps-exploit-range">Firmware 3.00 – 4.51</div>
<div class="ps-exploit-sub">Follow the on-screen steps for this firmware range.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 1.00–2.50</span>
<span class="ps-exploit-badge wip">CHECK ROUTE</span>
</div>
<div class="ps-exploit-range">Firmware 1.00 – 2.50</div>
<div class="ps-exploit-sub">This wizard does not include complete steps for this range.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="8.21 - 9.59" onclick="setWizardFw('8.21 - 9.59')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Check compatibility</span>
<span class="ps-exploit-badge wip">NO STEPS</span>
</div>
<div class="ps-exploit-range">Firmware 8.21 – 9.59</div>
<div class="ps-exploit-sub">This wizard has no verified route for this range.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="unlisted" onclick="setWizardFw('unlisted')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">My firmware is not listed</span>
<span class="ps-exploit-badge wip">VERIFY FIRST</span>
</div>
<div class="ps-exploit-range">Other firmware version</div>
<div class="ps-exploit-sub">Do not choose a nearby range; verify compatibility first.</div>
</button>
</div>
<div class="ps-ip-wrap">
<label for="customIpInput" class="ps-ip-label">
<span class="ps-ip-title">Console IP Address (optional):</span>
<span class="ps-ip-desc">Used to fill in commands if you choose the computer or phone method.</span>
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
> - The detachable disc drive requires one-time online registration with Sony to pair with the motherboard.
> - **Never connect to PSN to pair the drive on an exploitable firmware (<= 13.60)**, as it will **force an irreversible update to the latest patched firmware**.
> - Games, digital dumps, emulators, homebrew, and internal M.2 SSD storage work 100% without the physical disc drive paired.

---

<p align="center">
  <b>🤖 Interactive Firmware Wizard for the PS5 Community</b><br>
  <i>Select your hardware and firmware to generate custom offline jailbreak instructions.</i>
</p>
