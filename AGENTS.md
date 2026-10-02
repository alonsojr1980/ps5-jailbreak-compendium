# 🤖 Guidelines for AI Agents: Maintaining Multi-Language Synchronization

Welcome, AI Agent! This document outlines strict operational rules, architectural standards, and synchronization workflows for maintaining and updating the **PS5 Jailbreak Compendium** repository.

---

## 🏛️ Repository Architecture

This repository uses an internationalized documentation structure:

```text
├── assets/
│   └── banner.png                # Master header banner graphic
├── i18n/
│   ├── en/
│   │   └── README.md             # Complete English Documentation
│   └── pt/
│       └── README.md             # Complete Portuguese Documentation (Português)
├── banner.png                    # Root fallback banner
├── README.md                     # Landing page with header banner & language links ONLY
├── upload.bat                    # Windows Git push automation helper (ignored in git)
├── .gitignore                    # Local ignore rules
├── AGENTS.md                     # Universal AI Agent maintenance guidelines (this file)
└── GEMINI.md                     # Specific instructions for Gemini & Antigravity agents
```

---

## 🚨 Core Rules for Agents

### 1. Mandatory Multi-Language Synchronization
- Whenever you make changes, updates, additions, or corrections to any documentation, you **MUST synchronize all active languages** (`i18n/en/README.md` and `i18n/pt/README.md`).
- **Never** leave one language updated while another remains outdated.
- If new technical developments occur (e.g., a new firmware jailbreak, payload release, DNS address change, or vulnerability patch), update both English and Portuguese files in the same turn or task.

### 2. Preserve the Root `README.md` Contract
- The root `README.md` is **strictly a portal / landing page**.
- It must contain **only**:
  1. The big header banner image (`assets/banner.png`) labeled `"PS5 JAILBREAK COMPENDIUM"`.
  2. Repository status and license badges.
  3. The language selector table with links to the translated documentation in `/i18n/[language]/README.md`.
  4. The AI curation disclaimer footer.
- **Do not** insert full documentation guides, exploits, or payload tutorials directly into the root `README.md`.

### 3. Structural & Section Parity
All language files must strictly maintain the same **11-section relevance hierarchy**:

1. **📊 1. Firmwares with Available Jailbreaks** (Matrix, Tiers, Relapse Exploit deep-dive, Hardware model notes)
2. **🚀 2. How to Jailbreak: Chain of Procedures & Preparations** (Mermaid flowchart, anti-update firewall, Slim/Pro detachable drive advisory, DNS setup, exploit trigger, payload injection)
3. **🧰 3. Curated Exploits & Entry Points** (Relapse, UMTX, IPv6, BD-JB, Mast1c0re, Byepervisor)
4. **⚙️ 4. Essential Payloads & System Frameworks** (Architecture diagram, etaHEN, kstuff, elfldr, libhijacker, shsrv, ftps5, Master Ports Directory)
5. **📦 5. Payload Injection & Automation Methods** (USB auto-loader layout, netcat terminal commands, Python sender script)
6. **🕹️ 6. Homebrew Apps, Emulators & Game Managers** (Itemzflow, Apollo, PS5SX2, Chiaki-ng, RetroArch)
7. **🌐 7. Exploit Hosts, DNS Servers & Offline Tools** (DNS table, web hosts, local Python server, ESP32)
8. **🔧 8. Troubleshooting & Panic Recovery** (Symptom / Cause / Solution table)
9. **📚 9. Technical Terms & Scene Glossary** (Untranslatable standards table & scene definitions)
10. **🏛️ 10. Background: Exploitation Timeline & Security Architecture**
11. **⚖️ 11. Disclaimer & AI Curation Notice**

---

## 🛡️ Technical Terms Policy: Untranslatable Industry Vocabulary

Certain technical terms in computer security, console hacking, and reverse engineering are globally standardized and **must NEVER be translated** into regional dialects under any circumstances. Literal translations obscure technical meaning and break alignment with developer tools.

