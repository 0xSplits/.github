# 0xSplits

Onchain financial infrastructure for builders. A full-stack financial operations platform -- built on open source payment contracts that run for free, forever.

**[Website](https://splits.org)** | **[Teams](https://teams.splits.org)** | **[Docs](https://docs.splits.org)** | **[Explorer](https://app.splits.org)**

---

## Onchain Financial Ops Platform

Purpose-built operational platform for builders at [teams.splits.org](https://teams.splits.org). Smart Vaults, treasury management, expenses, and more -- whether you're a solo builder working with agents or a full team.

| Repo | Description | Language |
|------|-------------|----------|
| [splits-contracts-monorepo](https://github.com/0xSplits/splits-contracts-monorepo) | ERC-4337 Smart Vaults | Solidity |
| [splits-connect](https://github.com/0xSplits/splits-connect) | Browser extension | TypeScript |

## Open Source Contracts & Tools

Public good payment primitives. Audited, zero fees, deployed on 13+ chains. $250M+ distributed.

- **Split** -- Distribute funds to any number of recipients by percentage
- **Waterfall** -- Sequential payments (e.g., pay A first, then B gets the rest)
- **Swapper** -- Automatically convert received tokens

Plus SDK, subgraph, and docs for building on top. Explorer at [app.splits.org](https://app.splits.org).

| Repo | Description | Language |
|------|-------------|----------|
| [splits-contracts-monorepo](https://github.com/0xSplits/splits-contracts-monorepo) | v2 core contracts (Split, Waterfall, Swapper) | Solidity |
| [splits-contracts](https://github.com/0xSplits/splits-contracts) | v1 core contracts (legacy) | Solidity |
| [splits-waterfall](https://github.com/0xSplits/splits-waterfall) | Waterfall payment contracts | Solidity |
| [splits-sdk](https://github.com/0xSplits/splits-sdk) | JS/TS SDK + React hooks | TypeScript |
| [docs](https://github.com/0xSplits/docs) | Documentation site source | TypeScript |

## Quick Links

- [Integration guide](https://docs.splits.org)
- [SDK reference](https://github.com/0xSplits/splits-sdk)
- [Contract addresses](https://docs.splits.org/contracts)

## For AI Agents

If you're an LLM or agent working with this codebase:

- **Start here:** [`AGENTS.md`](https://github.com/0xSplits/.github/blob/main/AGENTS.md) -- org-level overview and repo map
- **Machine-readable index:** [`llms.txt`](https://github.com/0xSplits/.github/blob/main/profile/llms.txt) -- structured repo manifest
- **Contracts deep dive:** [`splits-contracts-monorepo/AGENTS.md`](https://github.com/0xSplits/splits-contracts-monorepo/blob/main/AGENTS.md) -- architecture, build commands, key gotchas
