<div align="center">

<img src="assets/axionax_brand.jpg" width="200" alt="Axionax brand logo" />
&nbsp;&nbsp;&nbsp;&nbsp;
<img src="assets/axx_token.jpg" width="200" alt="AXX token logo" />

# Axionax Protocol

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=1000&color=6366F1&center=true&vCenter=true&width=600&lines=High-performance+Layer-1+blockchain;45%2C000%2B+TPS+%E2%80%A2+Sub-0.5s+finality;Decentralized+computing+and+AI+workloads" alt="Axionax Protocol — headline" />

[![Documentation](https://img.shields.io/badge/Documentation-axionax.org-10B981?style=for-the-badge&logo=readthedocs&logoColor=white)](https://axionax.org)
[![License](https://img.shields.io/badge/License-AGPLv3%2FMIT-F59E0B?style=for-the-badge)](#license)
[![Chain ID](https://img.shields.io/badge/Chain_ID-86137-8B5CF6?style=for-the-badge)](#network-information)

**Layer-1 blockchain for decentralized computing and AI workloads**

This repository contains the **organization profile** for Axionax Protocol on GitHub (overview and links). Protocol and application source code live in the [Core](#core-universe--protocol-and-infrastructure) and [Web](#web-universe--applications-and-sdk) Universe repositories.

| Throughput | Finality | Consensus |
| :---: | :---: | :--- |
| 45,000+ TPS (target architecture) | Sub-0.5s | PoPC (Proof of Probabilistic Checking) |

</div>

---

## Table of contents

- [Overview](#overview)
- [Key features](#key-features)
- [Ecosystem repositories](#ecosystem-repositories)
- [Quick start](#quick-start)
- [Network information](#network-information)
- [Roadmap](#roadmap)
- [Organization activity](#organization-activity)
- [Contributing](#contributing)
- [License](#license)
- [Connect and support](#connect-and-support)

---

## Overview

**Axionax Protocol (AXX)** is a Layer-1 network built to run high-throughput decentralized computing and AI-oriented workloads. Execution, validation, data availability, and settlement are integrated in a single stack so builders can deploy without stitching together external modular services.

The design emphasizes performance, security, and a straightforward path for operators and application developers.

---

## Key features

| Area | Summary |
| :--- | :--- |
| **Throughput** | Architecture targets **45,000+ TPS** with **sub-0.5s** finality for latency-sensitive and compute-heavy use cases. |
| **Consensus** | **Proof of Probabilistic Checking (PoPC)** supports decentralized validation with efficient block processing. |
| **Data availability** | Built-in data availability layer reduces dependence on third-party DA networks. |
| **Compute and AI** | Primitives and tooling aimed at decentralized inference, training workflows, and general compute on-chain and adjacent services. |

---

## Ecosystem repositories

Work is organized in two monorepos (**Universe** architecture): Core (protocol and operations) and Web (applications and SDK).

### Core Universe — protocol and infrastructure

[![Core Universe](https://img.shields.io/badge/Core_Universe-Production-10B981?style=for-the-badge&logo=rust)](https://github.com/axionaxprotocol/axionax-core-universe)
[![Stars](https://img.shields.io/github/stars/axionaxprotocol/axionax-core-universe?style=flat-square&logo=github)](https://github.com/axionaxprotocol/axionax-core-universe/stargazers)

- **Stack:** Rust, Python, Docker, shell automation  
- **Scope:** Blockchain node, PoPC consensus, WASM runtime, deployment and testing tooling  
- **[Repository →](https://github.com/axionaxprotocol/axionax-core-universe)**

### Web Universe — applications and SDK

[![Web Universe](https://img.shields.io/badge/Web_Universe-Live-3B82F6?style=for-the-badge&logo=react)](https://github.com/axionaxprotocol/axionax-web-universe)
[![Stars](https://img.shields.io/github/stars/axionaxprotocol/axionax-web-universe?style=flat-square&logo=github)](https://github.com/axionaxprotocol/axionax-web-universe/stargazers)

- **Stack:** Next.js 14, React, TypeScript, Tailwind CSS, pnpm  
- **Scope:** Web portals, marketplace dApp, `@axionax/sdk`, protocol-facing documentation  
- **[Repository →](https://github.com/axionaxprotocol/axionax-web-universe)**

---

## Quick start

### Node operators and core developers

```bash
git clone https://github.com/axionaxprotocol/axionax-core-universe.git
cd axionax-core-universe/core
cargo build --release
```

### dApp and web developers

```bash
git clone https://github.com/axionaxprotocol/axionax-web-universe.git
cd axionax-web-universe
pnpm install
pnpm dev
```

### SDK (npm)

```bash
npm install @axionax/sdk
```

```typescript
import { AxionaxClient } from '@axionax/sdk';

const client = new AxionaxClient({
  rpcUrl: 'http://localhost:8545',
  chainId: 31337, // local dev; use 86137 for public testnet
});

const tx = await client.sendTransaction({
  to: '0x742d35Cc6634C0532925a3b844Bc9e7595f0bEb',
  value: '1000000000000000000', // 1 AXX
});

console.log('Transaction hash:', tx.hash);
```

---

## Network information

| Network | Chain ID | RPC | Status |
| :--- | :---: | :--- | :---: |
| Local development | `31337` | `http://localhost:8545` | Available |
| Testnet | `86137` | See [Core Universe README — testnet](https://github.com/axionaxprotocol/axionax-core-universe#current-network-testnet) | Active |
| Mainnet | `86150` | — | In preparation |

---

## Roadmap

| Phase | Focus | Status |
| :--- | :--- | :---: |
| **1 — Foundation** | Core chain (Rust + PoPC), smart contracts (WASM), TypeScript SDK, Universe layout | Complete |
| **2 — Optimization** | UX, production deployment, DevOps automation, security reviews, benchmark validation | ~95% |
| **3 — Launch preparation** | Whitepaper and public docs, faucet and explorer, VPS deployment, validator tooling, public testnet | ~50% |
| **4 — Mainnet** | Genesis export, state validation, RPC hardening, distribution, mainnet launch | ~20% |

Percentages are planning indicators; see Core and Web repositories for the latest delivery state.

---

## Organization activity

<div align="center">

[![GitHub organization overview](https://github-readme-stats.vercel.app/api?username=axionaxprotocol&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=6366F1&icon_color=10B981&text_color=FFFFFF)](https://github.com/axionaxprotocol)

</div>

*Widget by [github-readme-stats](https://github.com/anuraghazra/github-readme-stats); figures are indicative.*

---

## Contributing

1. Fork the relevant repository ([Core](https://github.com/axionaxprotocol/axionax-core-universe) or [Web](https://github.com/axionaxprotocol/axionax-web-universe)).  
2. Create a branch (`git switch -c feature/your-change`).  
3. Commit with clear messages (e.g. `feat:`, `fix:`, `docs:`).  
4. Push and open a pull request.

Guidelines and detailed processes are published on **[axionax.org](https://axionax.org)**.

---

## License

Licensing varies by component. Refer to each repository:

- **Core Universe:** `core/` — AGPLv3; `ops/` and `tools/` — MIT. See [Core Universe — License](https://github.com/axionaxprotocol/axionax-core-universe#license).  
- **Web Universe:** MIT. See [Web Universe LICENSE](https://github.com/axionaxprotocol/axionax-web-universe/blob/main/LICENSE).

---

## Connect and support

<div align="center">

[![Website](https://img.shields.io/badge/Website-axionax.org-10B981?style=for-the-badge)](https://axionax.org)
[![Documentation](https://img.shields.io/badge/Documentation-axionax.org-green?style=for-the-badge)](https://axionax.org)
[![Core Universe](https://img.shields.io/badge/Core_Universe-GitHub-blue?style=for-the-badge)](https://github.com/axionaxprotocol/axionax-core-universe)
[![Web Universe](https://img.shields.io/badge/Web_Universe-GitHub-blue?style=for-the-badge)](https://github.com/axionaxprotocol/axionax-web-universe)

**Community** — Official Discord, X (Twitter), and Telegram links will be listed on **[axionax.org](https://axionax.org)** when they go live *(planned Q2 2026)*.

</div>

<br>

<div align="center">

**Axionax Protocol**  
*Last updated: April 1, 2026*

![Contribution grid animation](https://raw.githubusercontent.com/axionaxprotocol/axionaxprotocol/output/github-contribution-grid-snake-dark.svg)

</div>
