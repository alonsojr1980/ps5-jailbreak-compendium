# ♊ Guidelines for Gemini & Antigravity Agents

This document provides system-level instructions for **Gemini models** and **Antigravity CLI agents** operating within the `PS5-JB-LINKS` workspace.

---

## 🎯 Primary Directives

1. **Keep All Internationalized Documents in Sync**:
   - The documentation in this repository is distributed across:
     - `i18n/en/README.md` (English)
     - `i18n/pt/README.md` (Português)
   - **Action Rule**: Whenever you modify, expand, or fix any section in one language, you **must immediately reflect the equivalent changes in all other active languages**.
   - Do not complete a task until both English and Portuguese versions are 100% synchronized in content, table columns, code snippets, and structural sections.

2. **Root `README.md` Contract**:
   - The root `README.md` must remain lightweight and visual.
   - It contains only:
     - The top header banner (`assets/banner.png` or `banner.png`) with text `"PS5 JAILBREAK COMPENDIUM"`.
     - Badges (Firmware status, latest exploit, license).
     - The language selector table linking to `/i18n/[lang]/README.md`.
     - The AI curation disclaimer.
   - Do not bloat the root `README.md` with full documentation bodies.

3. **Technical Terms & Keyword Preservation**:
   - Never translate technical jargon, function names, syscalls, or tool identifiers into regional dialects.
   - Always preserve:
     - `Relapse-Exploit`, `UMTX`, `Byepervisor`, `BD-JB`, `Mast1c0re`
     - `aio_multi_wait`, `JavaScriptCore`, `StructuredSerialize`, `ArrayBuffer`, `Uint32Array`
     - `etaHEN`, `ps5-kstuff`, `kstuff-lite`, `elfldr`, `libhijacker`, `shsrv`, `ftps5`, `websrv`, `gdbsrv`
     - Ports: `9021`, `9027`, `1337`, `2323`, `3232`, `8080`, `2159`
     - DNS IPs: `45.56.67.85`, `62.210.38.117`, `165.227.83.145`

4. **11-Section Relevance Order**:
   Every translation file must follow this exact section sequence:
   1. 📊 Firmwares with Available Jailbreaks (Matrix, Tiers, Relapse Exploit, Hardware models)
   2. 🚀 How to Jailbreak: Chain of Procedures & Preparations (Flowchart, Anti-Update, Slim/Pro Advisory, DNS, Trigger, Payload Injection)
   3. 🧰 Curated Exploits & Entry Points
   4. ⚙️ Essential Payloads & System Frameworks
   5. 📦 Payload Injection & Automation Methods
   6. 🕹️ Homebrew Apps, Emulators & Game Managers
   7. 🌐 Exploit Hosts, DNS Servers & Offline Tools
   8. 🔧 Troubleshooting & Panic Recovery
   9. 📚 Glossary of PS5 Scene Terms
   10. 🏛️ Background: Exploitation Timeline & Security Architecture
   11. ⚖️ Disclaimer & AI Curation Notice

5. **Windows & Git Environment Guidelines**:
   - On this machine, prioritize `C:\Program Files\Git\cmd\git.exe` for git commands (it has Git Credential Manager configured).
   - Ensure `upload.bat` is ignored by `.gitignore` and never committed to the remote repo.
   - Ensure commits for documentation updates reference both languages (e.g., `docs: Update payload documentation across en and pt`).

6. **AI Disclaimer Integrity**:
   - Preserve the notice indicating that this repository is an AI-generated and curated reference compendium for educational and research purposes.
