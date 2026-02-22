# Copilot Instructions for axionax Protocol

## Repository Role

This is the **organization-level landing page repository** for axionax Protocol. It contains only the main `README.md` that serves as the entry point for the entire project ecosystem.

**This is NOT a code repository.** The actual implementation lives in two separate Universe repositories:
- **Core Universe** (Backend): `axionaxprotocol/axionax-core-universe` - Blockchain protocol, deployment, dev tools
- **Web Universe** (Frontend): `axionaxprotocol/axionax-web-universe` - Web apps, marketplace, docs, SDK

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

### Project Structure Reference
```
axionax Protocol Organization
├── axionaxprotocol/axionaxprotocol (this repo) - Landing page
├── axionax-core-universe/
│   ├── core/          - Rust blockchain + Python DeAI (PoPC, staking, RPC)
│   ├── configs/       - Monolith / Scout TOML configs
│   ├── scripts/       - join-axionax, update-node, health-check
│   ├── ops/           - Docker, Nginx, monitoring (e.g. ops/deploy)
│   └── tools/         - Dev utilities, faucet
└── axionax-web-universe/
    ├── apps/          - web (Next.js), marketplace (Vite/React), etc.
    ├── packages/sdk/  - TypeScript SDK (@axionax/sdk)
    └── docs/          - Documentation (if present)
```
Verify current layout in each repo's README when updating.

## Content Guidelines

### Technical Specifications
Maintain consistency with these core specs:
- **Chain ID**: 86137 (Testnet), 86150 (Mainnet), 31337 (Local)
- **Performance**: 45,000+ TPS, <0.5s finality, $0.0001 avg fee
- **Consensus**: PoPC (Proof of Probabilistic Checking)
- **Tech Stack**: Rust, Python, TypeScript, Next.js 14, Docker

### Roadmap Phases
Keep phase completion percentages accurate:
- Phase 1 (Foundation): ✅ 100% Complete
- Phase 2 (Optimization): 🔄 70% Complete
- Phase 3 (Launch Prep): Q1 2026
- Phase 4 (Mainnet): Q2 2026

### Tone & Language
- **English** only (the entire repository now uses English)
- Professional but friendly (use emojis in tables/sections)
- Focus on tangible achievements over promises
- Use "we" when referring to the team

## Common Updates

### Adding New Features
When referencing new features, link to the specific Universe repo:
```markdown
- ✅ New feature in Core Universe ([PR #123](https://github.com/axionaxprotocol/axionax-core-universe/pull/123))
```

### Updating Statistics
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

## Don't Do This

❌ **Add source code** - This repo is documentation only  
❌ **Create new directories** - Only `.github/` and root `README.md` belong here  
❌ **Duplicate content** - Don't copy docs from Universe repos, link to them  
❌ **Change license info** - Universe repos have specific licenses (AGPLv3/MIT)

## When to Redirect

If asked to work on actual implementation:
- **Blockchain/consensus code** → Direct to axionax-core-universe
- **Website/UI features** → Direct to axionax-web-universe  
- **SDK development** → Direct to axionax-web-universe/packages/sdk
- **Deployment configs** → Direct to axionax-core-universe/ops/deploy

## Recent Changes

- **Feb 20, 2026**: Documentation now on main website only — all axionax-docs / GitHub Pages docs URLs removed; documentation links point to https://axionax.org
- **Feb 20, 2026**: Data verification pass — Network table (Testnet link to Core README), License links (Core has no root LICENSE; use README#license), added axionax.org; copilot structure/stats/links aligned with actual repos
- **Feb 20, 2026**: README overhaul — professional structure, English-only, Table of Contents, refined Quick Start & Roadmap
- **Nov 22, 2025**: Universe architecture migration completed
- **Nov 22, 2025**: PoPC definition standardized to "Proof of Probabilistic Checking"
