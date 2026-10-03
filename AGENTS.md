# 🤖 Repository Maintenance Guidelines

This repository is an interactive, multilingual PS5 guide. The wizard is the only user-facing procedure; do not recreate or maintain separate static how-to, technical, or compendium guides.

## Repository Structure

```text
├── assets/                         # Shared visual assets
├── interactive/
│   ├── README.md                   # English interactive wizard
│   ├── i18n/en/README.md           # English wizard route
│   ├── i18n/es/README.md           # Spanish wizard route
│   ├── i18n/pt/README.md           # Portuguese wizard route
│   ├── index.html                  # Docsify app, styling, and wizard behavior
│   ├── _sidebar.md                # Wizard navigation
│   ├── _navbar.md                 # Wizard language navigation
│   └── i18n/*/_sidebar.md          # Localized wizard navigation
├── i18n/*/_sidebar.md              # Root-site language navigation
├── index.html                     # Entry point redirecting to the wizard
├── README.md                      # Lightweight language-selection portal
├── .nojekyll                      # Preserve for GitHub Pages
└── GEMINI.md                      # Gemini/Antigravity maintenance guidance
```

## Core Rules

### 1. Keep the wizard languages synchronized
- When changing wizard content or behavior, update the equivalent English, Spanish, and Portuguese versions in `interactive/i18n/{en,es,pt}/README.md` and `interactive/index.html` as applicable.
- Keep firmware choices, warnings, steps, and outcomes consistent in all three languages.
- Check navigation links whenever routes change.

### 2. Write for people who want to follow steps
- Lead with the action the reader needs to take and the expected result.
- Keep technical explanations optional and brief; do not require readers to learn exploit internals to follow a procedure.
- Use clear firmware choices and stop with an explicit verification message when the wizard has no supported route. Never silently assign an unlisted firmware to another route.
- Preserve standard project and technical names (for example, `Jailbreak`, `Payload`, `etaHEN`, and `ps5-kstuff`) when they appear, but avoid adding a glossary or jargon-heavy explanations unless requested.

### 3. Keep the root README as a portal
- The root `README.md` must remain a landing page with the banner, repository/license badges, links to the three interactive language versions, and the AI-curation notice.
- Do not add standalone guides or technical documentation to the root README.

### 4. Docsify and GitHub Pages
- The site uses Docsify and requires no static-site build step.
- Never delete or alter `.nojekyll`.
- Keep `_sidebar.md`, `_navbar.md`, and the language sidebars free of links to removed static guides; point readers to the interactive wizard.
- Preserve the established dark PlayStation visual theme when changing app styling.

### 5. Local-only changes
- Never run `git push` or publish changes to a remote. The user controls publishing.
- Make only changes explicitly requested or required to keep the requested work consistent.

## Adding a Language

1. Add `interactive/i18n/<lang_code>/README.md` and its localized sidebar.
2. Translate the wizard UI and procedure text while preserving project names and route behavior.
3. Add the language to the root portal and navigation.

## AI Disclosure

Retain the AI-assisted curation notice in the root portal and do not claim endorsement or maintenance by Sony or other organizations without factual attribution.
