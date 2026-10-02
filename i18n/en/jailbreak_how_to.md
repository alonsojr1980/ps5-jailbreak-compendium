# 🚀 PS5 Jailbreak: Direct How-To Guide
### *by ALONSOJR1980*

<div align="center">

[![PS5 Firmware](https://img.shields.io/badge/Supported%20FW-1.00%20--%2013.60-success?style=for-the-badge&logo=playstation&logoColor=white)](https://github.com/alonsojr1980/ps5-jailbreak-compendium)
[![Exploit](https://img.shields.io/badge/Primary%20Exploit-Relapse%20%7C%20UMTX-blueviolet?style=for-the-badge&logo=codeforces&logoColor=white)](jailbreak_tech_info.md)
[![Live Website](https://img.shields.io/badge/Live%20Website-GitHub%20Pages-00d2ff?style=for-the-badge&logo=githubpages&logoColor=white)](https://alonsojr1980.github.io/ps5-jailbreak-compendium/)
[![Payloads](https://img.shields.io/badge/Payloads-etaHEN%20%7C%20ps5--kstuff-ff69b4?style=for-the-badge&logo=coffeescript&logoColor=white)](jailbreak_tech_info.md#4-payload-engineering--system-frameworks)

**Navigation:**
[🔬 Technical Deep Dive (Tech Info)](jailbreak_tech_info.md) | [🇧🇷 Versão em Português](../pt/jailbreak_how_to.md) | [🇪🇸 Versión en Español](../es/jailbreak_how_to.md) | [🌐 Main Portal](../../README.md)

</div>

An ultra-direct, gamified tactical guide to jailbreaking your PlayStation 5 across firmwares 1.00 through 13.60, locking down anti-update defenses, and executing payloads.

---

<!-- GAMIFIED QUEST HUD -->
<div class="ps-quest-hud" id="psQuestHud">
  <div class="ps-hud-header">
    <div class="ps-hud-title-wrap">
      <div class="ps-hud-rank-icon" id="psRankIcon">🎮</div>
      <div>
        <div class="ps-hud-title">Campaign: PS5 Jailbreak Protocol</div>
        <div class="ps-hud-subtitle">Complete quests to liberate firmware and claim PlayStation Trophies</div>
      </div>
    </div>
    <div class="ps-hud-stats">
      <div class="ps-hud-stat-pill">
        <span>🏆 TROPHIES:</span>
        <span id="psTrophiesCount">0 / 5</span>
      </div>
      <div class="ps-hud-stat-pill">
        <span>⚡ XP:</span>
        <span id="psProgressPct">0%</span>
      </div>
    </div>
  </div>

  <div class="ps-progress-bar-container">
    <div class="ps-progress-bar-fill" id="psProgressFill"></div>
  </div>

  <div class="ps-hud-footer">
    <div><span>△</span> Click tile to inspect Intel &bull; <span>◯</span> Claim Trophy when completed &bull; <span>✕</span> Execute</div>
    <div class="ps-hud-controls">
      <button class="ps-btn-hud" onclick="toggleAllSteps(true)">📂 Expand All</button>
      <button class="ps-btn-hud" onclick="toggleAllSteps(false)">📁 Collapse All</button>
      <button class="ps-btn-hud" onclick="resetAllQuests()">🔄 Reset Campaign</button>
    </div>
  </div>
</div>

<!-- QUEST 0 -->
<details class="step-tile" data-quest="quest-step-0" open>
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">QUEST 0</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🎯 Target Scouting: Firmware Identification</span>
      <span class="step-tile-desc">Identify system software version (1.00 – 13.60) & confirm vulnerability tier</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">RECON</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 MISSION OBJECTIVE:</strong> Locate your PS5 system software version and confirm your jailbreak exploit tier.
</div>

### 🎒 Required Gear
- PS5 Console & DualSense Controller
- TV / Display output

### ⚡ Tactical Execution
1. Power on your PS5 and open **Settings ➔ System ➔ System Software ➔ Console Information**.
2. Read the **System Software** line:
   - Format: `XX.XX-XX.XX.XX.XX-XX.XX` (First 4 digits indicate firmware: e.g. `07.61`, `04.50`, `13.60`).

### 📊 Firmware Compatibility Matrix

| Firmware Bracket | Exploit Status | Tactical Exploit Vector |
| :---: | :---: | :--- |
| **1.00 – 2.50** | ✅ **Hypervisor Root** | [Byepervisor / IPv6 UAF](#method-c-early-firmwares-100--250-byepervisor) |
| **3.00 – 4.51** | ✅ **Peak Stability** | [IPv6 Socket UAF / UMTX](#method-b-firmwares-300--451--500--550-umtx--ipv6) |
| **5.00 – 5.50** | ✅ **Highly Stable** | [UMTX Exploit](#method-b-firmwares-300--451--500--550-umtx--ipv6) |
| **6.00 – 6.50** | ⚠️ **Active Porting** | [UMTX2 / Mast1c0re](#method-b-firmwares-300--451--500--550-umtx--ipv6) |
| **7.00 – 13.60** | ✅ **Modern Era** | [Relapse Exploit (aio_multi_wait)](#method-a-firmwares-700--1360-relapse-exploit) |
| **14.00+** | ❌ **Patched** | Keep console **strictly offline**. **Do not update!** |

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 REWARD:</span> 🥉 Bronze Trophy &bull; <em>"Recon Specialist"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-0" data-todo-text="Mark Accomplished" data-done-text="Mission Accomplished" onclick="toggleQuest('quest-step-0', 'Recon Specialist', 'Bronze Trophy', '🎯')">
    <span>◯</span> Mark Accomplished
  </button>
</div>

</details>

<!-- QUEST 1 -->
<details class="step-tile" data-quest="quest-step-1">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">QUEST 1</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🛡️ Defense Protocol: Anti-Update Armor</span>
      <span class="step-tile-desc">Lock down Sony telemetry and deploy network firewalls before connecting</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">MANDATORY</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 MISSION OBJECTIVE:</strong> Immunize your console against accidental background system software downloads.
</div>

### 🎒 Required Gear
- In-Console System Settings
- Home Router / Pi-hole / AdGuard (Optional extra defense)

### ⚡ Tactical Execution: In-Console Hardening
- [x] **Settings ➔ System ➔ System Software ➔ System Software Updates and Settings**:
  - Turn **OFF** *Download Update Files Automatically*.
  - Turn **OFF** *Install Update Files Automatically*.
- [x] **Settings ➔ System ➔ Power Saving ➔ Features Available in Rest Mode**:
  - Turn **OFF** *Stay Connected to the Internet*.
- [x] **Settings ➔ Saved Data and Game/App Settings ➔ Automatic Updates**:
  - Turn **OFF** *Auto-Download*.
  - Turn **OFF** *Auto-Install in Rest Mode*.

### 🌐 Router / Pi-hole Blacklist Domains
Blacklist these Sony endpoints on your home network:

```text
fus01.ps5.update.playstation.net
fuk01.ps5.update.playstation.net
feu01.ps5.update.playstation.net
fjp01.ps5.update.playstation.net
fkr01.ps5.update.playstation.net
fcn01.ps5.update.playstation.net
ps5.update.playstation.net
telemetry.api.playstation.com
telemetry-ingest.api.playstation.com
```

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 REWARD:</span> 🥉 Bronze Trophy &bull; <em>"Network Sentinel"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-1" data-todo-text="Mark Accomplished" data-done-text="Mission Accomplished" onclick="toggleQuest('quest-step-1', 'Network Sentinel', 'Bronze Trophy', '🛡️')">
    <span>◯</span> Mark Accomplished
  </button>
</div>

</details>

<!-- BOSS HAZARD WARNING -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number warning">BOSS HAZARD</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚠️ Slim & Pro Detachable Disc Drive Pairing Trap</span>
      <span class="step-tile-desc">DO NOT connect to PSN to register a detachable drive on exploitable firmware</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag warning">PERMADEATH TRAP</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>⚠️ TACTICAL INTEL:</strong> The detachable disc drive requires a one-time cryptographic <strong>Handshake</strong> with Sony's servers to bind with the console motherboard.
</div>

> [!CAUTION]
> - **The Trap**: If your console is on an exploitable firmware (<= 13.60), connecting to PSN to pair the drive will **force an irreversible update to the latest patched firmware**, permanently eliminating jailbreak capability.
> - **Operational Rule**: If your drive is not already paired, **do not update** to pair it. Digital game dumps, homebrew, emulators, and internal M.2 SSD storage work 100% without the disc drive.

</details>

<!-- QUEST 2 -->
<details class="step-tile" data-quest="quest-step-2">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">QUEST 2</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚔️ Infiltration: Exploit Trigger & Kernel RW</span>
      <span class="step-tile-desc">Trigger WebKit memory spray & aio_multi_wait race to open Port 9021</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">KERNEL BREACH</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 MISSION OBJECTIVE:</strong> Achieve arbitrary Kernel Read/Write and start the <code>elfldr</code> payload listener on <strong>Port 9021</strong>.
</div>

### 🎒 Required Gear
- Exploit DNS: `45.56.67.85` (Relapse) or `62.210.38.117` (UMTX)
- PS5 User's Guide Browser

### ⚡ Tactical Execution: Select Your Firmware Vector

#### Method A: Modern Firmwares 7.00 – 13.60 (Relapse Exploit)
1. Navigate to **Settings ➔ Network ➔ Settings ➔ Set Up Internet Connection**.
2. Select your connection, press **Options (☰)** ➔ **Advanced Settings**:
   - **DNS Settings**: `Manual`
   - **Primary DNS**: `45.56.67.85`
   - **Secondary DNS**: `0.0.0.0` (or `62.210.38.117`)
3. Save and run the connection test (*Internet: OK*; *PSN: Failed* — this is correct).
4. Open **Settings ➔ System ➔ User's Guide, Health & Safety ➔ User's Guide**.
5. The Relapse host executes WebKit heap spray followed by the `aio_multi_wait` kernel exploit.
6. Await confirmation prompt:
   `[+] Kernel RW Obtained! elfldr listening on port 9021...`

> [!TIP]
> If your console abruptly powers off, a **Kernel Panic** occurred. Wait 30 seconds, press the physical power button, allow the storage rebuild to finish, and re-run the exploit.

---

#### Method B: Stable Firmwares 3.00 – 4.51 & 5.00 – 5.50 (UMTX / IPv6)
1. Set **Primary DNS** to `62.210.38.117` or `165.227.83.145`.
2. Open **Settings ➔ System ➔ User's Guide**.
3. Select **IPv6 UAF** (for 3.00–4.51) or **UMTX Exploit** (for 5.00–5.50).
4. The exploit succeeds in seconds and launches `elfldr` on Port 9021.

---

#### Method C: Early Firmwares 1.00 – 2.50 (Byepervisor)
1. Load exploit via User's Guide or BD-JB Blu-ray disc.
2. Inject **Byepervisor** to take full control of the Hypervisor (Ring -1).

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 REWARD:</span> 🥈 Silver Trophy &bull; <em>"Perimeter Breached"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-2" data-todo-text="Mark Accomplished" data-done-text="Mission Accomplished" onclick="toggleQuest('quest-step-2', 'Perimeter Breached', 'Silver Trophy', '⚔️')">
    <span>◯</span> Mark Accomplished
  </button>
</div>

</details>

<!-- QUEST 3 -->
<details class="step-tile" data-quest="quest-step-3">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">QUEST 3</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚡ Power Surge: Payload Delivery & Activation</span>
      <span class="step-tile-desc">Inject etaHEN and ps5-kstuff via USB autoloader or Netcat port 9021</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">PAYLOAD INJECTION</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 MISSION OBJECTIVE:</strong> Deliver and execute the essential homebrew payloads (<code>etaHEN</code> &amp; <code>ps5-kstuff</code>) to patch system restrictions.
</div>

### 🎒 Required Gear
- USB Flash Drive formatted as **exFAT** (Option 1) OR Terminal Netcat / PowerShell (Option 2)
- Payload Binaries: `etaHEN.bin`, `ps5-kstuff.bin`

### ⚡ Tactical Execution: Injection Options

#### Option 1: Automatic USB Loading (Recommended)
1. Format a USB drive as **exFAT** with MBR partition scheme.
2. Create a folder named `payloads` on the root of the USB drive:
   ```text
   USB Drive (exFAT):
   └── payloads/
       ├── etaHEN.bin
       └── ps5-kstuff.bin
   ```
3. Insert the drive into one of the **rear USB 3.0 ports** on your PS5.
4. When triggering the exploit, the loader automatically detects and executes payloads from USB!

---

#### Option 2: Network Injection via Terminal (Netcat)
Send the payloads from your PC over the local network to PS5 IP on **Port 9021**:

```bash
# On Linux / macOS / WSL:
nc -w 3 <PS5_IP_ADDRESS> 9021 < etaHEN.bin
nc -w 3 <PS5_IP_ADDRESS> 9021 < ps5-kstuff.bin
```

```powershell
# On Windows (PowerShell):
$ps5_ip = "192.168.1.150"
$bytes = [System.IO.File]::ReadAllBytes("etaHEN.bin")
$client = New-Object System.Net.Sockets.TcpClient($ps5_ip, 9021)
$stream = $client.GetStream()
$stream.Write($bytes, 0, $bytes.Length)
$stream.Close(); $client.Close()
Write-Host "[SUCCESS] etaHEN deployed to PS5!"
```

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 REWARD:</span> 🥇 Gold Trophy &bull; <em>"Kernel Overlord"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-3" data-todo-text="Mark Accomplished" data-done-text="Mission Accomplished" onclick="toggleQuest('quest-step-3', 'Kernel Overlord', 'Gold Trophy', '⚡')">
    <span>◯</span> Mark Accomplished
  </button>
</div>

</details>

<!-- QUEST 4 -->
<details class="step-tile" data-quest="quest-step-4">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">QUEST 4</span>
    <span class="step-tile-text">
      <span class="step-tile-title">👑 Sovereign Liberation: Homebrew & Backups</span>
      <span class="step-tile-desc">Deploy etaHEN Toolbox, FTP port 1337, Itemzflow, and Apollo Save Tool</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">ROOT FREEDOM</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 MISSION OBJECTIVE:</strong> Establish the full homebrew and backup ecosystem on your liberated PlayStation 5.
</div>

### 🎒 Required Gear
- FTP Client (FileZilla / WinSCP)
- Homebrew Packages: `Itemzflow.pkg`, `Apollo.pkg`

### ⚡ Tactical Execution
1. **Verify etaHEN Toolbox**:
   - Open **Settings ➔ System**.
   - Verify the presence of the new **etaHEN Toolbox** system menu.
2. **Access High-Speed FTP Server**:
   - etaHEN automatically binds an FTP daemon to **Port 1337**.
   - Connect via FileZilla / WinSCP with anonymous credentials.
3. **Launch Itemzflow Game Manager**:
   - Install `Itemzflow.pkg` and launch it from the home screen.
   - Dump physical discs and digital purchases to an external USB hard drive or internal M.2 SSD.
   - Launch game backups directly from USB storage.
4. **Manage Saves with Apollo Save Tool**:
   - Export, import, and resign game saves across PSN accounts completely offline.

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 REWARD:</span> 🏆 Platinum Trophy &bull; <em>"Sovereign Root Master"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-4" data-todo-text="Mark Accomplished" data-done-text="Mission Accomplished" onclick="toggleQuest('quest-step-4', 'Sovereign Root Master', 'Platinum Trophy', '👑')">
    <span>◯</span> Mark Accomplished
  </button>
</div>

</details>

<!-- RESPAWN / RECOVERY -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number warning">RESPAWN</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🚑 Diagnostics & Panic Recovery Point</span>
      <span class="step-tile-desc">Recover from Kernel Panics, memory overflows, DNS desync, and CE-xxxx crashes</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag warning">CHECKPOINT</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🚑 RESPAWN INTEL:</strong> Exploit timing races may trigger harmless Kernel Panics. Consult this field diagnostics chart to recover quickly.
</div>

| Anomaly / Symptom | Root Cause | Field Solution |
| :--- | :--- | :--- |
| **Instant black screen / shutdown** | Kernel Panic during timing race | Wait 30s. Press physical console power button. Allow storage check to complete; re-trigger exploit. |
| **"Not enough free system memory"** | WebKit heap grooming overflow | Press `OK`, refresh page or clear browser cookies in settings. |
| **User's Guide loads official Sony page** | DNS desync or router ignoring custom DNS | Re-check Network Settings; ensure Primary DNS is `45.56.67.85` and Secondary is `0.0.0.0`. |
| **Port 9021 Connection Refused** | Stage 2 failed or `elfldr` crashed | Re-open User's Guide until "Listening on 9021" notification appears. |
| **Games fail to launch with CE-xxxx error** | `ps5-kstuff` payload not loaded | Ensure `kstuff` or `etaHEN` is loaded before opening games. |

</details>

---

<p align="center">
  <b>Need deep technical details, memory primitives, syscall internals, or network ports?</b><br>
  👉 Read the companion guide: <b><a href="jailbreak_tech_info.md">PS5 Jailbreak: Technical Deep Dive (Tech Info)</a></b>
</p>
