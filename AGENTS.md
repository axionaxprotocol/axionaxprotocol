# AGENTS.md

## Repository Overview

This is the **organization-level landing page** for nakharax.io, formerly Axionax Protocol (`axionaxprotocol/axionaxprotocol`). It is explicitly **not a code repository** — it contains only documentation (`README.md`) and GitHub Copilot configuration.

The actual runnable code lives in a single monorepo:
- **nakharax** (Rust/Python core + Next.js/React/TypeScript apps + shared SDK): `axionaxprotocol/nakharax`

See `.github/copilot-instructions.md` for full context on this repo's purpose and content guidelines.

## Cursor Cloud specific instructions

- **No build, lint, or test tooling exists in this repo.** There is no `package.json`, no lockfile, no Makefile, and no CI configuration. Do not attempt to run `pnpm install`, `npm install`, `cargo build`, or similar commands.
- **No dependencies to install.** The update script is intentionally a no-op (`echo "No dependencies to install"`).
- **Content is static.** The repo contains `README.md` (GitHub profile page) and `.github/copilot-instructions.md`.
- **Edits should be limited to documentation.** Per `.github/copilot-instructions.md`, do not add source code, create new directories, or duplicate content from the upstream monorepo.
- **For actual development work** on the blockchain core, web apps, SDK, or marketplace, you need to clone and work in the `nakharax` repository — not this one.
