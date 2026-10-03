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
<label class="ps-wizard-label">2. SELECT EXPLOIT TYPE & FIRMWARE RANGE:</label>
<div class="ps-exploit-grid">
<button type="button" class="ps-exploit-btn active" data-fw="9.60 - 13.60" onclick="setWizardFw('9.60 - 13.60')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Relapse Exploit</span>
<span class="ps-exploit-badge ready">WebKit</span>
</div>
<div class="ps-exploit-range">Firmware 9.60 – 13.60</div>
<div class="ps-exploit-sub">WebKit (JSC) + aio_multi_wait Kernel Race Condition</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="7.00 - 8.20" onclick="setWizardFw('7.00 - 8.20')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">BD-JB / Mast1c0re</span>
<span class="ps-exploit-badge ready">Disc / PS2</span>
</div>
<div class="ps-exploit-range">Firmware 7.00 – 8.20</div>
<div class="ps-exploit-sub">BD-J Blu-ray Disc / PS2 Savegame + aio_multi_wait</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="6.00 - 6.50" onclick="setWizardFw('6.00 - 6.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">UMTX2 / Mast1c0re</span>
<span class="ps-exploit-badge wip">WIP</span>
</div>
<div class="ps-exploit-range">Firmware 6.00 – 6.50</div>
<div class="ps-exploit-sub">UMTX2 Primitives & PS2 Savegame (Porting Active)</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="5.00 - 5.50" onclick="setWizardFw('5.00 - 5.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">UMTX Exploit</span>
<span class="ps-exploit-badge ready">Kernel UAF</span>
</div>
<div class="ps-exploit-range">Firmware 5.00 – 5.50</div>
<div class="ps-exploit-sub">FreeBSD libthr Mutex Primitives (CVE-2024-43102)</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="3.00 - 4.51" onclick="setWizardFw('3.00 - 4.51')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">IPv6 Socket UAF</span>
<span class="ps-exploit-badge ready">Golden Era</span>
</div>
<div class="ps-exploit-range">Firmware 3.00 – 4.51</div>
<div class="ps-exploit-sub">FreeBSD netinet6 Socket UAF / UMTX</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Byepervisor</span>
<span class="ps-exploit-badge special">Ring -1 Root</span>
</div>
<div class="ps-exploit-range">Firmware 1.00 – 2.50</div>
<div class="ps-exploit-sub">Full Hypervisor Compromise (The Holy Grail)</div>
</button>
</div>
<div class="ps-ip-wrap">
<label for="customIpInput" class="ps-ip-label">
<span class="ps-ip-title">Console IP Address (optional):</span>
<span class="ps-ip-desc">Tailors netcat commands in the "WITH PC/PHONE" tab below to your console.</span>
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
