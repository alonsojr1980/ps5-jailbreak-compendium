# 🚀 PS5 Jailbreak: Direct How-To Guide
### *by ALONSOJR1980*

<div align="center">

[![PS5 Firmware](https://img.shields.io/badge/Supported%20FW-1.00%20--%2013.60-success?style=for-the-badge&logo=playstation&logoColor=white)](https://github.com/alonsojr1980/ps5-jailbreak-compendium)
[![Exploit](https://img.shields.io/badge/Primary%20Exploit-Relapse%20%7C%20UMTX-blueviolet?style=for-the-badge&logo=codeforces&logoColor=white)](jailbreak_tech_info.md)
[![Live Website](https://img.shields.io/badge/Live%20Website-GitHub%20Pages-00d2ff?style=for-the-badge&logo=githubpages&logoColor=white)](https://alonsojr1980.github.io/ps5-jailbreak-compendium/)
[![Payloads](https://img.shields.io/badge/Payloads-etaHEN%20%7C%20ps5--kstuff-ff69b4?style=for-the-badge&logo=coffeescript&logoColor=white)](jailbreak_tech_info.md#4-payload-engineering--system-frameworks)

**Navigation:**
[🔬 Technical Deep Dive (Tech Info)](jailbreak_tech_info.md) | [🇧🇷 Versão em Português](../pt/jailbreak_how_to.md) | [🌐 Main Portal](../../README.md)

</div>

A direct, step-by-step, actionable guide to jailbreaking your PlayStation 5 across different firmware brackets, configuring the anti-update firewall, and loading essential payloads.

---

## 📑 Table of Contents

1. [🔍 Step 0: Check Your Console Firmware](#-step-0-check-your-console-firmware)
2. [🛡️ Step 1: Pre-Jailbreak Hardening & Anti-Update Firewall](#️-step-1-pre-jailbreak-hardening--anti-update-firewall)
3. [⚠️ PS5 Slim & Pro Detachable Disc Drive Critical Warning](#️-ps5-slim--pro-detachable-disc-drive-critical-warning)
4. [🎮 Step 2: Jailbreak by Firmware Bracket](#-step-2-jailbreak-by-firmware-bracket)
   - [Method A: Modern Firmwares 7.00 – 13.60 (Relapse Exploit)](#method-a-firmwares-700--1360-relapse-exploit)
   - [Method B: Stable Firmwares 3.00 – 4.51 & 5.00 – 5.50 (UMTX / IPv6)](#method-b-firmwares-300--451--500--550-umtx--ipv6)
   - [Method C: Early Firmwares 1.00 – 2.50 (Byepervisor)](#method-c-early-firmwares-100--250-byepervisor)
5. [📦 Step 3: Injecting Payloads (etaHEN & ps5-kstuff)](#-step-3-injecting-payloads-etahen--ps5-kstuff)
   - [Option 1: Automatic USB Loading (Recommended)](#option-1-automatic-usb-loading-recommended)
   - [Option 2: Network Injection via Terminal (Netcat)](#option-2-network-injection-via-terminal-netcat)
6. [🕹️ Step 4: Installing Homebrew & Launching Game Backups](#️-step-4-installing-homebrew--launching-game-backups)
7. [🔧 Quick Troubleshooting & Panic Recovery](#-quick-troubleshooting--panic-recovery)

---

## 🔍 Step 0: Check Your Console Firmware

Before doing anything, find out your exact PlayStation 5 system software version:

1. Turn on your PS5 and open **Settings ➔ System ➔ System Software ➔ Console Information**.
2. Look at **System Software**:
   - Format: `XX.XX-XX.XX.XX.XX-XX.XX` (The first 4 digits indicate your firmware, e.g. `07.61` or `04.50` or `13.60`).

### Compatibility Quick Check

| Firmware | Can I Jailbreak? | Recommended Exploit Method |
| :---: | :---: | :--- |
| **1.00 – 2.50** | ✅ **YES** (Hypervisor Root) | [Byepervisor / IPv6 UAF](#method-c-early-firmwares-100--250-byepervisor) |
| **3.00 – 4.51** | ✅ **YES** (Peak Stability) | [IPv6 Socket UAF / UMTX](#method-b-firmwares-300--451--500--550-umtx--ipv6) |
| **5.00 – 5.50** | ✅ **YES** (Highly Stable) | [UMTX Exploit](#method-b-firmwares-300--451--500--550-umtx--ipv6) |
| **6.00 – 6.50** | ⚠️ **YES** (Active Porting) | [UMTX2 / Mast1c0re](#method-b-firmwares-300--451--500--550-umtx--ipv6) |
| **7.00 – 13.60** | ✅ **YES** (Modern Era) | [Relapse Exploit (aio_multi_wait)](#method-a-firmwares-700--1360-relapse-exploit) |
| **14.00+** | ❌ **NO** (Patched) | Keep console **strictly offline** and wait. **Do not update!** |

---

## 🛡️ Step 1: Pre-Jailbreak Hardening & Anti-Update Firewall

Accidental background updates permanently destroy jailbreak capability. Apply these settings immediately before connecting to any network:

### 1. In-Console Settings Checklist
- [x] **Settings ➔ System ➔ System Software ➔ System Software Updates and Settings**:
  - Turn **OFF** *Download Update Files Automatically*.
  - Turn **OFF** *Install Update Files Automatically*.
- [x] **Settings ➔ System ➔ Power Saving ➔ Features Available in Rest Mode**:
  - Turn **OFF** *Stay Connected to the Internet*.
- [x] **Settings ➔ Saved Data and Game/App Settings ➔ Automatic Updates**:
  - Turn **OFF** *Auto-Download*.
  - Turn **OFF** *Auto-Install in Rest Mode*.

### 2. Router / Pi-hole / AdGuard Domain Blocklist
Add these Sony telemetry and update domains to your firewall blacklist:

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

---

## ⚠️ PS5 Slim & Pro Detachable Disc Drive Critical Warning

> [!CAUTION]
> If your console is a **PS5 Slim (CFI-2000)** or **PS5 Pro (CFI-7000)** with a detachable disc drive:
> - The drive requires a one-time cryptographic **Handshake** with Sony's servers to bind with the motherboard.
> - **The Trap**: If your console is on an exploitable firmware (<= 13.60), connecting to PSN to pair the drive will **force an irreversible system update to the latest firmware**.
> - **Rule**: If your drive is not already paired, **do not update** to pair it. Digital game backups, homebrew, emulators, and M.2 SSD storage operate 100% without the physical disc drive paired.

---

## 🎮 Step 2: Jailbreak by Firmware Bracket

### Method A: Firmwares 7.00 – 13.60 (Relapse Exploit)

This method covers all PS5 models (Fat, Slim, and Pro) running firmwares 7.00 through 13.60.

#### 1. Setup Custom DNS Connection
1. Navigate to **Settings ➔ Network ➔ Settings ➔ Set Up Internet Connection**.
2. Select your Wi-Fi or LAN connection, press **Options (☰)** ➔ **Advanced Settings**.
3. Set the following:
   - **IP Address Settings**: `Automatic`
   - **DHCP Host Name**: `Do Not Specify`
   - **DNS Settings**: `Manual`
     - **Primary DNS**: `45.56.67.85`
     - **Secondary DNS**: `0.0.0.0` (or `62.210.38.117`)
   - **Proxy Server**: `Do Not Use`
   - **MTU Settings**: `Automatic`
4. Save and run the connection test. *Internet Connection: Successful*; *PlayStation Network: Failed* (Normal & safe).

#### 2. Trigger the Exploit
1. Open **Settings ➔ System ➔ User's Guide, Health & Safety, and Other Information ➔ User's Guide**.
2. The browser redirects to the Relapse Exploit Host.
3. The WebKit exploit runs automatically (spraying JavaScriptCore heap memory).
4. The kernel exploit triggers via the `aio_multi_wait` race condition.
5. Wait for the confirmation:
   `[+] Kernel RW Obtained! elfldr listening on port 9021...`

> [!TIP]
> If your console freezes or abruptly powers down with a black screen, a **Kernel Panic** occurred. Wait 30 seconds, power on via the console power button, allow the storage rebuild to finish, and try again.

---

### Method B: Firmwares 3.00 – 4.51 & 5.00 – 5.50 (UMTX / IPv6)

These firmwares boast exceptional stability (near 100% success rate).

1. Set your PS5 **Primary DNS** to `62.210.38.117` (EchoStretch) or `165.227.83.145` (Al-Azif).
2. Open **Settings ➔ System ➔ User's Guide**.
3. Choose the appropriate exploit:
   - For **3.00 – 4.51**: Select **IPv6 UAF** or **UMTX**.
   - For **5.00 – 5.50**: Select **UMTX Exploit**.
4. The exploit completes in seconds, launching `elfldr` on Port 9021.

---

### Method C: Early Firmwares 1.00 – 2.50 (Byepervisor)

The most privileged firmware bracket with complete Hypervisor control (Ring -1).

1. Access the exploit host via User's Guide or BD-JB Blu-ray disc.
2. Trigger the kernel exploit and load the **Byepervisor** payload.
3. Byepervisor defeats the PS5 Hypervisor, granting arbitrary hypervisor read/write, code signing bypass, and RAM decryption.

---

## 📦 Step 3: Injecting Payloads (etaHEN & ps5-kstuff)

Once `elfldr` is listening on **Port 9021**, inject the essential homebrew payloads:

### Option 1: Automatic USB Loading (Recommended)

1. Format a USB drive as **exFAT** (MBR partition).
2. Create a folder named `payloads` on the root of the USB drive:
   ```text
   USB Drive (exFAT):
   └── payloads/
       ├── etaHEN.bin
       └── ps5-kstuff.bin
   ```
3. Plug the USB drive into a rear USB 3.0 port on your PS5.
4. When you run the exploit, the loader automatically detects and executes payloads from the USB drive!

---

### Option 2: Network Injection via Terminal (Netcat)

If sending payloads from your computer over the local network:

#### On Linux / macOS / WSL:
```bash
# Inject etaHEN (All-In-One Homebrew Enabler)
nc -w 3 <PS5_IP_ADDRESS> 9021 < etaHEN.bin

# Inject ps5-kstuff (if not bundled with etaHEN)
nc -w 3 <PS5_IP_ADDRESS> 9021 < ps5-kstuff.bin
```

#### On Windows (PowerShell):
```powershell
$ps5_ip = "192.168.1.150"
$bytes = [System.IO.File]::ReadAllBytes("etaHEN.bin")
$client = New-Object System.Net.Sockets.TcpClient($ps5_ip, 9021)
$stream = $client.GetStream()
$stream.Write($bytes, 0, $bytes.Length)
$stream.Close(); $client.Close()
Write-Host "[SUCCESS] etaHEN sent to PS5!"
```

---

## 🕹️ Step 4: Installing Homebrew & Launching Game Backups

Once **etaHEN** is injected:

1. **Verify etaHEN Toolbox**:
   - Open **Settings ➔ System**.
   - You will see the new **etaHEN Toolbox** menu entry.
2. **Access FTP Server**:
   - etaHEN automatically launches an FTP server on **Port 1337**.
   - Connect via FileZilla / WinSCP using your PS5 IP and port `1337` (Anonymous login).
3. **Launch Itemzflow (Game Manager)**:
   - Install `Itemzflow.pkg` via the Package Installer in Settings or run it directly.
   - Dump your physical discs or digital purchases to an external USB hard drive or internal M.2 NVMe SSD.
   - Launch games directly from USB storage without copying to internal drive.
4. **Manage Saves with Apollo Save Tool**:
   - Export, import, and resign game saves across different PSN accounts offline.

---

## 🔧 Quick Troubleshooting & Panic Recovery

| Problem | Root Cause | Solution |
| :--- | :--- | :--- |
| **Instant black screen / shutdown** | Kernel Panic during exploit timing race | Wait 30 seconds. Press physical power button. Let storage repair complete; re-launch exploit. |
| **"Not enough free system memory"** | WebKit heap grooming overflow | Press `OK`, refresh the page or clear browser cookies in settings. |
| **User's Guide loads official Sony page** | DNS desync or router ignoring custom DNS | Re-check Network Settings; ensure Primary DNS is set to `45.56.67.85` and Secondary is `0.0.0.0`. |
| **Port 9021 Connection Refused** | Stage 2 failed or `elfldr` crashed | Re-open User's Guide until "Listening on 9021" notification appears. |
| **Games fail to launch with CE-xxxx error** | `ps5-kstuff` payload not loaded | Ensure `kstuff` or `etaHEN` is loaded before opening games. |

---

<p align="center">
  <b>Need deep technical details, memory primitives, syscall internals, or network ports?</b><br>
  👉 Read the companion guide: <b><a href="jailbreak_tech_info.md">PS5 Jailbreak: Technical Deep Dive (Tech Info)</a></b>
</p>
