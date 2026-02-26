# Splits

Financial infrastructure for onchain builders.

We build apps, contracts, and developer tools that make it easy for builders to manage onchain treasuries, revenues, and expenses. Built on open source contracts that run for free, forever.

- Onchain banking: [teams.splits.org](https://teams.splits.org)
- Onchain banking guidebook: [notion](https://splits.notion.site/Splits-Guidebook-177f7c3c8eff80438f21c2032fe5d653)
- Payment lego explorer: [app.splits.org](https://app.splits.org)
- Payment lego docs: [docs.splits.org](https://docs.splits.org)
- Company blog: [splits.org/blog](https://splits.org/blog)

---

## Teams: Onchain financial ops platform

Purpose-built financial ops platform for builders at [teams.splits.org](https://teams.splits.org). Crosschain, multi-signature accounts with professional workflows for treasury management, automated rebalancing, accounting, invoicing, bank transfers, and more. Crafted for teams and solo builders working with agents. Free to use, no application/paperwork, sign up takes 30 seconds.

| Repo | Description | Language |
|------|-------------|----------|
| [splits-smart-vaults](https://github.com/0xSplits/splits-contracts-monorepo/tree/main/packages/smart-vaults) | Crosschain, multi-signature accounts (ERC-4337) | Solidity |
| [splits-connect](https://github.com/0xSplits/splits-connect) | Browser extension | TypeScript |

## Payment legos: Open source contracts & tools

Public good, stackable payment legos. Audited, zero fees, deployed on 13+ chains. $250M+ distributed.

- **Split:** Distribute future income to multiple recipients by percentage
- **Waterfall:** Sequential payments (e.g., pay A $X first, then B $Y, and split the rest 60/40)
- **Swapper:** Automatically convert received tokens

Plus SDK, subgraph, and docs for building on top. Contract explorer at [app.splits.org](https://app.splits.org).

| Repo | Description | Language |
|------|-------------|----------|
| [splits-v2](https://github.com/0xSplits/splits-contracts-monorepo/tree/main/packages/splits-v2) | v2 Split contracts | Solidity |
| [splits-contracts](https://github.com/0xSplits/splits-contracts) | v1 core contracts (legacy) | Solidity |
| [splits-waterfall](https://github.com/0xSplits/splits-waterfall) | Waterfall payment contracts | Solidity |
| [splits-swapper](https://github.com/0xSplits/splits-swapper) | Swapper payment contracts | Solidity |
| [splits-sdk](https://github.com/0xSplits/splits-sdk) | JS/TS SDK + React hooks | TypeScript |
| [docs](https://github.com/0xSplits/docs) | Documentation site source | TypeScript |

## Quick Links

- [Integration guide](https://docs.splits.org)
- [SDK reference](https://github.com/0xSplits/splits-sdk)
- [Contracts](https://docs.splits.org/core)

## For AI Agents

If you're an LLM or agent working with this codebase:

- **Start here:** [`AGENTS.md`](https://github.com/0xSplits/.github/blob/main/AGENTS.md) -- org-level overview and repo map
- **Machine-readable index:** [`llms.txt`](https://github.com/0xSplits/.github/blob/main/profile/llms.txt) -- structured repo manifest
- **Contracts deep dive:** [`splits-contracts-monorepo/AGENTS.md`](https://github.com/0xSplits/splits-contracts-monorepo/blob/main/AGENTS.md) -- architecture, build commands, key gotchas
