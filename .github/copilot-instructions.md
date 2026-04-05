# Copilot Instructions for axionax Protocol

## Repository Role

This is the **organization-level landing page repository** for **Axionax Protocol**. It contains the root `README.md`, supporting assets, and **Git submodules** at the repository root that embed the two Universe upstreams for a **pinned, reviewable snapshot** of their current `main` (or default branch) history.

**Primary content is not application code authored here.** Implementation is developed in:
- **Core Universe** (backend): `axionaxprotocol/axionax-core-universe` — protocol, deployment, dev tools (submodule path: `axionax-core-universe/`)
- **Web Universe** (frontend): `axionaxprotocol/axionax-web-universe` — web apps, marketplace, docs, SDK (submodule path: `axionax-web-universe/`)

Submodule **commits advance only when this repo is updated** (e.g. after `git submodule update --remote` and a parent commit). That is how maintainers record “Core/Web were at SHA … as of this landing-page revision.”

## Primary Responsibilities

When working in this repository, focus on:

1. **README.md maintenance** - Keep the organization overview accurate and up-to-date
2. **Cross-repository navigation** - Ensure links to Core/Web Universe repos are current
3. **Status updates** - Reflect latest achievements, roadmap progress, and metrics
4. **Onboarding clarity** - Help new contributors understand the Universe architecture

## Key Architecture Concepts

### Universe Migration (November 2025)
The project recently consolidated from **7 separate repositories → 2 monorepos**:
- Reduced setup time from ~30 mins to ~5 mins
- Eliminated duplicate dependencies (60% reduction)
- Centralized CI/CD (7 pipelines → 2)
- Improved developer experience significantly

When updating content, emphasize this modern monorepo architecture.

### Project structure reference
```
axionaxprotocol/axionaxprotocol (this repo)
├── README.md, assets/, .github/
├── axionax-core-universe/   ← submodule → axionaxprotocol/axionax-core-universe
│   ├── core/          — Rust blockchain + Python DeAI (PoPC, staking, RPC)
│   ├── configs/       — Monolith / Scout TOML configs
│   ├── scripts/       — join-axionax, update-node, health-check
│   ├── ops/           — Docker, Nginx, monitoring (e.g. ops/deploy)
│   └── tools/         — Dev utilities, faucet
└── axionax-web-universe/    ← submodule → axionaxprotocol/axionax-web-universe
    ├── apps/          — web (Next.js), marketplace (Vite/React), etc.
    ├── packages/sdk/  — TypeScript SDK (@axionax/sdk)
    └── docs/          — Documentation (if present)
```
Verify layout in each submodule’s `main` (or default branch) when updating pointers or documentation.

## Content Guidelines

### Technical specifications
Keep these aligned with the README and Universe repositories:
- **Chain ID:** 86137 (testnet), 86150 (mainnet, planned), 31337 (local development)
- **Performance:** State throughput, finality, and fees as *targets* or *design goals* unless citing a published benchmark; link to Core for measured results when available
- **Consensus:** PoPC (Proof of Probabilistic Checking)
- **Tech stack:** Rust, Python, TypeScript, Next.js 14, Docker

### Roadmap phases
Keep this aligned with the root **README** roadmap table and verify details in Core/Web Universe READMEs when updating.

Current README framing (update this list when the README roadmap changes):
- Phase 1 (Foundation): 100% complete
- Phase 2 (Optimization): 100% complete
- Phase 3 (Launch preparation): in progress
- Phase 4 (Mainnet): Q2 2026 target

Treat narrative percentages or delivery claims as **planning indicators** unless backed by a cited benchmark or release note in the Universe repos.

### Tone & language
- **English** only for repository-facing content
- Professional, direct, and scannable: minimal emoji in headings; reserve decorative elements for badges or optional footers where they aid scanning
- Qualify performance claims where appropriate (e.g. *target architecture*, *planning indicators*) and link to Universe repos for ground truth
- Use **Axionax Protocol** / **AXX** for product naming; avoid inconsistent casing (e.g. "axionax" in titles)

