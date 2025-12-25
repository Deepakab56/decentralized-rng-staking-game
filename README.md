# decentralized-rng-staking-game 🎮⛓️

A **fully on-chain decentralized staking game** where users stake ETH on numbered blocks and winners are selected using **verifiable randomness (Supra RNG)**.  
The protocol features **fair reward distribution**, **jackpot mechanics**, **token mint rewards**, and **round-based gameplay** — all enforced by immutable smart contracts.

---

## 📌 Table of Contents

- Overview
- Core Mechanics
- Features
- Tech Stack
- Smart Contract Architecture
- Game Flow
- Deployment
- Security Notes
- License

---

## 📖 Overview

This project implements a **round-based on-chain staking game**:

- Players stake ETH on one or more numbered blocks (0–24)
- After the staking window closes, a **random winning block** is selected using **Supra VRF**
- All ETH staked on the winning block shares the reward pool
- Additional **token-based jackpot and bonus rewards** are distributed

The game is:
- Fully on-chain
- Non-custodial
- Trustless and verifiable
- EVM-compatible

---

## ⚙️ Core Mechanics

- **25 stakeable blocks per round**
- **1-minute staking window**
- **Protocol fee on every stake**
- **Random winner selection via Supra Router**
- **Powerhouse jackpot chance**
- **Bonus token distribution (1 PLT mode)**
- **Automatic round reset**

---

## ✨ Features

- ✅ Block-based ETH staking (multiple blocks supported)
- ✅ Supra RNG-powered winner selection
- ✅ Fair reward distribution proportional to stake
- ✅ **Powerhouse jackpot mint & payout**
- ✅ Bonus token rewards (random or weighted)
- ✅ Protocol fee handling
- ✅ Fully non-custodial
- ✅ Reentrancy-protected
- ✅ Owner-controlled admin operations
- ✅ Max supply–safe token minting
- ✅ Fully on-chain round lifecycle

---

## 🛠 Tech Stack

- **Solidity** `^0.8.20`
- **Supra VRF Router**
- **OpenZeppelin-style security patterns**
- **EVM Compatible Chains**
  - Ethereum
  - BNB Smart Chain
  - Polygon
  - Arbitrum / Optimism

---

## 🧩 Smart Contract Architecture


**External Integrations**
- `IERC20` → Reward token with capped supply
- `ISupraRouter` → Verifiable randomness provider

---

## 🔄 Game Flow

### 1️⃣ Round Start
- `resetRound()` initializes a new round
- 1-minute staking window opens

### 2️⃣ Players Stake
- Users stake ETH on one or more blocks (0–24)
- Protocol fee deducted automatically

### 3️⃣ Randomness Request
- After staking window ends, RNG is requested from Supra

### 4️⃣ Winner Selection
- A winning block is selected
- Jackpot & reward modes determined

### 5️⃣ Reward Distribution
- ETH rewards distributed proportionally
- Token jackpots paid (if triggered)
- Bonus token rewards distributed

### 6️⃣ Next Round
- Remaining funds partially roll over
- New round begins

---

## 🚀 Deployment

### Compile
```bash
npx hardhat compile
