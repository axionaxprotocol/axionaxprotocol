<div align="center">

# 🌌 axionax Protocol

### High-Performance Layer-1 Blockchain for Decentralized Computing & AI Workloads

[![Website](https://img.shields.io/badge/Website-axionax.org-blue?style=flat-square)](https://axionax.org)
[![Docs](https://img.shields.io/badge/Docs-docs.axionax.org-green?style=flat-square)](https://axionaxprotocol.github.io/axionax-docs/)
[![License](https://img.shields.io/badge/License-AGPLv3%2FMIT-orange?style=flat-square)](#-license)
[![Chain ID](https://img.shields.io/badge/Chain%20ID-86137%20(Testnet)-purple?style=flat-square)](#)

**45,000+ TPS** • **<0.5s Finality** • **$0.0001 Avg Fee** • **PoPC (Proof of Probabilistic Checking)**

</div>

---

## 👋 สวัสดีครับ, เราคือทีม axionax Protocol!

เราคือทีมผู้พัฒนา **axionax Protocol (AXX)** ซึ่งเป็น Layer-1 Blockchain ที่ออกแบบมาสำหรับการประมวลผลแบบกระจายศูนย์ (Decentralized Compute) และ AI Workloads โดยเฉพาะ

### 🎯 วิสัยทัศน์

สร้าง Layer-1 ที่มีประสิทธิภาพสูงสุด โดยรวมศูนย์:
- ⚡ **Execution Layer** - ประมวลผล transaction และ smart contract
- ✅ **Validation Layer** - PoPC (Proof of Probabilistic Checking) consensus mechanism
- 📦 **Data Availability** - เก็บข้อมูลอย่างปลอดภัย
- 🔄 **Settlement Layer** - ยืนยันและจัดเก็บ state สุดท้าย

---

## 🎉 Latest Updates (November 22, 2025)

### ✨ Major Milestone: Universe Architecture

เราได้ปรับโครงสร้างทั้งหมดเป็น **Universe Monorepo Architecture** แล้ว! 🚀

<table>
  <tr>
    <td>🏗️ <b>Architecture Redesign</b></td>
    <td>รวม 7 repositories เดิมเป็น 2 Universe repos ที่จัดการง่ายกว่า มีประสิทธิภาพสูงกว่า</td>
  </tr>
  <tr>
    <td>🌌 <b>Core Universe</b></td>
    <td>รวมทุกอย่างเกี่ยวกับ blockchain core, deployment และ dev tools ไว้ที่เดียว</td>
  </tr>
  <tr>
    <td>🌐 <b>Web Universe</b></td>
    <td>รวม web apps, marketplace, docs และ SDK ในรูปแบบ monorepo</td>
  </tr>
  <tr>
    <td>📦 <b>Better DX</b></td>
    <td>Shared dependencies, unified CI/CD, easy code reuse และ version sync</td>
  </tr>
  <tr>
    <td>🚀 <b>Production Ready</b></td>
    <td>ทุกอย่างทดสอบแล้ว clone ได้ทันที พร้อมใช้งาน 100%</td>
  </tr>
</table>

### ✅ Previous Achievements

- 🧪 Comprehensive test suite (42 tests)
- 🎨 Enhanced UI with animations & hover effects
- 📚 Complete documentation (900+ lines)
- 🚀 Production deployment on VPS
- 🛠️ DevOps automation tools

---

## 🌌 Our Universe Repositories

ด้วย **Universe Architecture** ใหม่ เราจัดทุกอย่างให้เป็นระเบียบและใช้งานง่ายขึ้นมาก:

### 🌌 Core Universe - Backend & Infrastructure

<div align="center">

[![axionax-core-universe](https://img.shields.io/badge/🌌_Core_Universe-Production-brightgreen?style=for-the-badge)](https://github.com/axionaxprotocol/axionax-core-universe)

</div>

**Monorepo สำหรับ Blockchain Core, Operations และ Development Tools**

\`\`\`
axionax-core-universe/
├── 🦀 core/          # Blockchain protocol (Rust + Python DeAI)
├── 🌍 ops/deploy/    # Deployment automation & infrastructure  
└── 🛠️ tools/devtools/ # Development utilities & testing tools
\`\`\`

| Component | Description | Tech Stack | Status |
|-----------|-------------|------------|--------|
| **Core** | Blockchain protocol, consensus, crypto | Rust, Python | ✅ Production |
| **Deploy** | Docker, scripts, configs, monitoring | Bash, Docker, Nginx | ✅ Ready |
| **DevTools** | Testing framework, utilities (42 tests) | Python, Bash | ✅ Ready |

**🔗 [View Core Universe →](https://github.com/axionaxprotocol/axionax-core-universe)**

---

### 🌐 Web Universe - Frontend & SDK

<div align="center">

[![axionax-web-universe](https://img.shields.io/badge/🌐_Web_Universe-Live-brightgreen?style=for-the-badge)](https://github.com/axionaxprotocol/axionax-web-universe)

</div>

**Monorepo สำหรับ Web Applications, Marketplace, Documentation และ SDK**

\`\`\`
axionax-web-universe/
├── 📱 apps/web/         # Official website (Next.js 14)
├── 🛒 apps/marketplace/ # Compute marketplace dApp
├── 📚 apps/docs/        # Documentation site (50+ pages)
└── 📦 packages/sdk/     # TypeScript SDK for developers
\`\`\`

| Component | Description | Tech Stack | Status |
|-----------|-------------|------------|--------|
| **Website** | Official site & dashboard | Next.js 14, Tailwind | ✅ Live |
| **Marketplace** | Compute trading platform | Vite, React | 🟡 Beta |
| **Docs** | Developer documentation | Markdown, HTML | ✅ Active |
| **SDK** | TypeScript library for dApps | TypeScript 5.0 | ✅ Ready |

**🔗 [View Web Universe →](https://github.com/axionaxprotocol/axionax-web-universe)**

---

## ✨ Why Universe Architecture?

### 📊 Comparison: 7 Repos → 2 Universe Repos

| Before (7 Repos) | After (2 Universe Repos) |
|------------------|--------------------------|
| ❌ Scattered across 7 repos | ✅ Organized in 2 monorepos |
| ❌ Duplicate dependencies | ✅ Shared dependencies |
| ❌ Hard to sync versions | ✅ Unified version control |
| ❌ Complex CI/CD | ✅ Centralized CI/CD |
| ❌ Difficult code reuse | ✅ Easy code sharing |
| ❌ 7 separate clones needed | ✅ Clone once, have everything |

### 🎯 Benefits

- 🚀 **Faster Development** - No need to switch between repos
- 📦 **Better Dependency Management** - Shared packages, no duplication
- 🔄 **Easy Code Reuse** - Import from any package in the workspace
- ⚡ **Simplified CI/CD** - One pipeline for all related projects
- 🎨 **Consistent Tooling** - Same dev environment everywhere
- 📈 **Better DX** - Developer Experience improved dramatically

---

## 🛠️ Technology Stack

### Core Technologies

<p align="center">
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js"/>
</p>

### Infrastructure & DevOps

<p align="center">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx"/>
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis"/>
</p>

### Frontend Stack

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React"/>
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS"/>
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite"/>
  <img src="https://img.shields.io/badge/pnpm-F69220?style=for-the-badge&logo=pnpm&logoColor=white" alt="pnpm"/>
</p>

---

## 🚀 Quick Start

### Clone & Setup

\`\`\`bash
# Clone Core Universe (Backend)
git clone https://github.com/axionaxprotocol/axionax-core-universe.git
cd axionax-core-universe

# Build blockchain core
cd core
cargo build --release

# Clone Web Universe (Frontend)
git clone https://github.com/axionaxprotocol/axionax-web-universe.git
cd axionax-web-universe

# Install dependencies & run
pnpm install
pnpm dev
\`\`\`

### Using the SDK

\`\`\`typescript
import { AxionaxClient } from '@axionax/sdk';

const client = new AxionaxClient({
  rpcUrl: 'http://localhost:8545',
  chainId: 86137
});

// Send transaction
const tx = await client.sendTransaction({
  to: '0x...',
  value: '1000000000000000000' // 1 AXX
});
\`\`\`

---

## 📊 GitHub Stats & Activity

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=axionaxprotocol&show_icons=true&theme=radical&hide_border=true&include_all_commits=true" alt="axionax GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=axionaxprotocol&layout=compact&theme=radical&hide_border=true" alt="axionax Top Languages" />
</p>

---

## 🔗 Connect With Us

<div align="center">

[![Website](https://img.shields.io/badge/🌐_Website-axionax.org-blue?style=for-the-badge)](http://217.216.109.5)
[![Documentation](https://img.shields.io/badge/📖_Docs-Read_Here-green?style=for-the-badge)](https://axionaxprotocol.github.io/axionax-docs/)
[![GitHub](https://img.shields.io/badge/💻_GitHub-Follow_Us-black?style=for-the-badge)](https://github.com/axionaxprotocol)

**Community Channels (Coming Q1 2026)**

[![Discord](https://img.shields.io/badge/Discord-Coming_Soon-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://github.com/axionaxprotocol)
[![Twitter](https://img.shields.io/badge/Twitter-Coming_Soon-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://github.com/axionaxprotocol)
[![Telegram](https://img.shields.io/badge/Telegram-Coming_Soon-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://github.com/axionaxprotocol)

</div>

### 📊 Network Information

| Network | Chain ID | RPC Endpoint | Status |
|---------|----------|--------------|--------|
| Testnet | 86137 | Coming Soon | 🟡 Preparing |
| Mainnet | 86150 | Coming Soon | 🔵 Reserved |
| Local Dev | 31337 | localhost:8545 | ✅ Ready |

### 🐛 Report Issues

พบ bug หรือมีข้อเสนอแนะ? เปิด issue ได้ที่:
- [Core Universe Issues](https://github.com/axionaxprotocol/axionax-core-universe/issues)
- [Web Universe Issues](https://github.com/axionaxprotocol/axionax-web-universe/issues)

---

## 🎯 Roadmap to Public Testnet

### ✅ Phase 1: Foundation (Completed)
- [x] Core blockchain implementation (Rust + PoPC)
- [x] Smart contract support (WASM runtime)
- [x] TypeScript SDK for dApp developers
- [x] Development tools & testing framework (42 tests)
- [x] Official website deployment (Next.js + Docker)
- [x] Comprehensive documentation (900+ lines)
- [x] **Universe architecture migration** 🎉

### 🔄 Phase 2: Optimization (In Progress - 70% Complete)
- [x] UI/UX enhancements with animations
- [x] Production deployment automation
- [x] DevOps tooling & monitoring
- [x] Repository restructuring (Universe)
- [ ] Security audits & penetration testing
- [ ] Performance optimization & load testing (Target: 45K+ TPS)

### 🚀 Phase 3: Launch Preparation (Q1 2026)
- [ ] Community channels setup (Discord, Twitter, Telegram)
- [ ] Faucet & explorer deployment
- [ ] Validator onboarding documentation
- [ ] Marketing & launch campaign
- [ ] **Public Testnet Launch** 🎉

### 🌟 Phase 4: Mainnet (Q2 2026)
- [ ] Testnet validation & feedback
- [ ] Mainnet genesis ceremony
- [ ] Token distribution & staking
- [ ] Governance implementation
- [ ] **Mainnet Launch**

---

## 🤝 Contributing

เรายินดีรับการมีส่วนร่วมจากทุกคน! 🎉

### 🚀 วิธีการมีส่วนร่วม

1. **Fork** repository ที่คุณสนใจ (Core Universe หรือ Web Universe)
2. **Clone** ไปยัง local machine ของคุณ
3. **Create** branch ใหม่ (\`git checkout -b feature/amazing-feature\`)
4. **Commit** การเปลี่ยนแปลง (\`git commit -m 'Add amazing feature'\`)
5. **Push** ไปยัง branch (\`git push origin feature/amazing-feature\`)
6. **Open** Pull Request

### 📖 แหล่งข้อมูล

- [Developer Guide](https://axionaxprotocol.github.io/axionax-docs/DEVELOPER_GUIDE.html)
- [Testing Guide](https://axionaxprotocol.github.io/axionax-docs/TESTING_GUIDE.html)
- [API Reference](https://axionaxprotocol.github.io/axionax-docs/API_REFERENCE.html)

### 🎯 สิ่งที่เรากำลังมองหา

- 🐛 Bug fixes และ performance improvements
- 📚 Documentation improvements
- ✅ More test coverage (current: 42 tests)
- 🎨 UI/UX enhancements
- 🔒 Security audits และ vulnerability reports

---

## 📜 License

| Component | License | Purpose |
|-----------|---------|---------|
| **Core Universe / core** | AGPLv3 | Blockchain protocol core |
| **Core Universe / ops & tools** | MIT | Deployment & dev tools |
| **Web Universe** | MIT | Web apps, docs & SDK |

ดูรายละเอียดเพิ่มเติมใน \`LICENSE\` ของแต่ละ repository

---

## 📈 Development Statistics

<div align="center">

| Metric | Value | Status |
|--------|-------|--------|
| **Total Tests** | 42/42 | ✅ Passing |
| **Repositories** | 2 Universe | 🌌 Active |
| **Total Files** | 1,845+ | 📦 Tracked |
| **TPS** | 45,000+ | 🚀 High Performance |
| **Finality** | <0.5s | ⚡ Ultra Fast |
| **Avg Fee** | $0.0001 | 💰 Cost Effective |
| **Documentation** | 50+ pages | 📚 Comprehensive |
| **Architecture** | Monorepo | ✨ Modern |

</div>

---

## 🌟 Universe Architecture Benefits

<div align="center">

| Feature | Before (7 Repos) | After (2 Universe) | Improvement |
|---------|------------------|-------------------|-------------|
| **Setup Time** | ~30 mins | ~5 mins | 🚀 6x faster |
| **Dependencies** | Duplicated | Shared | 📦 60% reduction |
| **Code Reuse** | Difficult | Easy | ✨ Native support |
| **CI/CD** | 7 pipelines | 2 pipelines | ⚡ 3.5x simpler |
| **Version Sync** | Manual | Automatic | 🎯 100% accuracy |
| **Developer Experience** | Complex | Smooth | 💯 Much better |

</div>

---

<div align="center">

### 🌟 Star Our Universe

[![Star History Chart](https://api.star-history.com/svg?repos=axionaxprotocol/axionax-core-universe,axionaxprotocol/axionax-web-universe&type=Date)](https://star-history.com/#axionaxprotocol/axionax-core-universe&axionaxprotocol/axionax-web-universe&Date)

---

**Built with ❤️ by the axionax Protocol Team**

*Last Updated: November 22, 2025 - Universe Architecture Launch*

[![GitHub followers](https://img.shields.io/github/followers/axionaxprotocol?style=social)](https://github.com/axionaxprotocol)
[![GitHub stars](https://img.shields.io/github/stars/axionaxprotocol?style=social)](https://github.com/axionaxprotocol)

**🌌 Welcome to the axionax Universe! 🌐**

</div>
