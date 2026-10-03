# CoinPilot
![CoinPilot logo](assets/logo.png)

Coincheck spot trading bot with on-chain performance proof for friends.

## Overview

CoinPilot automates spot trading on Coincheck using customizable strategies while recording every trade's performance on Solana. This creates a transparent, tamper-proof track record that friends can follow and audit in real time, without ever exposing exchange API keys.

## Problem

Trading bots on centralized exchanges are black boxes. When friends share strategies or claim returns, there's no way to verify the numbers. Screenshots can be faked, memories are selective, and trust breaks down fast in informal friend-group trading.

## Solution

CoinPilot logs every executed trade's hash and PnL snapshot on Solana. This public, verifiable record lets friends audit each other's bot performance in real time, turning informal claims into provable facts.

## Features (MVP)

- Coincheck API integration for automated spot buy/sell based on simple strategies (MA cross, RSI)
- On-chain trade log program on Solana recording timestamp, pair, and PnL per trade
- Shared dashboard showing each friend's bot performance pulled from on-chain data
- Simple profit-split vault contract for pooled strategies
- Risk controls: max position size, stop-loss triggers

## Tech Stack

- Coincheck API
- Node.js
- Anchor (Solana)
- React
- PostgreSQL
- WebSocket price feeds

## How It Works

```
User Strategy Config
        |
        v
  Node.js Bot Engine --- Coincheck API (spot buy/sell)
        |
        v
  Trade Result (pair, PnL, timestamp)
        |
        v
  Anchor Program on Solana (on-chain trade log)
        |
        v
  React Dashboard <--- reads on-chain data
        |
        v
  Vault Contract (profit split for pooled strategies)
```

1. Users configure a strategy (MA cross, RSI) and risk limits.
2. The bot engine executes spot trades automatically via the Coincheck API.
3. Every executed trade's hash and PnL snapshot is recorded on a Solana program.
4. The shared dashboard pulls on-chain data so friends can audit real performance.
5. A simple vault contract splits profits for pooled strategies without sharing API keys.

## Roadmap

- Add more exchange integrations (Binance, bitFlyer) beyond Coincheck
- Build a strategy marketplace where users can publish and subscribe to verified bots
- Introduce staking-based reputation for strategy creators

## Pitch

- [Pitch Deck (PDF)](docs/pitch.pdf)
- [Pitch Script](docs/pitch-script.md)

## Team

- Name — Role — [GitHub](#) / [Twitter](#)
- Name — Role — [GitHub](#) / [Twitter](#)
- Name — Role — [GitHub](#) / [Twitter](#)

---

🎬 Pitch video: [docs/pitch-video.mp4](docs/pitch-video.mp4)
