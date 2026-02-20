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
│   ├── core/          - Rust blockchain + Python DeAI
│   ├── ops/deploy/    - Docker, Nginx, monitoring
│   └── tools/devtools/ - Testing framework (42 tests)
└── axionax-web-universe/
    ├── apps/web/         - Next.js 14 website
    ├── apps/marketplace/ - React marketplace dApp
    ├── apps/docs/        - 50+ documentation pages
    └── packages/sdk/     - TypeScript SDK
```

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
Key metrics in the README that may need updates:
- Total tests count (currently 42)
- Total files (currently 1,845+)
- Documentation pages (currently 50+)
- Phase completion percentages

### Link Maintenance
All external links point to:
- Website: `http://217.216.109.5` (production VPS)
- Docs: `https://axionaxprotocol.github.io/axionax-docs/`
- Issues: Link to appropriate Universe repo

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

- **Nov 22, 2025**: Universe architecture migration completed
- **Nov 22, 2025**: PoPC definition standardized to "Proof of Probabilistic Checking"
- Previous: UI enhancements, 42-test suite, production deployment automation
