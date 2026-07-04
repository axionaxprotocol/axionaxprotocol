# Copilot Instructions for nakharax.io

## Repository Role

This is the **organization-level landing page repository** for **nakharax.io** (formerly Axionax Protocol). It contains the root `README.md`, supporting assets, and a **Git submodule** at the repository root that embeds the upstream monorepo for a **pinned, reviewable snapshot** of its current `main` (or default branch) history.

**Primary content is not application code authored here.** Implementation is developed in a single monorepo:
- **nakharax** (Rust/Python core + Next.js/React/TypeScript apps + shared SDK): `axionaxprotocol/nakharax` (submodule path: `nakharax/`)

The submodule **commit advances only when this repo is updated** (e.g. after `git submodule update --remote` and a parent commit). That is how maintainers record "upstream was at SHA … as of this landing-page revision."

## Primary Responsibilities

When working in this repository, focus on:

1. **README.md maintenance** - Keep the organization overview accurate and up-to-date
2. **Cross-repository navigation** - Ensure links to the upstream repo are current
3. **Status updates** - Reflect latest achievements, roadmap progress, and metrics
4. **Onboarding clarity** - Help new contributors understand the monorepo architecture

## Key Architecture Concepts

### Rebrand and consolidation (July 2026)
The project was renamed **Axionax Protocol → nakharax.io** (token `AXX` → `NAK`, domain `axionax.org` → `nakharax.io`) and consolidated from **two Universe monorepos → one monorepo**:
- Core Universe (`axionax-core-universe`) and Web Universe (`axionax-web-universe`) were merged into `nakharax`, with a strict Web ↔ Core boundary enforced in-repo (`.windsurfrules`), communicating only via the JSON-RPC contract on port 8545.

When updating content, emphasize this single-monorepo architecture and the rebrand — do not reintroduce "Core Universe" / "Web Universe" as separate repositories.

### Project structure reference
```
axionaxprotocol/axionaxprotocol (this repo)
├── README.md, assets/, .github/
└── nakharax/                ← submodule → axionaxprotocol/nakharax
    ├── apps/
    │   ├── web/              — Public dApp + marketplace (Next.js · TypeScript)
    │   └── os-dashboard/      — Self-hosted node OS UI (Next.js · Tailwind)
    ├── services/core/         — Blockchain core + DeAI worker (Rust · Python)
    ├── packages/              — Shared TypeScript packages (@nakharax/sdk)
    ├── docs/                  — Cross-cutting docs (playbook, audits, RFCs, REBRAND_MIGRATION.md)
    └── scripts/               — Cross-cutting ops scripts
```
Verify layout in the submodule's `main` (or default branch) when updating pointers or documentation.

## Content Guidelines

### Technical specifications
Keep these aligned with the README and the upstream repository:
- **Chain ID:** 86137 (testnet), 86150 (mainnet, planned), 31337 (local development)
- **Performance:** State throughput, finality, and fees as *targets* or *design goals* unless citing a published benchmark; link to upstream for measured results when available
- **Consensus:** PoPC (Proof of Probabilistic Checking)
- **Tech stack:** Rust, Python, TypeScript, Next.js 14, Docker
- **Native token:** `NAK` (was `AXX`)

### Roadmap phases
Keep this aligned with the root **README** roadmap table and verify details in the upstream README when updating.

Current README framing (update this list when the README roadmap changes):
- Phase 1 (Foundation): 100% complete
- Phase 2 (Optimization): 100% complete
- Phase 3 (Launch preparation): in progress — rebrand complete, public testnet validators (EU + AU) live
- Phase 4 (Mainnet): Q2 2026 target

Treat narrative percentages or delivery claims as **planning indicators** unless backed by a cited benchmark or release note in the upstream repo.

### Tone & language
- **English** only for repository-facing content
- Professional, direct, and scannable: minimal emoji in headings; reserve decorative elements for badges or optional footers where they aid scanning
- Qualify performance claims where appropriate (e.g. *target architecture*, *planning indicators*) and link to the upstream repo for ground truth
- Use **nakharax.io** / **NAK** for product naming; note "formerly Axionax Protocol" where helpful for continuity, but do not lead with the old name

## Common Updates

### Adding new features
When referencing new features, link to the upstream repo:
```markdown
- New feature in nakharax ([PR #123](https://github.com/axionaxprotocol/nakharax/pull/123))
```

