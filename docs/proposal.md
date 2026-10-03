# CoinPilot

_Coincheck spot trading bot with on-chain performance proof for friends_

## Summary

CoinPilot automates spot trading on Coincheck based on customizable strategies while recording every trade's performance on Solana for transparent, tamper-proof tracking. Friends can follow each other's bot performance and split profits via a simple on-chain vault without exposing API keys.

## Target users

Retail crypto investors and their friend groups who want transparent, automated trading

## Problem

Trading bots on centralized exchanges are black boxes—friends can't verify each other's claimed returns or trust shared strategies.

## Solution

Log every executed trade's hash and PnL snapshot on Solana, creating a verifiable public track record that friends can audit in real time.

## MVP features

- Coincheck API integration for automated spot buy/sell based on simple strategies (MA cross, RSI)
- On-chain trade log program on Solana recording timestamp, pair, PnL per trade
- Shared dashboard showing each friend's bot performance pulled from on-chain data
- Simple profit-split vault contract for pooled strategies
- Risk controls: max position size, stop-loss triggers

## Chains

Solana

## Tech

Coincheck API, Node.js, Anchor (Solana), React, PostgreSQL, WebSocket price feeds

## Category

DeFi

## Why now

Retail interest in crypto trading automation is rising in Japan, and combining CEX execution with on-chain transparency solves the trust gap in informal friend-group trading.

## Roadmap

- Add more exchange integrations (Binance, bitFlyer) beyond Coincheck
- Build strategy marketplace where users can publish/subscribe to verified bots
- Introduce staking-based reputation for strategy creators
