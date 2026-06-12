# Treasury Payback Model

The **treasury payback model** is a voluntary repayment structure where a treasury withdrawal is treated as bridge funding until commercial revenue can cover operations, with scheduled surplus returns to the Cardano treasury.

## Position

[[proposals/eternl-path-to-sustainability-2026-2027]] is the ingested example. [[entities/tastenkunst|Tastenkunst GmbH]] asks for **$420,000** (₳1,680,000 at $0.25/ADA) for 12 months of [[entities/eternl|Eternl]] operations while **Pro subscription** revenue ramps. The model differs from [[concepts/treasury-escrow-oversight|milestone escrow]] (Pebble) and [[entities/intersect|Intersect]] TRSC/PSSC administration (Cardano Vision, Tweag).

## Eternl payback rules

Funds convert to stablecoins in a public wallet. **Every December and June:**

| Stage | Condition | Action |
|-------|-----------|--------|
| 1. Full repayment | Remaining treasury stablecoins + Pro-plan income > $420,000 | 100% of surplus repays treasury until **$420,000 USD equivalent** (as received) is fully repaid |
| 2. Additional donation | Full $420k repaid **and** Pro income > $420k in prior 12 months | Donate **50%** of income above $420k until **$210,000** additional ADA donated |
| 3. Transparency | Ongoing | On-chain Pro-plan metadata; public earnings report; publish repayment/donation tx hashes |

**Not counted toward payback:** Eternl DApp Browser / MonsterSwap service fees (cover office, legal, licenses). **Ada price guard:** if ADA > $0.25 at conversion, only $420k kept as stablecoins; excess ADA returned immediately.

## Contrast with other treasury patterns

| Pattern | Example | Release trigger |
|---------|---------|-----------------|
| Milestone escrow + oversight board | [[proposals/pebble-ecosystem-maintenance-2026]] | Deliverable acceptance per milestone |
| Intersect TRSC/PSSC + assurer | [[proposals/tweag-core-cardano-infrastructure-2026-2028]] | Contract milestones + 3rd-party assurance |
| Operational grant + revenue payback | [[proposals/eternl-path-to-sustainability-2026-2027]] | Calendar surplus assessments vs Pro revenue |

## Open questions

- How enforceable are voluntary payback commitments without on-chain escrow?
- Should DReps treat Pro revenue projections (~5,500 users at 4.2% conversion) as credible for a ₳1.68M ask?
- Does self-administration by the proposer weaken accountability vs Intersect or independent escrow boards?

## Related

- [[entities/eternl]]
- [[entities/tastenkunst]]
- [[proposals/eternl-path-to-sustainability-2026-2027]]
- [[concepts/treasury-escrow-oversight]]