### ❌ Prohibited Literal Translations (Never Translate These):
- **`Handshake`**: **NEVER** translate as `"aperto de mão"` (use `Handshake` or `Handshake Criptográfico`).
- **`Jailbreak`**: **NEVER** translate as `"fuga da prisão"` or regional slang.
- **`Payload`**: **NEVER** translate as `"carga útil"`.
- **`Kernel Panic`**: **NEVER** translate as `"pânico no kernel"`.
- **`Heap Spray`**: **NEVER** translate as `"spray de heap"`.
- **`Use-After-Free (UAF)`**: Preserve abbreviation and concept verbatim.
- **`Sandbox` / `Sandbox Escape`**: **NEVER** translate as `"caixa de areia"`.
- **`Rest Mode`**: Preserve as `Rest Mode` (or reference alongside `Modo de Repouso`).
- **`Dump` / `Dumping`**: **NEVER** translate as `"despejo"`.
- **`Hook` / `Hooking`**: Preserve verbatim.

### 🔒 Master Untranslatable Terms Directory

| Domain | Technical Term (Preserve Verbatim) | Context & Explanatory Requirement |
| :--- | :--- | :--- |
| **Protocols & Crypto** | `Handshake`, `Cryptographic Handshake` | Mutual authentication between console & servers (e.g. Slim/Pro drive pairing). |
| **Exploitation** | `Jailbreak`, `Exploit`, `Exploit Chain`, `PoC` | Privilege escalation and vulnerability exploitation taxonomy. |
| **Memory Safety** | `Use-After-Free (UAF)`, `Heap Spray`, `Heap Grooming`, `Race Condition`, `Infoleak` | Standard vulnerability primitives and CWE definitions. |
| **Operating System** | `Kernel Panic (KP)`, `Kernel`, `Userland`, `Hypervisor (HV)`, `Ring -1`, `Ring 0`, `kASLR`, `Syscall` | POSIX, FreeBSD, and hardware privilege architecture. |
| **Execution Delivery** | `Payload`, `Payload Injection`, `Autoloader`, `Daemon`, `ELF Loader` | Binary injection and execution mechanisms. |
| **Formats & Security** | `FSELF`, `FPKG`, `Keystone`, `Keystone DRM`, `app.db`, `Capsicum` | Proprietary Sony Prospero file formats and container systems. |
| **Homebrew Ecosystem** | `Homebrew`, `Toolbox`, `Trainer`, `Backups`, `Savegame`, `Debug Settings` | Community application and modification terms. |
| **Specific Projects** | `Relapse-Exploit`, `UMTX`, `Byepervisor`, `BD-JB`, `Mast1c0re`, `etaHEN`, `ps5-kstuff`, `elfldr`, `libhijacker`, `shsrv`, `ftps5`, `websrv`, `gdbsrv`, `Itemzflow` | Software package names and project identifiers. |
| **Ports** | `9021`, `9027`, `1337`, `2323`, `3232`, `8080`, `2159` | Standardized network service ports. |
| **DNS Addresses** | `45.56.67.85`, `62.210.38.117`, `165.227.83.145` | Static public community redirect servers. |

### 📖 The "TECHNICAL TERMS" Topic Obligation
Every translated documentation file **must include Section 9 ("Technical Terms & Scene Glossary")**.
- In Section 9, explain these terms in the target language so readers understand their underlying mechanisms, but **keep the terms themselves in English**.

---

## 🌐 Adding New Languages

If a user or task asks to support a new language (e.g., Spanish `es`, French `fr`, German `de`, Japanese `ja`):

1. Create directory `i18n/<lang_code>/`.
2. Translate the entire documentation into `i18n/<lang_code>/README.md` ensuring full section parity.
3. Strictly enforce the Untranslatable Technical Terms policy above.
4. Update the language selector table in the root `README.md` with the new language option and flag emoji.
5. Update the language navigation bar at the top of all existing `i18n/*/README.md` files.

---

## 🤖 AI Disclosure & Legal Preservation

Always retain the AI-assisted curation notice in Section 11 and in the document footers:
```html
<p align="center">
  <b>🤖 AI-Generated & Curated Compendium</b><br>
  <i>This reference guide is synthesized using AI from publicly disclosed security research and community documentation for educational and archival purposes. Keep your console offline and preserve your firmware.</i>
</p>
```
Do not claim maintenance by Sony, official organizations, or unofficial teams without factual attribution.
