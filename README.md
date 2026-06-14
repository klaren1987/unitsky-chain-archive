# Unitsky String Technologies

**EVM-compatible blockchain · Chain ID 778889 · Native token UST**

[![Chain ID](https://img.shields.io/badge/Chain%20ID-778889-blue)](https://chainlist.org)
[![RPC](https://img.shields.io/badge/RPC-HTTPS-green)](https://147-45-143-23.sslip.io/rpc)
[![Explorer](https://img.shields.io/badge/Explorer-online-brightgreen)](https://147-45-143-23.sslip.io)
[![CI](https://github.com/klaren1987/unitsky-chain/actions/workflows/rpc-health.yml/badge.svg)](https://github.com/klaren1987/unitsky-chain/actions/workflows/rpc-health.yml)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

---

## Network

| Parameter | Value |
|-----------|-------|
| **Chain ID** | `778889` (`0xBE289`) |
| **Native Token** | **UST** |
| **Block Time** | ~5 seconds |
| **Consensus** | Clique PoA |
| **Mining** | PoW smart contract |
| **HTTPS RPC** | https://147-45-143-23.sslip.io/rpc |
| **WebSocket** | wss://147-45-143-23.sslip.io/ws |
| **Explorer** | https://147-45-143-23.sslip.io |

---

## Add to MetaMask

**One click:** [Add via Chainlist](https://chainlist.org/?search=778889)

**Manual:**

| Field | Value |
|-------|-------|
| Network Name | `Unitsky String Technologies` |
| RPC URL | `https://147-45-143-23.sslip.io/rpc` |
| Chain ID | `778889` |
| Currency Symbol | `UST` |
| Block Explorer | `https://147-45-143-23.sslip.io` |

---

## Mining (earn free UST)

UST tokens are distributed **only** through mining — no pre-mine, no ICO, no team allocation.

```bash
git clone https://github.com/klaren1987/unitsky-chain.git
cd unitsky-chain
pip install -r requirements.txt
cp .env.miner.example .env.miner
# Edit .env.miner: set MINER_ADDRESS to your wallet
python miner/usst_miner.py
```

**GPU mining** (NVIDIA CUDA): ~590 MH/s on RTX 4060  
**CPU mining**: works on any machine

Mining algorithm: `keccak256(miner_address, nonce, work_block)`  
Contract: [`contracts/USSTMine.sol`](contracts/USSTMine.sol)

---

## DEX — Swap UST ↔ USDT

A **Uniswap V2** fork is live on chain 778889.

| Contract | Address |
|----------|---------|
| **DEX UI** | https://147-45-143-23.sslip.io/dex |
| UniswapV2Factory | `0xbFAe9F1DF838F63eBedB29f54C7c9FA25c16fe06` |
| UniswapV2Router02 | `0xaD30634417751B8088a5ca3F812d74c3c2331e85` |
| WUST (Wrapped UST) | `0x63787dE7FEb0beB1b545eB564794b5bCEEB317CF` |
| USDT (fixed supply) | `0xb7cBe6aFbF7f21798f54A44ca84Cda2D888179ec` |
| UST/USDT Pair | `0x11e5b927937267F625084CFaF52917E338e2AF44` |

Init code hash: `0x96e8ac4277198ff8b6f785478aa9a39f403cb768dd02cbee326c3e7da348845f`

Price: **1 UST = 0.10 USDT** · Liquidity: ~51 000 UST + 5 100 USDT

---

## Registry Status

| Registry | Status | Link |
|----------|--------|------|
| ethereum-lists/chains | ✅ Merged | [PR #8418](https://github.com/ethereum-lists/chains/pull/8418) |
| DefiLlama Chainlist | ✅ Merged | [PR #2830](https://github.com/DefiLlama/chainlist/pull/2830) |
| wevm/viem | ⏳ Pending review | [PR #4721](https://github.com/wevm/viem/pull/4721) |
| blockscout/chainscout | ⏳ Pending review | [PR #242](https://github.com/blockscout/chainscout/pull/242) |
| GeckoTerminal | ⏳ Submitted | Network + DEX listing request sent |

Auto-discoverable in **MetaMask**, **WalletConnect**, **Rainbow**, **wagmi**, **chainid.network**

---

## Repository Structure

```
.
├── chain/              Genesis block configuration
├── config/
│   ├── caddy/          Caddyfile (HTTPS reverse proxy)
│   ├── explorer/       Custom block explorer (static SPA)
│   └── wireguard/      WireGuard VPN config examples
├── contracts/          USSTMine.sol — PoW mining contract
├── docs/
│   ├── whitepaper.md   Full technical documentation
│   └── announcements.md  Community post templates
├── miner/              Python miner (GPU + CPU)
├── scripts/            Setup and maintenance scripts
├── docker-compose*.yml Container orchestration
└── .env.miner.example  Miner configuration template
```

---

---

## Documentation

- [Whitepaper](docs/whitepaper.md) — full technical docs
- [Announcements](docs/announcements.md) — ready-to-post community templates
- [Contributing](CONTRIBUTING.md) — how to contribute

---

## Roadmap

- [x] Mainnet launch
- [x] Public HTTPS RPC + block explorer
- [x] GPU miner (NVIDIA CUDA ~590 MH/s, double-buffer optimized)
- [x] Open-source repository
- [x] Chain registry submissions (ethereum-lists ✅, Chainlist ✅, viem ⏳, blockscout ⏳)
- [x] GitHub CI health checks
- [x] DEX live — Uniswap V2 fork, UST/USDT pair at https://147-45-143-23.sslip.io/dex
- [x] GeckoTerminal listing submitted ⏳
- [ ] GeckoTerminal / CoinGecko listing approved
- [ ] Bridge to Ethereum mainnet

---

## License

[MIT](LICENSE)
