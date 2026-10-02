# ♊ Guidelines for Gemini & Antigravity Agents

This document provides system-level instructions for **Gemini models** and **Antigravity CLI agents** operating within the `PS5-JB-LINKS` workspace.

---

## 🎯 Primary Directives

1. **Keep All Internationalized Documents in Sync**:
   - The documentation in this repository is distributed across:
     - `i18n/en/README.md` (English Index)
     - `i18n/en/jailbreak_how_to.md` (English Step-by-Step Guide)
     - `i18n/en/jailbreak_tech_info.md` (English Technical Deep Dive)
     - `i18n/pt/README.md` (Português Index)
     - `i18n/pt/jailbreak_how_to.md` (Português Guia Prático)
     - `i18n/pt/jailbreak_tech_info.md` (Português Análise Técnica)
   - **Action Rule**: Whenever you modify, expand, or fix any section in one language, you **must immediately reflect the equivalent changes in all other active languages**.
   - Keep the clean separation between practical how-to (`jailbreak_how_to.md`) and low-level internals (`jailbreak_tech_info.md`).
   - Do not complete a task until both English and Portuguese versions are 100% synchronized in content, table columns, code snippets, and structural sections.

2. **Root `README.md` Contract**:
   - The root `README.md` must remain lightweight and visual.
   - It contains only:
     - The top header banner (`assets/banner.png` or `banner.png`) with text `"PS5 JAILBREAK COMPENDIUM"`.
     - Badges (Firmware status, latest exploit, license).
     - The language selector table linking to `/i18n/[lang]/README.md`.
     - The AI curation disclaimer.
   - Do not bloat the root `README.md` with full documentation bodies.

3. **Untranslatable Technical Terms Policy**:
   - **Strict Prohibition**: Never translate standardized technical keywords, protocols, or exploitation concepts into regional dialects.
   - Specifically:
     - **`Handshake`**: Never translate as `"aperto de mão"`. Use `Handshake` or `Handshake Criptográfico`.
     - **`Jailbreak`**: Never translate as `"fuga da prisão"`.
     - **`Payload`**: Never translate as `"carga útil"`.
     - **`Kernel Panic`**: Never translate as `"pânico no kernel"`.
     - **`Heap Spray`**: Never translate as `"spray de heap"`.
     - **`Use-After-Free (UAF)`**: Preserve abbreviation and concept verbatim.
     - **`Sandbox` / `Sandbox Escape`**: Never translate as `"caixa de areia"`.
     - **`Rest Mode`**: Preserve as `Rest Mode` (or mention alongside `Modo de Repouso`).
     - **`Dump` / `Dumping`**: Never translate as `"despejo"`.
     - **`Hook` / `Hooking`**: Preserve verbatim.
   - Also preserve:
     - `Relapse-Exploit`, `UMTX`, `Byepervisor`, `BD-JB`, `Mast1c0re`
     - `aio_multi_wait`, `JavaScriptCore`, `StructuredSerialize`, `ArrayBuffer`, `Uint32Array`
     - `etaHEN`, `ps5-kstuff`, `kstuff-lite`, `elfldr`, `libhijacker`, `shsrv`, `ftps5`, `websrv`, `gdbsrv`
     - Ports: `9021`, `9027`, `1337`, `2323`, `3232`, `8080`, `2159`
     - DNS IPs: `45.56.67.85`, `62.210.38.117`, `165.227.83.145`
   - **Mandatory Topic**: Every language file must maintain Section 9 as **"Technical Terms & Scene Glossary"** where these terms are thoroughly explained in the local language, while keeping the terms themselves in English.

4. **11-Section Relevance Order**:
   Every translation file must follow this exact section sequence:
   1. 📊 1. Firmwares with Available Jailbreaks (Matrix, Tiers, Relapse Exploit, Hardware models)
   2. 🚀 2. How to Jailbreak: Chain of Procedures & Preparations (Flowchart, Anti-Update, Slim/Pro Advisory, DNS, Trigger, Payload Injection)
   3. 🧰 3. Curated Exploits & Entry Points
   4. ⚙️ 4. Essential Payloads & System Frameworks
   5. 📦 5. Payload Injection & Automation Methods
   6. 🕹️ 6. Homebrew Apps, Emulators & Game Managers
   7. 🌐 7. Exploit Hosts, DNS Servers & Offline Tools
   8. 🔧 8. Troubleshooting & Panic Recovery
   9. 📚 9. Technical Terms & Scene Glossary
   10. 🏛️ 10. Background: Exploitation Timeline & Security Architecture
   11. ⚖️ 11. Disclaimer & AI Curation Notice

5. **Windows & Git Environment Guidelines**:
   - **🚫 STRICT DIRECTIVE: NEVER execute `git push` automatically**:
     - Agents must **NEVER** push commits or files to GitHub or any remote repository automatically.
     - All documentation, translation, and code updates must remain local to the workspace.
     - If the upload workflow, remote URL, or push commands require changes, update the local [`upload.bat`](upload.bat) script only.
     - The user will inspect changes and execute `upload.bat` manually to publish to GitHub.
   - On this machine, prioritize `C:\Program Files\Git\cmd\git.exe` for local git commands (it has Git Credential Manager configured).
   - Ensure `upload.bat` is ignored by `.gitignore` and never committed to the remote repo.
   - Ensure commits for documentation updates reference both languages (e.g., `docs: Update technical terms and glossary across en and pt`).

6. **AI Disclaimer Integrity**:
   - Preserve the notice indicating that this repository is an AI-generated and curated reference compendium for educational and research purposes.
