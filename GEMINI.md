# ♊ Guidelines for Gemini & Antigravity Agents

The repository is an interactive, multilingual PS5 guide. The wizard is the only user-facing procedure; do not recreate or maintain separate static how-to, technical, or compendium guides.

## Maintenance Rules

1. **Keep all wizard languages in sync.** Update equivalent user-facing content in `interactive/i18n/en/README.md`, `interactive/i18n/es/README.md`, and `interactive/i18n/pt/README.md`. Keep relevant UI and route logic in `interactive/index.html` consistent across languages.
2. **Write for readers who want to follow steps.** Put clear actions and expected outcomes first. Keep technical explanations optional and concise. If a firmware has no verified wizard route, ask the reader to check current compatibility rather than assigning it to another route.
3. **Preserve technical and project names** when they are needed, but do not make understanding exploit internals a prerequisite for using the wizard.
4. **Keep the root `README.md` a portal** with the banner, repository/license badges, links to all three interactive wizard languages, and the AI-curation notice. Do not put guide content there.
5. **Preserve `.nojekyll`** and the PlayStation dark visual theme. Keep root and localized navigation links pointed at the interactive wizard.
6. **Never push to GitHub.** Changes stay local; the user decides when to publish.
7. **Stay within the requested scope** and preserve unrelated files and behavior.

## Adding a Language

Add a localized wizard page under `interactive/i18n/<lang_code>/README.md`, synchronize its navigation and wording, and add it to the root portal.

## AI Disclosure

Retain the AI-assisted curation notice on the root portal. Do not imply Sony or another organization endorses or maintains this repository without evidence.