### Submodule pointer
- After advancing the submodule with `git submodule update --remote`, **commit the parent repo** so GitHub shows the new submodule SHA (compare view / history).
- Prefer short, descriptive parent commits: e.g. `chore: bump nakharax submodule to <short-sha>`.
- Do not rewrite submodule history; treat it as a read-only mirror of upstream except for pointer bumps.

### Updating statistics
When adding or updating metrics in the README, verify against the actual repository:
- Test counts: run or check CI upstream (cargo test / pytest / frontend typecheck)
- File counts and doc page counts: confirm in the upstream repo
- Phase completion: keep aligned with roadmap section
Do not hardcode numbers that can become outdated; link to the repo or "see repository" where appropriate.

### Link Maintenance
Keep these links current and working:
- **Website & documentation:** `https://nakharax.io` — official site; all documentation is hosted here.
- Testnet RPC: `https://rpc.nakharax.io`; see the upstream README "Network" section for validator details and live endpoints.
- Issues: Link to the upstream `nakharax` repo.

## Do not

- **Implement protocol or product features inside the parent repo** — edit the upstream `nakharax` repo, then bump the submodule pointer here if needed
- **Add unrelated top-level trees** — keep root limited to `README.md`, `LICENSE`, `AGENTS.md` (if present), `assets/`, `.github/`, `.gitmodules`, and the single `nakharax/` submodule path
- **Duplicate upstream documentation** — summarize and link out (the submodule is for checkout and SHA tracking, not doc copies)
- **Change license summaries** inaccurately — **this landing repo** is MIT (`LICENSE` at repository root); upstream is AGPL-3.0 by default, MIT for explicit downstream agreements, by sub-tree
- **Feature unrelated org products** (e.g. other ventures under the same GitHub org that share no code or branding with nakharax.io) — this profile is scoped to nakharax.io only

## When to Redirect

If asked to work on actual implementation:
- **Blockchain/consensus code** → Direct to `nakharax/services/core`
- **Website/UI features** → Direct to `nakharax/apps`
- **SDK development** → Direct to `nakharax/packages/sdk`
- **Deployment configs** → Direct to `nakharax/services/core/ops/deploy`

## Recent Changes

- **Jul 4, 2026**: **Rebrand sync** — Axionax Protocol → **nakharax.io** (`AXX` → `NAK`, `axionax.org` → `nakharax.io`); collapsed the two Core/Web Universe submodules into a single `nakharax/` submodule pointing at the consolidated monorepo; replaced brand assets with official nakharax SVGs; README, AGENTS.md, and this file updated to match
- **Apr 1, 2026**: **Merged to `main`** — Resolved README/Copilot conflicts with upstream; preserved root `LICENSE` (MIT), `AGENTS.md`, README roadmap table from `main`; integrated submodules + professional README sections
- **Apr 1, 2026**: **Git submodules** — `axionax-core-universe/` and `axionax-web-universe/` at repo root; README "Universe submodules" section (`clone --recurse-submodules`, `submodule update --remote`); Copilot structure and "Do not" rules updated for submodule workflow
- **Apr 1, 2026**: README and Copilot refresh — **Axionax Protocol** branding; qualified metrics and planning-indicator roadmap; org-profile callout in README; SDK example `chainId: 31337` for localhost with testnet note; contributing uses `git switch`; community defers to axionax.org (no placeholder social badges); org-stats widget disclaimer; TOC includes Organization activity; Copilot specs/roadmap aligned; "Do not" section as plain list
- **Mar 30, 2026**: Status sync — Roadmap phases updated (Phase 2→95%, Phase 3→50%, Phase 4→20%); Testnet status→Active; Mainnet→In Preparation; Community Channels launch pushed to Q2 2026
- **Feb 20, 2026**: Documentation now on main website only — all axionax-docs / GitHub Pages docs URLs removed; documentation links point to https://axionax.org
- **Feb 20, 2026**: Data verification pass — Network table (Testnet link to Core README), License links (Core has no root LICENSE; use README#license), added axionax.org; copilot structure/stats/links aligned with actual repos
- **Feb 20, 2026**: README overhaul — professional structure, English-only, Table of Contents, refined Quick Start & Roadmap
- **Nov 22, 2025**: Universe architecture migration completed
- **Nov 22, 2025**: PoPC definition standardized to "Proof of Probabilistic Checking"
