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

## Plain-language user story

**Without this (today):** Maya wants leveraged spot exposure and a hedge. She hops DEX → lender → options app (if any), each with its own UI, schemas, and discovery path. Her wallet can’t see “open intents” across protocols; a bot writer reimplements every integration from scratch. Liquidity stays in silos; advanced strategies need several apps and fragile custom txs.

**With this funded and delivered:** Protocols publish to a shared [[concepts/defi-kernel|DeFi Kernel]] registry. Maya (or her wallet/bot) discovers fillable orders and options pools through one pattern; the SDK builds composable txs. She opens leveraged spot and hedges with American options on compatible contracts—fewer hops, shared metadata, more on-chain activity on shared rails.

## Security trust surface

**You should not treat present-day reputation as a security proof for the new products.** Trust rests mostly on *process promises* plus *past product audits*, which do not carry over to WP2/WP3.

| Supportive | Limiting |
|------------|----------|
| Existing Danogo surfaces have published **Anastasia Labs** audit PDFs (Bond DEX, fixed/flex lending + leverage, oracle aggregator, CLMM) — [docs audit page](https://docs.dano.finance/introduction/audit-report) | Those audits cover **current Danogo stack**, not the treasury-funded Spot Leverage Order Book or American Options |
| Proposal: smart-contract WPs require **security review or audit before mainnet**; critical unresolved issues **block** those milestones; [[entities/minswap-labs]] gates disbursement | Wording is **"review *or* audit"** — weaker than naming a firm, two audits, bug bounty, or formal verification |
| Live TVL / operating history (~$13M DefiLlama) is weak market-survival evidence | No named founders; limited reputational hostage if something goes wrong |
| Registry can publish audit status as metadata | Registry listing itself is **not** a security gate (no audit committee) |

**DRep framing:** Process + prior Anastasia engagement is a reason to believe they *know* the bar; it is **not** a reason to pre-trust the new protocol code until reports for WP2/WP3 land. Leverage + options remain high-severity surfaces even post-audit.

## DRep position

No published local vote-context markdown for this proposal is ingested yet, so no DRep position is recorded here.

## Related

- [[concepts/defi-kernel]]
- [[entities/dano-finance]]
- [[entities/minswap-labs]]
- [[analysis/global-order-book-complexity]]
