# AGENTS.md

## Repository Overview

This is the **organization-level landing page** for axionax Protocol (`axionaxprotocol/axionaxprotocol`). It is explicitly **not a code repository** — it contains only documentation (`README.md`), GitHub Copilot configuration, and two saved HTML page snapshots.

The actual runnable code lives in two separate repositories:
- **Core Universe** (Rust/Python): `axionaxprotocol/axionax-core-universe`
- **Web Universe** (Next.js/React/TypeScript): `axionaxprotocol/axionax-web-universe`

See `.github/copilot-instructions.md` for full context on this repo's purpose and content guidelines.

## Cursor Cloud specific instructions

- **No build, lint, or test tooling exists in this repo.** There is no `package.json`, no lockfile, no Makefile, and no CI configuration. Do not attempt to run `pnpm install`, `npm install`, `cargo build`, or similar commands.
- **No dependencies to install.** The update script is intentionally a no-op (`echo "No dependencies to install"`).
- **Content is static.** The repo contains `README.md` (GitHub profile page), `.github/copilot-instructions.md`, and two large HTML snapshots (`share_page.html`, `share_page_brand.html`). To preview the HTML files locally, use `python3 -m http.server 8080` from the workspace root and open them in a browser.
- **Edits should be limited to documentation.** Per `.github/copilot-instructions.md`, do not add source code, create new directories, or duplicate content from the Universe repos.
- **For actual development work** on the blockchain core, web apps, SDK, or marketplace, you need to clone and work in the appropriate Universe repository — not this one.
