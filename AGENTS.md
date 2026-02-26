# Splits -- Agent Guide

## What is Splits?

Onchain financial operations for builders. Two pillars:

**Open Source Contracts & Tools** -- Public good payment primitives that run for free, forever. Audited, zero fees, deployed on 13+ chains, $250M+ distributed. Explorer at [app.splits.org](https://app.splits.org).
- **Split** -- distribute funds to N recipients by percentage
- **Waterfall** -- sequential/priority-based distribution
- **Swapper** -- automatic token conversion

**Onchain Financial Ops Platform** -- Purpose-built operational platform for builders at [teams.splits.org](https://teams.splits.org). Multi-chain, passkey-based, multi-signature smart accounts (ERC-4337), treasury management, expenses, accounting, bank transfers, invoicing. Works for solo builders and teams alike.

**Networks:**
- Full support (native smart accounts, all platform features): Ethereum, Base, Optimism, Arbitrum, Celo, World Chain
- Partial support (send/receive assets via bridging): 70+ EVM networks powered by relay.link (see https://relay.link for full chain list)

## Repo Map

Start with the repo that matches your task:

| Repo | When to look here |
|------|------------------|
| `splits-contracts-monorepo` | Writing, auditing, or integrating with v2 contracts or smart accounts (ERC-4337). **Has its own AGENTS.md and CLAUDE.md.** |
| `splits-contracts` | Working with v1 contracts (legacy -- prefer v2) |
| `splits-sdk` | Building JS/TS integrations, React UIs, or querying splits data |
| `splits-waterfall` | Waterfall-specific contract work |
| `splits-swapper` | Swapper-specific contract work |
| `docs` | Documentation site at docs.splits.org |
| `splits-connect` | Minimal browser extension for smart accounts (4337) |

## Common Dev Patterns

### Contracts (Solidity)
- **Toolchain:** Foundry (forge, cast, anvil)
- **Monorepo:** Turborepo + pnpm workspaces
- **Solidity version:** 0.8.23
- **Testing:** `forge test -vvv` (single package) or `pnpm test` (all)
- **Formatting:** `forge fmt` (Solidity), `pnpm format` (everything else)
- **Optimization:** via-ir with 5M optimizer runs

### SDK / Frontend (TypeScript)
- **Package manager:** pnpm
- **Workspaces:** pnpm workspaces
- **Key packages:** `@0xsplits/splits-sdk`, `@0xsplits/splits-sdk-react`

## Key Architecture Concepts

- **SplitsWarehouse** (ERC6909): Central token accounting in v2. All deposits/withdrawals flow through here.
- **Pull vs Push splits**: PullSplit deposits to warehouse (recipients claim later, gas-efficient). PushSplit sends directly.
- **Token IDs:** `uint256(uint160(tokenAddress))` in the warehouse.
- **Recipients must be sorted** by address ascending -- contracts revert otherwise.
- **Smart Vaults** use ERC-4337 v0.7 with m-of-n multi-sig and passkey signers.

## Deeper References

For contract-level details (architecture, build commands, gotchas, deployment):
- [`splits-contracts-monorepo/AGENTS.md`](https://github.com/0xSplits/splits-contracts-monorepo/blob/main/AGENTS.md)
- [`splits-contracts-monorepo/CLAUDE.md`](https://github.com/0xSplits/splits-contracts-monorepo/blob/main/CLAUDE.md)

For integration patterns and API docs:
- [docs.splits.org](https://docs.splits.org)
- [`splits-sdk` README](https://github.com/0xSplits/splits-sdk)

Machine-readable org index:
- [`llms.txt`](https://github.com/0xSplits/.github/blob/main/profile/llms.txt)
