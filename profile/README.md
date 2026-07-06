<img src="./docs/logo.svg" alt="SoroWill" width="64" height="64" />

# SoroWill 🔐

> **A trustless on-chain inheritance protocol on Stellar Soroban** — protect your crypto legacy with an automatic digital will. No lawyer. No court. No middleman.

[![Stellar](https://img.shields.io/badge/Network-Stellar-blue?logo=stellar)](https://stellar.org)
[![Soroban](https://img.shields.io/badge/Smart%20Contracts-Soroban-purple)](https://soroban.stellar.org)
[![License](https://img.shields.io/badge/License-MIT-green)](https://github.com/SoroWill/sorowill-contracts/blob/main/LICENSE)
[![Drips Wave](https://img.shields.io/badge/Drips-Stellar%20Wave%20Program-blueviolet)](https://drips.network/wave)

**Live app: [sorowill.vercel.app](https://sorowill.vercel.app/)**

---

## What is SoroWill?

SoroWill is a digital will protocol on Stellar. Lock USDC into a Soroban smart contract, designate beneficiaries with percentage splits, and set a check-in period. If you stop checking in, your USDC **automatically routes to your heirs** after a grace period.

Traditional crypto inheritance is broken — if you lose access, die, or become incapacitated without having shared your keys, your funds are lost forever. SoroWill solves this for anyone with a Stellar wallet, without needing a lawyer, a court, or a third party to hold your keys.

---

## How it works

```
Day 0 ── Create your Will
         └── Lock USDC, add beneficiaries with %, set check-in period (e.g. 90 days)

Day 90 ── Check-in deadline
          └── Miss it? A 7-day grace period begins
          └── Still alive? Call emergency_checkin() to reset the timer

Day 97 ── Grace period expires
          └── Anyone calls release_inheritance()
          └── USDC splits instantly to all beneficiaries by percentage
```

**Checking in regularly:** the owner simply calls `check_in()` before the deadline to prove they are alive and reset the countdown. The dashboard shows a live countdown timer.

---

## Key Features

- 🔐 **Trustless** — smart contract enforces everything, no third party needed
- ⏱️ **Dead Man's Switch** — automatic USDC release after a missed check-in + grace period
- 👨‍👩‍👧‍👦 **Multi-beneficiary** — up to 10 heirs, each with their own percentage
- 🛡️ **Guardian System** — 2-of-3 multisig guardians can trigger an early release
- ↩️ **Reversible** — owner can cancel and withdraw anytime while active
- 📨 **Grace Period** — 7-day window after a missed check-in for emergency recovery
- 💰 **Top-up anytime** — add more USDC to the will whenever you want

---

## Repositories

| Repo | Language | Description |
|---|---|---|
| [sorowill-contracts](https://github.com/SoroWill/sorowill-contracts) | ![Rust](https://img.shields.io/badge/-Rust-orange?logo=rust) | Soroban smart contracts — will creation, check-in, grace period, automatic inheritance release |
| [sorowill-sdk](https://github.com/SoroWill/sorowill-sdk) | ![TypeScript](https://img.shields.io/badge/-TypeScript-blue?logo=typescript) | npm package (`@sorowill/sdk`) — typed client, countdown utilities, Freighter wallet adapter |
| [sorowill-app](https://github.com/SoroWill/sorowill-app) | ![Next.js](https://img.shields.io/badge/-Next.js-black?logo=next.js) | Next.js 14 dashboard — create wills, check in, manage beneficiaries, claim inheritance |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Smart Contracts | Rust, Soroban SDK 22.0.0 |
| Blockchain | Stellar Network (testnet) |
| Token | USDC via Stellar Asset Contract (SAC) |
| SDK | TypeScript 5, @stellar/stellar-sdk |
| Wallet | Freighter |
| Frontend | Next.js 14, Tailwind CSS |

---

## Why Stellar?

Stellar's fast, low-cost transactions make SoroWill practical for everyday people, not just the wealthy — anyone with a Stellar wallet can protect their crypto legacy, without the cost or delay of traditional estate processes.

---

## Contributing via Drips Wave

SoroWill is part of the **Stellar Wave Program** on Drips — an open-source contributor bounty program backed by the Stellar Development Foundation.

Browse open issues across our 3 repositories, apply to work on one, and earn rewards when your PR is merged.

👉 **[Join the Stellar Wave Program](https://drips.network/wave)**

> **Do NOT start work on any issue until assigned by the maintainer.**
> Comment on the issue to express interest and wait for assignment.

---

## License

MIT — see individual repositories for details.

---

<div align="center">
  <sub>Built on <a href="https://stellar.org">Stellar</a> · Part of the <a href="https://drips.network/wave">Stellar Wave Program</a></sub>
</div>
