<div align="center">

<img src="assets/nakharax_brand.svg" width="360" alt="nakharax.io brand lockup" />

# nakharax.io

<sub>formerly **Axionax Protocol**. Native token: **NAK** (was AXX).</sub>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=1000&color=29F06A&center=true&vCenter=true&width=600&lines=Cheap%2C+accessible+compute+for+everyone;A+paid%2C+verifiable+grid+for+parallel+science+%26+AI;Own+a+node%2C+earn+NAK" alt="nakharax.io — headline" />

[![Documentation](https://img.shields.io/badge/Documentation-nakharax.io-29F06A?style=for-the-badge&logo=readthedocs&logoColor=white)](https://nakharax.io)
[![License](https://img.shields.io/badge/License-AGPL--3.0%20%2F%20MIT-FF7A1A?style=for-the-badge)](LICENSE)
[![Chain ID](https://img.shields.io/badge/Testnet_Chain_ID-86137-111318?style=for-the-badge)](#network-information)

**Layer-1 network for decentralized compute — PoPC verification, a paid compute marketplace, and science/AI workloads at the edge**

This repository contains the **organization profile** for nakharax.io on GitHub (overview and links). A **pinned snapshot** of upstream development is also included as a **Git submodule** at the repository root (see [Universe submodule](#universe-submodule)).

| Consensus | Native token | Mainnet target |
| :---: | :---: | :--- |
| PoPC (Proof of Probabilistic Checking) | NAK | Q2 2026 |

</div>

---

## Table of contents

- [Overview](#overview)
- [Naming & rebrand](#naming--rebrand)
- [Key features](#key-features)
- [Ecosystem repository](#ecosystem-repository)
- [Universe submodule](#universe-submodule)
- [Quick start](#quick-start)
- [Network information](#network-information)
- [Roadmap](#roadmap)
- [Organization activity](#organization-activity)
- [Contributing](#contributing)
- [License](#license)
- [Connect and support](#connect-and-support)

---

## Overview

**nakharax.io (NAK)** is a Layer-1 network built to run high-throughput decentralized compute for parallel science and AI workloads. Execution, validation, data availability, and settlement are integrated in a single stack so operators can run a node and earn NAK, and builders can deploy without stitching together external modular services.

The design emphasizes performance, security, and a straightforward path for operators and application developers.

---

## Naming & rebrand

The project was renamed **Axionax Protocol → nakharax.io**. The in-repo rename in the upstream monorepo is complete and verified (workspace tests green):

| Layer | Result |
| :--- | :--- |
| Brand / docs / UI | ✅ nakharax.io |
| Native token | ✅ `NAK` (was `AXX`) |
| Domain | ✅ `nakharax.io` (was `axionax.org`) |
| Code identifiers, env vars, packages | ✅ renamed (e.g. `@nakharax/sdk`, `NAKHARAX_*`) |

See the upstream repo's [`docs/REBRAND_MIGRATION.md`](https://github.com/axionaxprotocol/nakharax/blob/main/docs/REBRAND_MIGRATION.md) for the full migration status.

---

## Key features

| Area | Summary |
| :--- | :--- |
| **Compute marketplace** | A paid, verifiable grid where node operators earn **NAK** for parallel science and AI workloads. |
| **Consensus** | **Proof of Probabilistic Checking (PoPC)** supports decentralized validation with efficient block processing. |
| **Data availability** | Built-in data availability layer reduces dependence on third-party DA networks. |
| **Edge compute and AI** | Primitives and tooling for decentralized inference, training workflows, and on-chain/adjacent compute — including NPU-accelerated (Hailo-8) worker roles. |

---

## Ecosystem repository

Work is organized as a **single monorepo** (Web ↔ Core boundary enforced in-repo, communicating only via the JSON-RPC contract on port 8545).

[![nakharax](https://img.shields.io/badge/nakharax-Testnet_live-29F06A?style=for-the-badge&logo=rust)](https://github.com/axionaxprotocol/nakharax)
[![Stars](https://img.shields.io/github/stars/axionaxprotocol/nakharax?style=flat-square&logo=github)](https://github.com/axionaxprotocol/nakharax/stargazers)

- **Stack:** Rust, Python, TypeScript, Next.js 14, Docker
- **Scope:** Blockchain node (`services/core`), PoPC consensus, WASM runtime, web dApp + node OS dashboard (`apps/`), shared SDK (`packages/`)
- **[Repository →](https://github.com/axionaxprotocol/nakharax)**

```
nakharax/
├── apps/
│   ├── web/              # Public dApp + marketplace (Next.js · TypeScript)
│   └── os-dashboard/     # Self-hosted node OS UI (Next.js · Tailwind)
├── services/
│   └── core/             # Blockchain core + DeAI worker (Rust · Python)
├── packages/             # Shared TypeScript packages (@nakharax/sdk)
├── docs/                 # Cross-cutting docs (playbook, audits, RFCs)
└── scripts/               # Cross-cutting ops scripts
```

---

## Universe submodule

The directory `nakharax/` is a **Git submodule** pointing at the official upstream repository. The parent repo records a **specific commit**; that commit moves forward only when this repository is updated (for example after `git submodule update --remote` and a commit). This gives a clear, reviewable record of "how far" upstream was at each landing-page revision.

### Clone this repository with the submodule

```bash
git clone --recurse-submodules https://github.com/axionaxprotocol/axionaxprotocol.git
cd axionaxprotocol
```

If you already cloned without the submodule:

```bash
git submodule update --init --recursive
```

### Advance the submodule pointer to the latest upstream commit

```bash
git submodule update --remote --merge
# Review changes in nakharax/, then commit the updated submodule SHA in the parent repo
```

Use `git submodule status` to see the currently pinned revision.

---

## Quick start

### Node operators and core developers

```bash
git clone https://github.com/axionaxprotocol/nakharax.git
cd nakharax/services/core
docker compose -f docker-compose.dev.yml up -d --build
```

### dApp and web developers

```bash
git clone https://github.com/axionaxprotocol/nakharax.git
cd nakharax
pnpm install
pnpm --filter nakharax-os-dashboard dev
```

### SDK (npm)

```bash
npm install @nakharax/sdk
```

```typescript
import { getBlockNumber, getBalance, isReachable, DEFAULT_NODES } from '@nakharax/sdk';

const rpcUrl = DEFAULT_NODES[0].url; // https://rpc.nakharax.io (public testnet)

if (await isReachable(rpcUrl)) {
  const block = await getBlockNumber(rpcUrl);
  console.log('Latest block:', block.ok ? block.data : block.error.message);
}
```

---

## Network information

| Network | Chain ID | RPC | Status |
| :--- | :---: | :--- | :---: |
| Local development | `31337` | `http://localhost:8545` | Available |
| Testnet | `86137` | `https://rpc.nakharax.io` | Active |
| Mainnet | `86150` | — | In preparation |

Public testnet endpoints: `https://rpc.nakharax.io` · explorer · api · faucet · dApp at `https://app.nakharax.io`. See the [upstream README — Network](https://github.com/axionaxprotocol/nakharax#network) for validator details and P2P troubleshooting.

---

## Roadmap

| Phase | Focus | Status |
| :--- | :--- | :---: |
| **Phase 1: Foundation** | Core blockchain (Rust + PoPC), Smart contracts (WASM), TypeScript SDK, Universe architecture | ✅ **100%** |
| **Phase 2: Optimization** | UI/UX enhancements, Production deployment, DevOps automation, Security audits, throughput testing | ✅ **100%** |
| **Phase 3: Launch Prep** | Axionax → nakharax.io rebrand, public testnet validators (EU + AU), faucet & explorer, validator documentation | 🔄 **In Progress** |
| **Phase 4: Mainnet** | Testnet validation, Genesis ceremony, Token distribution (NAK), Mainnet Launch | 🎯 **Q2 2026** |

---

## Organization activity

<div align="center">

[![GitHub organization overview](https://github-readme-stats.vercel.app/api?username=axionaxprotocol&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=29F06A&icon_color=FF7A1A&text_color=FFFFFF)](https://github.com/axionaxprotocol)

</div>

*Widget by [github-readme-stats](https://github.com/anuraghazra/github-readme-stats); figures are indicative.*

---

## Contributing

We welcome contributions: bug reports, documentation, and code improvements.

1. Fork the [upstream repository](https://github.com/axionaxprotocol/nakharax).
2. Create a branch (`git switch -c feature/your-change`).
3. Commit with clear messages (e.g. `feat:`, `fix:`, `docs:`).
4. Push and open a pull request.

Guidelines and detailed processes are published on **[nakharax.io](https://nakharax.io)**.

---

## License

Dual-licensed under **AGPL-3.0** (default) or **MIT** for explicit downstream agreements:

- **This Repository:** MIT. See [LICENSE](LICENSE).
- **Upstream (`nakharax`):** AGPL-3.0 by default; MIT for explicit downstream agreements. See [License in each sub-tree](https://github.com/axionaxprotocol/nakharax#license).

---

## Connect and support

<div align="center">

[![Website](https://img.shields.io/badge/Website-nakharax.io-29F06A?style=for-the-badge)](https://nakharax.io)
[![Documentation](https://img.shields.io/badge/Documentation-nakharax.io-29F06A?style=for-the-badge)](https://nakharax.io)
[![nakharax](https://img.shields.io/badge/nakharax-GitHub-111318?style=for-the-badge&logo=rust&logoColor=white)](https://github.com/axionaxprotocol/nakharax)

**Community** — Official Discord, X (Twitter), and Telegram links will be listed on **[nakharax.io](https://nakharax.io)** when they go live *(planned Q2 2026)*.

</div>

<br>

<div align="center">

**nakharax.io**
*Last updated: July 4, 2026*

![Contribution grid animation](https://raw.githubusercontent.com/axionaxprotocol/axionaxprotocol/output/github-contribution-grid-snake-dark.svg)

</div>
