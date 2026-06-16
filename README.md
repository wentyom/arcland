# 🌍 Arc Land

> On-chain territory dApp built on Arc Network. Claim, customize and trade land parcels on a 50×50 blockchain grid.

**🗺️ On-Chain Territory • 💱 Parcel Marketplace • 🎨 Customize Your Block**

---

## 🚀 About Arc Land

**Arc Land** is a decentralized land ownership dApp on **Arc Network (Testnet)**. Every parcel on the 50×50 grid is a permanent, on-chain asset — owned, named, and colored by real wallet addresses.

Instead of static maps, Arc Land is a **live blockchain grid** where users can explore claimed territory, inspect owners, buy and sell parcels, and build their on-chain presence.

The goal of Arc Land is to make **on-chain ownership tangible, visual, and interactive** within the Arc ecosystem.

---

## ✨ Features

- 🗺️ **50×50 Grid** — 2,500 unique on-chain parcels, each with X/Y coordinates.
- ⛓️ **Permanent Ownership** — Claiming a parcel is forever. No expiry, no renewal.
- 🎨 **Customize** — Set a custom name and color for any parcel you own, stored on-chain.
- 💱 **Marketplace** — List your parcel for sale at any price. Buy amber-pulsing parcels from other owners.
- 🏆 **Leaderboard** — Real-time Top Owners ranking by number of parcels held.
- 🔍 **Parcel Inspector** — Click any cell to see owner, status, mint price, and neighbor count.
- 🔦 **Live Map** — Canvas-rendered grid with zoom, pan, brightness control and hover tooltips.

---

## 🏗️ Platform Sections

Arc Land is organized into three panels:

- **Left Sidebar** — Parcel info panel and My Land tab (your owned parcels).
- **Main Canvas** — Interactive 50×50 map with zoom and pan controls.
- **Right Panel** — Legend and live Top Owners leaderboard.

---

## 💡 How It Works

### 1. Connect Wallet
Supported wallets: MetaMask, Rabby, OKX, Coinbase Wallet, Trust Wallet — any EVM wallet.
Arc Network must be added (Chain ID: `5042002`). The app auto-prompts to add/switch.

### 2. Get Testnet USDC
Visit [faucet.circle.com](https://faucet.circle.com), select Arc Testnet, and request USDC.
USDC is the native gas token on Arc — used for both gas fees and parcel purchases.

### 3. Claim a Parcel
Click any empty cell on the map → **CLAIM PARCEL** button appears.

**Pricing:**
| Owned Neighbors | Price |
|---|---|
| 0 | 0.5 USDC |
| 1 | 0.6 USDC |
| 2 | 0.7 USDC |
| 3 | 0.8 USDC |
| 4 | 0.9 USDC (max) |

> Each neighboring parcel already owned by anyone adds +0.1 USDC to the base price.

### 4. Customize Your Parcel
After claiming, set a **name** and **color** for your parcel. Both are stored on-chain via `setName()` and `setColor()` contract calls.

### 5. List for Sale
Open any parcel you own → **LIST FOR SALE** → enter your price in USDC.
Platform fee: **5%** deducted on sale. Cancel listing at any time.

### 6. Buy Other Parcels
Amber-pulsing parcels on the map are listed for sale. Click one → **BUY** → confirm the transaction.

---

## ⚙️ Technical Details

| Detail | Value |
|---|---|
| Network | Arc Network Testnet |
| Chain ID | 5042002 |
| Gas Token | USDC (18 decimals) |
| Contract | `0x6F27e9A335298c5Cfb65D5AF04465084Aa11eFeC` |
| Grid Size | 50 × 50 = 2,500 parcels |
| Base Price | 0.5 USDC |
| Max Price | 0.9 USDC (4 neighbors) |
| Marketplace Fee | 5% on sale |
| Explorer | [testnet.arcscan.app](https://testnet.arcscan.app) |

### Smart Contract Functions

```solidity
buy(uint256 x, uint256 y) payable
setName(uint256 x, uint256 y, string name)
setColor(uint256 x, uint256 y, string color)
listForSale(uint256 x, uint256 y, uint256 price)
cancelListing(uint256 x, uint256 y)
ownedCount(address owner) view
```

---

## 🗺️ Map Controls

| Control | Action |
|---|---|
| Click parcel | Inspect / claim / buy |
| Drag | Pan the map |
| Scroll wheel | Zoom in / out |
| `+` / `−` buttons | Zoom control |
| `CTR` button | Center map |
| Brightness slider | Adjust map brightness |

---

## 🎨 Map Legend

| Color | Meaning |
|---|---|
| Dark green `#0e1a10` | Empty, unclaimed parcel |
| Bright green `#39ff14` | Your parcel |
| Blue `hsl(210,65%,45%)` | Owned by another address |
| Pulsing amber | Listed for sale |

---

## 🏛️ Built by Arc Architects

Arc Land was developed under the **Arc Architects** program — Circle's official community builder initiative for dApps on Arc Network.

Built by [@wentyom](https://x.com/wentyom) as part of the [ArcWorld](https://arcworld.io) ecosystem.

---

## 🔗 Links

- 🌐 App: [land.arcworld.io](https://land.arcworld.io)
- 🌍 ArcWorld Hub: [arcworld.io](https://arcworld.io)
- 🔍 Explorer: [testnet.arcscan.app](https://testnet.arcscan.app)
- 💧 Faucet: [faucet.circle.com](https://faucet.circle.com)
- 🐦 Twitter: [@wentyom](https://x.com/wentyom)
