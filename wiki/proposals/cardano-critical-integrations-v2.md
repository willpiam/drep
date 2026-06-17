# Cardano Critical Integrations V2

**Type:** Treasury withdrawal (integration maintenance + Fireblocks)  
**Proposer:** [[entities/intersect|Intersect]] (Administrator)  
**Co-proposers:** [[entities/input-output-group|IOG]], [[entities/cardano-foundation|Cardano Foundation]], [[entities/emurgo|EMURGO]], [[entities/midnight-foundation|Midnight Foundation]]  
**Source:** [[sources/cardano-critical-integrations-v2]]  
**On-chain recipient:** `stake17xzc8pt7fgf0lc0x7eq6z7z6puhsxmzktna7dluahrj6g6ghh5qjr` (Intersect 2025 TRSC)

Intersect requests **₳23,000,000** (~$5.75M at $0.25/ADA) for a **12-month** Year 2 program sustaining [[concepts/cardano-critical-integrations|CCI V1]] integrations and funding native **Fireblocks** institutional custody integration.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳23,000,000 |
| USD equivalent | ~$5,750,000 at $0.25/ADA |
| Duration | 12 months |
| Prior CCI V1 receipt | ₳70,000,000 (prior 24 months; enacted Dec 2025) |
| Admin model | Intersect TRSC/PSSC; Pentad Steering Committee |
| Programme report | [Intersect status update](https://intersectmbo.org/news/cardano-critical-integrations-program-status-update-report) |

## Budget breakdown (public categories)

| Category | Amount (₳) | Share | Notes |
|----------|------------|-------|-------|
| Integration & maintenance | 20,700,000 | ~90% | V1 ops + Fireblocks Year 1 fees |
| Enhancement & tooling reserve | 1,150,000 | ~5% | Ring-fenced; returned if unused |
| Legal, audit, contract admin | 1,150,000 | ~5% | Article II.7.4 compliance |
| **Total** | **23,000,000** | 100% | Vendor detail confidential |

## Scope

1. **Operations & maintenance** — Year 2 licensing/platform fees for Circle USDCx, LayerZero, Pyth, Dune; Cardano-side attestor, DVN/endpoint, oracle, and subgraph ops.
2. **Fireblocks** — Full native Cardano support (ADA, CNTs, staking/governance delegation foundations); integration fee + Year 1 platform fee.
3. **Enhancement & tooling reserve** — SDKs, reference implementations, monitoring/reconciliation/observability upgrades; Steering Committee approval per drawdown.
4. **Compliance & oversight** — Legal, independent audits, contract administration.

## Exclusions

USDT0, LayerZero OFT expansion, new tier-1 integrations, dapp funding, liquidity programs, marketing/events — each excluded and intended for separate governance actions.

## Governance and controls

- **Pentad Steering Committee:** IOG, CF, EMURGO, Midnight (voting); Intersect (Administrator, non-voting). 3/4 quorum for allocation decisions.
- **TRSC multisig:** Sundae Labs, Cardano Foundation, DQuadrant, Xerberus, NMKR.
- Funds at `addr1xxzc8pt7fgf0lc0x7eq6z7z6puhsxmzktna7dluahrj6g6v9swzhujsjlls7dajp59u95re0qdk9vh8mumlemw89535s4ecqxj`; auto-abstain delegation, no SPO staking.
- Drawdowns after signed agreements and SOW verification; stablecoin ringfencing until disbursement.
- Bi-annual reporting; unused funds returned at 12-month conclusion.
- NCL guardrail TREASURY-03a compliance at submission.

## Strategic framing

The proposal argues Cardano's TVL (~$192M as of Nov 2025 per V1 context) lags comparable ecosystems lacking standard DeFi primitives. CCI V1 delivered foundational integrations; V2 prevents operational gaps as V1 contracts expire. Competitive L1s fund infrastructure maintenance as recurring operating cost.

## DRep position

Published vote context: [vote 65](../../vote_context/markdown/65_critical.md) — **NO** on *Cardano Critical Integrations V2* (2026-06-17).

**Considerations recorded:**

- USDCx integration has been positive
- ₳70M was allocated ~6 months earlier (V1 enacted Dec 2025)
- Cardano Foundation involvement — concern over lack of community-elected board members
- EMURGO involvement — concern over concentration of voting power
- Proposal implies recurring annual treasury commitment

**Statement:** "We gave you guys ₳70M 6 months ago. Now you want ₳23M more?"

Prior votes on CCI V1 were **YES** (budget info Nov 2025; treasury withdrawal Dec 2025, enacted).

**On-chain:** [gov_action1cp0w6zwgwpj98jtu3r2q838lgwmhs6j49l58zx4q05lx220lmzaqqztnljz](https://cardanoscan.io/govAction/gov_action1cp0w6zwgwpj98jtu3r2q838lgwmhs6j49l58zx4q05lx220lmzaqqztnljz)

## Open questions

- Is ₳23M/12 months the expected steady-state run-rate, or a one-time Year 2 catch-up?
- What public metrics will the Steering Committee use to justify maintenance renewals?
- How does Fireblocks integration progress compare to other chains' institutional onboarding timelines?
- Can enhancement-reserve tooling (e.g. USDCx SDK) be scoped with community-visible deliverables?

## Related

- [[concepts/cardano-critical-integrations]]
- [[proposals/cardano-critical-integrations-v1]]
- [[entities/intersect]]
- [[entities/cardano-foundation]]
- [[entities/emurgo]]
- [[entities/midnight-foundation]]
- [[concepts/treasury-escrow-oversight]]
