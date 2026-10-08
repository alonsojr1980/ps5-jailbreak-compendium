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
<!-- Step 1: Model Selection -->
<div class="ps-wizard-step" id="wizardStep1">
<div class="ps-wizard-bookmark" aria-hidden="true">
<span class="ps-bm-num">01</span>
<span class="ps-bm-text">MODEL</span>
</div>
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
</div>
<!-- Step 2: Firmware Selection -->
<div class="ps-wizard-step" id="wizardStep2">
<div class="ps-wizard-bookmark" aria-hidden="true">
<span class="ps-bm-num">02</span>
<span class="ps-bm-text">FIRMWARE</span>
</div>
<div class="ps-wizard-field">
<label class="ps-wizard-label">2. CHOOSE YOUR FIRMWARE RANGE:</label>
<div class="ps-exploit-grid">
<button type="button" class="ps-exploit-btn active" data-fw="7.00 - 13.60" onclick="setWizardFw('7.00 - 13.60')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 7.00–13.60</span>
<span class="ps-exploit-badge ready">STEPS AVAILABLE</span>
</div>
<div class="ps-exploit-sub">WebKit + aio_multi_wait kernel exploit (Relapse). Direct browser setup.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="3.00 - 6.50" onclick="setWizardFw('3.00 - 6.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 3.00–6.50</span>
<span class="ps-exploit-badge ready">STEPS AVAILABLE</span>
</div>
<div class="ps-exploit-sub">UMTX & IPv6 Socket UAF kernel exploits. Requires USB drive for payloads.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 1.00–2.50</span>
<span class="ps-exploit-badge ready">STEPS AVAILABLE</span>
</div>
<div class="ps-exploit-sub">Byepervisor Hypervisor (Ring -1) root compromise and kernel read/write.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="14.00+" onclick="setWizardFw('14.00+')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 14.00 or higher</span>
<span class="ps-exploit-badge patched">NOT EXPLOITABLE</span>
</div>
<div class="ps-exploit-sub">Patched by Sony. No public exploit exists. Keep console strictly offline.</div>
</button>
</div>
<div class="ps-ip-wrap">
<label for="customIpInput" class="ps-ip-label">
<span class="ps-ip-title">Console IP Address (optional):</span>
<span class="ps-ip-desc">Used to fill in commands if you choose the computer or phone method.</span>
</label>
<input type="text" id="customIpInput" class="ps-input" inputmode="decimal" autocomplete="off" aria-describedby="customIpError" value="192.168.1.150" placeholder="192.168.1.xxx" oninput="onCustomIpInput(this.value)">
<span id="customIpError" class="ps-ip-error" role="alert">Enter a valid IP address, for example 192.168.1.150.</span>
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
> - The detachable disc drive requires one-time online registration with Sony to pair with the motherboard.
> - **Never connect to PSN to pair the drive on an exploitable firmware (<= 13.60)**, as it will **force an irreversible update to the latest patched firmware**.
> - Games, digital dumps, emulators, homebrew, and internal M.2 SSD storage work 100% without the physical disc drive paired.

---

<p align="center">
  <b>🤖 Interactive Firmware Wizard for the PS5 Community</b><br>
  <i>Select your hardware and firmware to generate custom offline jailbreak instructions.</i>
</p>