## Common Updates

### Adding new features
When referencing new features, link to the specific Universe repo:
```markdown
- New feature in Core Universe ([PR #123](https://github.com/axionaxprotocol/axionax-core-universe/pull/123))
```

### Submodule pointers
- After advancing submodules with `git submodule update --remote`, **commit the parent repo** so GitHub shows the new submodule SHAs (compare view / history).
- Prefer short, descriptive parent commits: e.g. `chore: bump core-universe submodule to <short-sha>`.
- Do not rewrite submodule history; treat them as read-only mirrors of upstream except for pointer bumps.

### Updating statistics
When adding or updating metrics in the README, verify against the actual repositories:
- Test counts: run or check CI in Core (cargo test / pytest) and Web
- File counts and doc page counts: confirm in each repo
- Phase completion: keep aligned with roadmap section
Do not hardcode numbers that can become outdated; link to repos or "see repository" where appropriate.

### Link Maintenance
Keep these links current and working:
- **Website & documentation:** `https://axionax.org` — official site; all documentation is hosted here (axionax-docs repo/URL no longer used).
- Testnet RPC: See Core Universe README "Current Network (Testnet)" for live endpoints.
- Issues: Link to the appropriate Universe repo.

## Do not

- **Implement protocol or product features inside the parent repo** — edit Core or Web Universe upstream, then bump submodule pointers here if needed
- **Add unrelated top-level trees** — keep root limited to `README.md`, `LICENSE`, `AGENTS.md` (if present), `assets/`, `.github/`, `.gitmodules`, and the two fixed submodule paths
- **Duplicate Universe documentation** — summarize and link out (submodules are for checkout and SHA tracking, not doc copies)
- **Change license summaries** inaccurately — **this landing repo** is MIT (`LICENSE` at repository root); Core is AGPLv3/MIT by path; Web Universe is MIT

## When to Redirect

If asked to work on actual implementation:
- **Blockchain/consensus code** → Direct to axionax-core-universe
- **Website/UI features** → Direct to axionax-web-universe  
- **SDK development** → Direct to axionax-web-universe/packages/sdk
- **Deployment configs** → Direct to axionax-core-universe/ops/deploy

## Recent Changes

- **Apr 1, 2026**: **Merged to `main`** — Resolved README/Copilot conflicts with upstream; preserved root `LICENSE` (MIT), `AGENTS.md`, README roadmap table from `main`; integrated submodules + professional README sections
- **Apr 1, 2026**: **Git submodules** — `axionax-core-universe/` and `axionax-web-universe/` at repo root; README “Universe submodules” section (`clone --recurse-submodules`, `submodule update --remote`); Copilot structure and “Do not” rules updated for submodule workflow
- **Apr 1, 2026**: README and Copilot refresh — **Axionax Protocol** branding; qualified metrics and planning-indicator roadmap; org-profile callout in README; SDK example `chainId: 31337` for localhost with testnet note; contributing uses `git switch`; community defers to axionax.org (no placeholder social badges); org-stats widget disclaimer; TOC includes Organization activity; Copilot specs/roadmap aligned; "Do not" section as plain list
- **Mar 30, 2026**: Status sync — Roadmap phases updated (Phase 2→95%, Phase 3→50%, Phase 4→20%); Testnet status→Active; Mainnet→In Preparation; Community Channels launch pushed to Q2 2026
- **Feb 20, 2026**: Documentation now on main website only — all axionax-docs / GitHub Pages docs URLs removed; documentation links point to https://axionax.org
- **Feb 20, 2026**: Data verification pass — Network table (Testnet link to Core README), License links (Core has no root LICENSE; use README#license), added axionax.org; copilot structure/stats/links aligned with actual repos
- **Feb 20, 2026**: README overhaul — professional structure, English-only, Table of Contents, refined Quick Start & Roadmap
- **Nov 22, 2025**: Universe architecture migration completed
- **Nov 22, 2025**: PoPC definition standardized to "Proof of Probabilistic Checking"
