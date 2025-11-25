<div align="center">

# 🌌 axionax Protocol

[![Documentation](https://img.shields.io/badge/📚_Documentation-axionax--docs-10B981?style=for-the-badge&logo=readthedocs&logoColor=white)](https://axionaxprotocol.github.io/axionax-docs/)
[![License](https://img.shields.io/badge/⚖️_License-AGPLv3/MIT-F59E0B?style=for-the-badge)](#-license)
[![Chain ID](https://img.shields.io/badge/🔗_Chain_ID-86137-8B5CF6?style=for-the-badge)](#)

**High-Performance Layer-1 Blockchain for Decentralized Computing & AI Workloads**

<br>

| ⚡ **TPS** | ⏱️ **Finality** | 💰 **Avg Fee** | 🔐 **Consensus** | 🔗 **Chain ID** |
|:---:|:---:|:---:|:---:|:---:|
| 45,000+ | <0.5s | $0.0001 | PoPC | 86137 |

</div>

---

## 🎯 Overview

**axionax Protocol (AXX)** คือ Layer-1 blockchain ที่ออกแบบมาเพื่อรองรับ decentralized computing และ AI workloads โดยรวมทั้ง 4 layers หลักไว้ในที่เดียว:

| Layer | Description | Status |
|-------|-------------|:------:|
| ⚡ **Execution** | Transaction processing & smart contract execution | ✅ |
| ✅ **Validation** | PoPC (Proof of Probabilistic Checking) consensus | ✅ |
| 📦 **Data Availability** | Secure, accessible data storage layer | ✅ |
| 🔄 **Settlement** | Final state confirmation & persistence | ✅ |

---

## 🌌 Universe Architecture

เราใช้ **Universe Monorepo Architecture** - รวม 7 repositories เดิมเป็น 2 monorepos ที่มีประสิทธิภาพสูงกว่า

<div align="center">

| Metric | Before | After | Improvement |
|--------|:------:|:-----:|:-----------:|
| Setup Time | ~30 mins | ~5 mins | 🚀 6x faster |
| Dependencies | Duplicated | Shared | 📦 60% less |
| CI/CD Pipelines | 7 | 2 | ⚡ 3.5x simpler |
| Code Reuse | Difficult | Native | ✨ Easy |

</div>

### 🌌 Core Universe - Backend & Infrastructure

[![Core Universe](https://img.shields.io/badge/🌌_Core_Universe-Production-10B981?style=for-the-badge&logo=rust)](https://github.com/axionaxprotocol/axionax-core-universe)
[![Stars](https://img.shields.io/github/stars/axionaxprotocol/axionax-core-universe?style=flat-square)](https://github.com/axionaxprotocol/axionax-core-universe/stargazers)

Blockchain core, deployment tools, และ testing framework (42 tests)

```
axionax-core-universe/
├── core/          # Rust blockchain + PoPC consensus + WASM runtime
├── ops/deploy/    # Docker, Nginx, monitoring (Prometheus + Grafana)
└── tools/devtools/# Testing framework & build utilities
```

**Tech Stack:** Rust, Python, Docker, Bash  
**🔗 [View Repository →](https://github.com/axionaxprotocol/axionax-core-universe)**

### 🌐 Web Universe - Frontend & SDK

[![Web Universe](https://img.shields.io/badge/🌐_Web_Universe-Live-3B82F6?style=for-the-badge&logo=react)](https://github.com/axionaxprotocol/axionax-web-universe)
[![Stars](https://img.shields.io/github/stars/axionaxprotocol/axionax-web-universe?style=flat-square)](https://github.com/axionaxprotocol/axionax-web-universe/stargazers)

Web applications, marketplace, documentation, และ TypeScript SDK

```
axionax-web-universe/
├── apps/
│   ├── web/         # Next.js 14 website
│   ├── marketplace/ # Vite + React marketplace dApp
│   └── docs/        # 50+ documentation pages
└── packages/sdk/    # TypeScript SDK for dApp developers
```

**Tech Stack:** Next.js 14, React, TypeScript, Tailwind CSS, pnpm  
**🔗 [View Repository →](https://github.com/axionaxprotocol/axionax-web-universe)**

---

## 🚀 Quick Start

### Clone & Build

```bash
# Core Universe - Backend
git clone https://github.com/axionaxprotocol/axionax-core-universe.git
cd axionax-core-universe/core
cargo build --release

# Web Universe - Frontend
git clone https://github.com/axionaxprotocol/axionax-web-universe.git
cd axionax-web-universe
pnpm install && pnpm dev
```

### Using the SDK

```bash
npm install @axionax/sdk
```

```typescript
import { AxionaxClient } from '@axionax/sdk';

const client = new AxionaxClient({
  rpcUrl: 'http://localhost:8545',
  chainId: 86137
});

// Send transaction
const tx = await client.sendTransaction({
  to: '0x742d35Cc6634C0532925a3b844Bc9e7595f0bEb',
  value: '1000000000000000000' // 1 AXX
});

console.log('Transaction hash:', tx.hash);
```

---

## 🛠️ Technology Stack

<p align="center">
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx"/>
</p>

---

## 🔗 Network Information

| Network | Chain ID | RPC Endpoint | Status |
|---------|:--------:|--------------|:------:|
| **Testnet** | 86137 | Coming Soon | 🟡 Preparing |
| **Mainnet** | 86150 | Coming Soon | 🔵 Reserved |
| **Local Dev** | 31337 | localhost:8545 | ✅ Ready |

---

## 🗺️ Roadmap

<table>
<tr>
<th width="25%">Phase</th>
<th width="50%">Key Deliverables</th>
<th width="25%">Status</th>
</tr>
<tr>
<td><b>Phase 1</b><br><sub>Foundation</sub></td>
<td>
• Core blockchain (Rust + PoPC)<br>
• Smart contracts (WASM)<br>
• TypeScript SDK<br>
• Testing framework (42 tests)<br>
• Documentation (50+ pages)<br>
• Universe architecture
</td>
<td align="center">
✅ <b>Complete</b><br>
<sub>100%</sub>
</td>
</tr>
<tr>
<td><b>Phase 2</b><br><sub>Optimization</sub></td>
<td>
• UI/UX enhancements<br>
• Production deployment<br>
• DevOps automation<br>
• Security audits<br>
• Performance testing (45K+ TPS)
</td>
<td align="center">
🟡 <b>In Progress</b><br>
<sub>70%</sub>
</td>
</tr>
<tr>
<td><b>Phase 3</b><br><sub>Launch Prep</sub></td>
<td>
• Community channels setup<br>
• Faucet & explorer<br>
• Validator documentation<br>
• Marketing campaign<br>
• <b>Public Testnet Launch</b>
</td>
<td align="center">
🔵 <b>Q1 2026</b><br>
<sub>Planned</sub>
</td>
</tr>
<tr>
<td><b>Phase 4</b><br><sub>Mainnet</sub></td>
<td>
• Testnet validation<br>
• Genesis ceremony<br>
• Token distribution<br>
• Governance<br>
• <b>Mainnet Launch</b>
</td>
<td align="center">
🟣 <b>Q2 2026</b><br>
<sub>Target</sub>
</td>
</tr>
</table>

---

## 📊 Statistics

<div align="center">

| Metric | Value |
|--------|:-----:|
| **Total Tests** | 42/42 ✅ |
| **Documentation Pages** | 50+ |
| **Total Files** | 1,845+ |
| **Active Repositories** | 2 Universe Repos |
| **Transaction Throughput** | 45,000+ TPS |
| **Block Finality** | <0.5 seconds |
| **Average Fee** | $0.0001 |

</div>

---

## 🤝 Contributing

เรายินดีรับ contributions จากทุกคน!

### How to Contribute

1. Fork repository ที่สนใจ ([Core Universe](https://github.com/axionaxprotocol/axionax-core-universe) / [Web Universe](https://github.com/axionaxprotocol/axionax-web-universe))
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

### Developer Resources

- [Developer Guide](https://axionaxprotocol.github.io/axionax-docs/DEVELOPER_GUIDE.html)
- [Testing Guide](https://axionaxprotocol.github.io/axionax-docs/TESTING_GUIDE.html)
- [API Reference](https://axionaxprotocol.github.io/axionax-docs/API_REFERENCE.html)

### We're Looking For

- 🐛 Bug fixes & performance improvements
- 📚 Documentation enhancements
- ✅ Increased test coverage
- 🎨 UI/UX improvements
- 🔒 Security audits & vulnerability reports

---

## 📋 License

| Component | License | Description |
|-----------|:-------:|-------------|
| **Core Universe / core** | AGPLv3 | Blockchain protocol core |
| **Core Universe / ops & tools** | MIT | Deployment & dev tools |
| **Web Universe** | MIT | Web apps, docs & SDK |

See individual repository `LICENSE` files for details.

---

## 📞 Connect

<div align="center">

[![Documentation](https://img.shields.io/badge/📖_Documentation-GitHub_Pages-green?style=for-the-badge)](https://axionaxprotocol.github.io/axionax-docs/)
[![GitHub](https://img.shields.io/badge/💻_GitHub-axionaxprotocol-black?style=for-the-badge)](https://github.com/axionaxprotocol)
[![Core Universe](https://img.shields.io/badge/🌌_Core_Universe-Repository-blue?style=for-the-badge)](https://github.com/axionaxprotocol/axionax-core-universe)

**Community Channels** *(Coming Q1 2026)*

[![Discord](https://img.shields.io/badge/Discord-Coming_Soon-7289DA?style=flat-square&logo=discord)](https://github.com/axionaxprotocol)
[![Twitter](https://img.shields.io/badge/Twitter-Coming_Soon-1DA1F2?style=flat-square&logo=twitter)](https://github.com/axionaxprotocol)
[![Telegram](https://img.shields.io/badge/Telegram-Coming_Soon-2CA5E0?style=flat-square&logo=telegram)](https://github.com/axionaxprotocol)

</div>

### Report Issues

- [Core Universe Issues](https://github.com/axionaxprotocol/axionax-core-universe/issues)
- [Web Universe Issues](https://github.com/axionaxprotocol/axionax-web-universe/issues)

---

<div align="center">

**Built with ❤️ by the axionax Protocol Team**

*Last Updated: November 25, 2025*

[![GitHub followers](https://img.shields.io/github/followers/axionaxprotocol?style=social)](https://github.com/axionaxprotocol)
[![GitHub stars](https://img.shields.io/github/stars/axionaxprotocol?style=social)](https://github.com/axionaxprotocol)

**🌌 Welcome to the axionax Universe! 🌐**

</div>
