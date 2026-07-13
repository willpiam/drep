# Global Order Book / DeFi Kernel

**Type:** Treasury withdrawal (DeFi coordination standard + reference protocols)  
**Proposer:** [[entities/dano-finance|Dano Finance]]  
**Administrator:** [[entities/minswap-labs|Minswap Labs]] (1% budget administration fee)  
**Source:** [[sources/global-order-book-connect-cardano-defi]]

The proposal requests **₳3,333,000** (₳3,300,000 delivery + ₳33,000 admin fee) to accelerate the **[[concepts/defi-kernel|DeFi Kernel]]** open standard and deliver two DeFi Kernel-compatible protocols plus a composable transaction-builder SDK.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳3,333,000 |
| Delivery budget | ₳3,300,000 |
| Admin fee | ₳33,000 (1% to Minswap Labs) |
| Proposer track record (self-reported) | ~$18M TVL; 10,000+ on-chain transactions |

## Work packages

| WP | Budget (ADA) | Deliverable |
|----|-------------:|-------------|
| WP1 DeFi Kernel registry | 300,000 | defikernel.org platform, submission process, compatibility docs |
| WP2 Spot Leverage Order Book | 1,000,000 | Leveraged spot trading protocol (collateral, borrow, settlement) |
| WP3 American Options | 1,000,000 | Pool-based American options market-making |
| WP4 Composable DeFi Transaction Builder SDK | 1,000,000 | Discovery, schema parsing, tx construction, adapters |

Each protocol workstream: design/testnet → security review/mainnet → adoption/reporting milestones.

## KPI framework (primary)

- DeFi Kernel registry live with ≥2 documented compatible contract packages from this proposal.
- Spot Leverage Order Book: **$1M rolling 30-day trading volume** within 90 days of mainnet.
- American Options: **$1M rolling 30-day option notional volume** within 90 days of mainnet.
- SDK v1 released; ≥1 external wallet/bot/indexer/dApp integration started or completed.

Stretch targets: $3–5M rolling 30-day volumes at 180 days.

## Accountability

- Minswap Labs milestone review and fund administration.
- Security review or audit required before mainnet for smart-contract workstreams.
- **5% of protocol fees** from Treasury-funded Spot Leverage and Options contracts returned to Treasury for 12 months post-mainnet.
- Unused/unearned funds returned per administrator process.

## DRep position

No published local vote-context markdown for this proposal is ingested yet, so no DRep position is recorded here.

## Related

- [[concepts/defi-kernel]]
- [[entities/dano-finance]]
- [[entities/minswap-labs]]
