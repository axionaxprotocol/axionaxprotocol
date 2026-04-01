<div align="center">

<img src="assets/axionax_brand.jpg" width="200" alt="Axionax brand logo" />
&nbsp;&nbsp;&nbsp;&nbsp;
<img src="assets/axx_token.jpg" width="200" alt="AXX token logo" />

# Axionax Protocol

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=1000&color=6366F1&center=true&vCenter=true&width=600&lines=High-performance+Layer-1+blockchain;45%2C000%2B+TPS+%E2%80%A2+Sub-0.5s+finality;Decentralized+computing+and+AI+workloads" alt="Axionax Protocol — headline" />

[![Documentation](https://img.shields.io/badge/📚_Documentation-axionax.org-10B981?style=for-the-badge&logo=readthedocs&logoColor=white)](https://axionax.org)
[![License](https://img.shields.io/badge/⚖️_License-MIT-F59E0B?style=for-the-badge)](LICENSE)
[![Chain ID](https://img.shields.io/badge/🔗_Chain_ID-86137-8B5CF6?style=for-the-badge)](#)

**Layer-1 blockchain for decentralized computing and AI workloads**

| Throughput | Finality | Consensus |
| :---: | :---: | :--- |
| 45,000+ TPS (target architecture) | Sub-0.5s | PoPC (Proof of Probabilistic Checking) |

</div>

---

## 📖 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [The axionax Universe](#-the-axionax-universe)
- [Quick Start](#-quick-start)
- [Network Information](#-network-information)
- [Roadmap](#%EF%B8%8F-roadmap)
- [Contributing](#-contributing)
- [License](#-license)

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
  chainId: 86137,
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
| **Phase 1: Foundation** | Core blockchain (Rust + PoPC), Smart contracts (WASM), TypeScript SDK, Universe architecture | ✅ **100%** |
| **Phase 2: Optimization** | UI/UX enhancements, Production deployment, DevOps automation, Security audits, 45K+ TPS testing | ✅ **100%** |
| **Phase 3: Launch Prep** | Community channels, Faucet & Explorer, Validator documentation, Public Testnet Launch | 🔄 **In Progress** |
| **Phase 4: Mainnet** | Testnet validation, Genesis ceremony, Token distribution, Mainnet Launch | 🎯 **Q2 2026** |

---

## 🤝 Contributing

We welcome contributions from everyone! Whether it's reporting bugs, improving documentation, or contributing code, your help is appreciated.

1. Fork the relevant repository ([Core](https://github.com/axionaxprotocol/axionax-core-universe) or [Web](https://github.com/axionaxprotocol/axionax-web-universe)).  
2. Create a branch (`git checkout -b feature/your-change`).  
3. Commit with clear messages (e.g. `feat:`, `fix:`, `docs:`).  
4. Push and open a pull request.

Guidelines and detailed processes are published on **[axionax.org](https://axionax.org)**.

---

## License

Licensing varies by component. Refer to each repository:

- **This Repository:** MIT. See [LICENSE](LICENSE).
- **Core Universe:** `core/` → AGPLv3; `ops/` and `tools/` → MIT. See [Core Universe → License](https://github.com/axionaxprotocol/axionax-core-universe#license).
- **Web Universe:** MIT. See [Web Universe LICENSE](https://github.com/axionaxprotocol/axionax-web-universe/blob/main/LICENSE).

---

## Connect and support

<div align="center">

[![Website](https://img.shields.io/badge/🌐_Website-axionax.org-10B981?style=for-the-badge)](https://axionax.org)
[![Documentation](https://img.shields.io/badge/📖_Docs-axionax.org-6366F1?style=for-the-badge)](https://axionax.org)
[![Core Universe](https://img.shields.io/badge/🌌_Core-Repository-3B82F6?style=for-the-badge&logo=rust&logoColor=white)](https://github.com/axionaxprotocol/axionax-core-universe)
[![Web Universe](https://img.shields.io/badge/🌐_Web-Repository-3B82F6?style=for-the-badge&logo=react&logoColor=white)](https://github.com/axionaxprotocol/axionax-web-universe)

</div>

<br>

<div align="center">

**Built with ❤️ by the axionax Protocol Team**

</div>
