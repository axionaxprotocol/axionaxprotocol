<div align="center">

<img src="assets/nakharax_brand.svg" width="400" alt="nakharax.io" />

<br />

**Cheap, accessible compute for everyone.**

A paid, verifiable grid for parallel science and AI — powered by Proof of Probabilistic Checking.

<br />

[![Testnet](https://img.shields.io/badge/Testnet-86137-29F06A?style=flat-square)](#network)
[![Rust](https://img.shields.io/badge/Rust-1.81%2B-111318?style=flat-square&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![License](https://img.shields.io/badge/AGPL--3.0_/_MIT-FF7A1A?style=flat-square)](LICENSE)
[![nakharax.io](https://img.shields.io/badge/nakharax.io-29F06A?style=flat-square&logo=googlechrome&logoColor=white)](https://nakharax.io)

</div>

---

## What is nakharax.io?

**nakharax.io** is a decentralized compute network where anyone with a PC, server, or Raspberry Pi can lend spare cycles and earn **NAK** — and researchers who could never afford a supercomputer can rent thousands of idle machines to run simulations, batch inference, and parameter sweeps.

The blockchain is the **trust and settlement rail**: job escrow, payment in NAK, and reputation. Verification is handled by **Proof of Probabilistic Checking (PoPC)**, which validates compute results from untrusted workers in microseconds.

> Think: a modern, paid [BOINC](https://boinc.berkeley.edu/) / [Folding@home](https://foldingathome.org/) — with verification and a marketplace.

<sub>Formerly **Axionax Protocol** (AXX). See [rebrand status](#rebrand-status).</sub>

---

## Why it matters

| Problem | nakharax.io |
| :--- | :--- |
| Cloud compute is expensive and centralized | Workers earn NAK; requesters pay less than AWS/GCP |
| Volunteer grids have no incentive layer | NAK payment makes contribution sustainable |
| You can't trust a stranger's compute result | PoPC verifies 1,000 samples in **~437 µs** |
| AI inference on foreign servers breaks data sovereignty | On-device / in-country private inference (PDPA/GDPR-ready) |

---

## Architecture

One monorepo. Strict **Web ↔ Core** boundary — they communicate only via JSON-RPC on port `8545`.

```
nakharax/
├── apps/
│   ├── web/                 Next.js dApp + compute marketplace
│   └── os-dashboard/        Self-hosted node OS dashboard
├── services/
│   └── core/                Rust blockchain node + Python DeAI worker
├── packages/
│   └── sdk/                 @nakharax/sdk — typed RPC client (TypeScript)
├── docs/                    Protocol docs, audits, RFCs
└── scripts/                 Ops tooling
```

| Component | Stack | Status |
| :--- | :--- | :---: |
| PoPC consensus engine | Rust | Shipping |
| Full node / block production | Rust | Shipping |
| Staking & governance | Rust | Shipping |
| JSON-RPC (ETH-compatible + custom) | Rust | Shipping |
| DeAI worker (AI inference) | Python + PyTorch | Shipping |
| TypeScript SDK | TypeScript | Shipping |
| Compute marketplace (on-chain escrow) | Solidity + Python | In progress |
| Data availability (erasure coding) | Rust | In progress |

<sub>Full subsystem status: [`docs/REALITY_MAP.md`](https://github.com/axionaxprotocol/nakharax/blob/main/docs/REALITY_MAP.md)</sub>

---

## Network

### Testnet — Chain ID `86137`

| Node | Location | Role | RPC |
| :--- | :---: | :--- | :--- |
| Validator #1 | EU | Validator + RPC + Nakharax OS | `https://app.nakharax.io` |
| Validator #2 | AU | Validator + chain services | `https://rpc.nakharax.io` |

Public endpoints: **RPC** `https://rpc.nakharax.io` · **Explorer** · **Faucet** · **API**

| Constant | Value |
| :--- | :--- |
| Mainnet Chain ID | `86150` |
| RPC port | `8545` (HTTP) · `8546` (WS) |
| P2P port | `30303` (TCP + QUIC) |
| Block reward | `1.0 NAK` |
| Min validator stake | `10,000 NAK` |

---

## Hardware requirements

| Role | CPU | RAM | Disk | Network |
| :--- | :--- | :--- | :--- | :--- |
| **Worker** (PC / server) | 4 cores | 8 GB | 100 GB SSD | 50 Mbps |
| **Validator** (full node) | 8 cores | 16 GB | 500 GB NVMe | 100 Mbps, static IP |
| **Monolith Scout** (Hailo) | Pi 5 + Hailo-8 NPU | 8 GB | 256 GB SSD | 50 Mbps |
| **HYDRA** (Sentinel + Worker) | 12 cores | 32 GB | 1 TB NVMe | 100 Mbps |

---

## Quick start

### Run a node (Docker)

```bash
git clone https://github.com/axionaxprotocol/nakharax.git
cd nakharax/services/core
cp .env.example .env
docker compose -f docker-compose.dev.yml up -d --build

# Verify
curl -sX POST http://localhost:8545 \
  -H 'Content-Type: application/json' \
  -d '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1}'
```

### Join the network (bare metal)

```bash
cd nakharax/services/core
python3 scripts/update-node.py       # install toolchains + system check
python3 scripts/join-nakharax.py     # pick: Worker / Monolith Scout / HYDRA
```

### Use the SDK

```bash
npm install @nakharax/sdk
```

```typescript
import { getBlockNumber, isReachable, DEFAULT_NODES } from '@nakharax/sdk';

const rpc = DEFAULT_NODES[0].url;

if (await isReachable(rpc)) {
  const block = await getBlockNumber(rpc);
  console.log('Latest block:', block.ok ? block.data : block.error.message);
}
```

---

## Measured performance

Real numbers from `cargo bench` — component-level, not end-to-end TPS. System throughput depends on networking, mempool, and block assembly.

| Operation | Median |
| :--- | :--- |
| PoPC `generate_challenge` (1,000 samples) | ~437 µs |
| Merkle `verify_proof` | ~10.9 ns |
| `ed25519_verify` | ~35.6 µs (~28k/core/s) |
| `blake2s_256` hash | ~129 ns |

<sub>Block time: **5 seconds** (`configs/protocol.mainnet.yaml`). Test suite: **~360 tests passing** across 19 Rust crates + Python DeAI.</sub>

---

## Roadmap

| Phase | Focus | Status |
| :--- | :--- | :---: |
| **1 — Foundation** | Rust blockchain + PoPC, WASM contracts, TypeScript SDK, monorepo | **Done** |
| **2 — Hardening** | Security audits, DevOps, production deployment, UI/UX | **Done** |
| **3 — Launch prep** | Rebrand (Axionax → nakharax.io), public testnet (EU + AU validators), faucet, explorer | **In progress** |
| **4 — Mainnet** | Genesis ceremony, NAK token distribution, mainnet launch | **Planned** |

---

## Rebrand status

The project was renamed **Axionax Protocol → nakharax.io** in June 2026. In-repo rename is complete and verified (all workspace tests green).

| | Before | After |
| :--- | :--- | :--- |
| Name | Axionax Protocol | nakharax.io |
| Token | AXX | NAK |
| Domain | axionax.org | nakharax.io |
| Packages | `@axionax/sdk` | `@nakharax/sdk` |
| Env vars | `AXIONAX_*` | `NAKHARAX_*` |

<sub>Full migration runbook: [`docs/REBRAND_MIGRATION.md`](https://github.com/axionaxprotocol/nakharax/blob/main/docs/REBRAND_MIGRATION.md)</sub>

---

## Repository structure

This repository (`axionaxprotocol/axionaxprotocol`) is the **GitHub organization profile** — overview and navigation only. A [Git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) pins a snapshot of the upstream monorepo:

```bash
# Clone with submodule
git clone --recurse-submodules https://github.com/axionaxprotocol/axionaxprotocol.git

# Or init after clone
git submodule update --init --recursive

# Advance pointer to latest upstream
git submodule update --remote --merge
```

All development happens upstream at [**axionaxprotocol/nakharax**](https://github.com/axionaxprotocol/nakharax).

---

## Contributing

1. Fork [axionaxprotocol/nakharax](https://github.com/axionaxprotocol/nakharax)
2. Pick the right sub-tree: `apps/` for UI, `services/core/` for chain/AI
3. Match existing style — `cargo clippy` and `pnpm lint` must be clean
4. Commit: `<type>(<scope>): <description>` — see [CONTRIBUTING.md](https://github.com/axionaxprotocol/nakharax/blob/main/docs/CONTRIBUTING.md)
5. Open a pull request

---

## License

- **This repository:** MIT — see [LICENSE](LICENSE)
- **Upstream:** AGPL-3.0 (default) or MIT for explicit downstream agreements — see each sub-tree

---

<div align="center">

[![Website](https://img.shields.io/badge/nakharax.io-29F06A?style=for-the-badge&logo=googlechrome&logoColor=white)](https://nakharax.io)
[![GitHub](https://img.shields.io/badge/Source-111318?style=for-the-badge&logo=github&logoColor=white)](https://github.com/axionaxprotocol/nakharax)

<sub>Last updated: July 2026</sub>

</div>
