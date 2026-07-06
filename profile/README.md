<img src="https://raw.githubusercontent.com/SoroWill/.github/main/docs/logo.svg" alt="SoroWill" width="64" height="64" />

# SoroWill

**Trustless on-chain inheritance on Stellar Soroban.**

[![Stellar Soroban](https://img.shields.io/badge/Stellar-Soroban-08b5e5?logo=stellar)](https://developers.stellar.org/docs/build/smart-contracts)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/SoroWill/sorowill-contracts/blob/main/LICENSE)

**Live app: [sorowill.vercel.app](https://sorowill.vercel.app/)**

## What is SoroWill

SoroWill lets anyone lock USDC (or any SEP-41 token) into a smart contract, name beneficiaries with percentage splits, and set a check-in period. If the owner stops checking in, the contract releases the funds to the beneficiaries after a grace period — no lawyer, no court, no middleman.

1. **Create a will** — lock a token balance, name beneficiaries and their shares, set a check-in period and a grace period.
2. **Check in** — prove you're still active before each deadline.
3. **Miss a check-in** — anyone can trigger the will, starting the grace period.
4. **Release** — if the grace period expires without a response, anyone can release the balance to the beneficiaries proportionally, in one transaction.
5. **Guardian override** — up to 3 named guardians can force an early release (2-of-3) if the owner is known to be incapacitated rather than simply inactive.

The owner can cancel or update beneficiaries at any time while the will is active.

## Repositories

| Repo | What it is |
|---|---|
| [`sorowill-contracts`](https://github.com/SoroWill/sorowill-contracts) | The Soroban smart contract (Rust) — the actual protocol that holds funds and enforces the rules. |
| [`sorowill-sdk`](https://github.com/SoroWill/sorowill-sdk) | TypeScript SDK ([`@sorowill/sdk`](https://www.npmjs.com/package/@sorowill/sdk) on npm) for talking to the contract and handling Freighter wallet connections. |
| [`sorowill-app`](https://github.com/SoroWill/sorowill-app) | The Next.js dashboard — create a will, check in, review beneficiaries and guardians, claim an inheritance. |

## Tech Stack

- **Rust** + **soroban-sdk** for the contract
- **TypeScript** + **@stellar/stellar-sdk** for the SDK
- **Next.js 14** + **Tailwind CSS** for the app
- **Freighter** for wallet connections

## Contributing via Drips Wave

These repos participate in the **Stellar Wave Program** on [Drips](https://drips.network/wave). Maintainer-tagged issues carry point values, and contributors who resolve them during an active Wave earn a proportional share of that Wave's reward pool. Check each repo's `CONTRIBUTING.md` for its contribution workflow.
