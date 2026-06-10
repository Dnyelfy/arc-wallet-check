# Arc Wallet Check ⚡

**Score your onchain activity on Arc Testnet.**

Live → **https://arc-wallet-check.vercel.app**

Paste any Arc address and get an instant, data-driven picture of its onchain life — no wallet connection or signature required for analysis.

## What it does

- **Wallet Quality Score (0–100)** — computed from real onchain data: transaction volume, wallet age, recency, contract diversity, token transfers, builder signals and gas balance. Tiers: 🌱 Newcomer → 🟡 Casual → 🔵 Active → ⚡ Power User.
- **Activity heatmap** — GitHub-style 12-week grid of daily transaction density.
- **"What's missing?" checklist** — an airdrop-readiness audit that tells you exactly which activity signals your wallet lacks and how to fix them.
- **Airdrop simulator** — play with FDV / airdrop share / eligible-wallet sliders to see a hypothetical allocation for your score (clearly labeled as speculation, not financial advice).
- **Downloadable score card** — canvas-rendered PNG, ready to share.
- **Stamp on-chain ⛓** — seal your score into Arc itself with a real transaction (`ArcWalletCheck|score=…` in calldata), verifiable on ArcScan.

## How it works

- **Data**: [ArcScan](https://testnet.arcscan.app) (Blockscout) REST API — address info, counters, paginated transaction history (up to 150 latest txs). Falls back to raw JSON-RPC (`rpc.testnet.arc.network`) if the explorer API is unavailable.
- **Chain**: Arc Testnet · Chain ID `5042002` · USDC-native gas.
- **Stack**: a single dependency-free `index.html` — vanilla JS, no build step, no framework. Deploy anywhere.

## Run locally

Serve the file over HTTP (MetaMask doesn't inject into `file://` pages):

```bash
npx serve .
```

## Sister project

🗳 [ArcVote](https://arcvote-one.vercel.app/arc-dapp.html) — onchain governance, GM/GN and message board on Arc, by the same builder.

---

Built by [@Dnyelfy](https://x.com/Dnyelfy) · Arc Testnet · not affiliated with Circle/Arc
