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

## Blockfrost NFP commercial payback (proposed, post-subsidy)

[[proposals/blockfrost-transformation-to-not-for-profit]] is primarily an **18-month milestone-escrowed transition** ([[concepts/treasury-escrow-oversight|Intersect TRSC/PSSC]]), not a payback-first operational grant. However, its **post-subsidy sustainability** section proposes that an elected not-for-profit board may operate **paid API tiers** with **profits returned to the Cardano Treasury** — structurally similar to Eternl's voluntary repayment but deferred to board discretion after the treasury subsidy ends. A vendor-backed federation alternative would route membership fees to the NFP rather than direct treasury payback. Neither path is contractually locked in the initial 18-month ask.

## CB DAO unused-fund return

[[proposals/cardano-builder-dao|Cardano Builder DAO]] commits to returning **unused or unallocated** DAO treasury funds to the Cardano Treasury after approved work completes — not a revenue payback model, but a **surplus-return** practice. After rounds 1–2, CB DAO returned **₳354,790** ([on-chain tx](https://adastat.net/transactions/dfcf57c8c65c50bb208106db91b2db38c4a7512f9fbf100f9f5e1f6301ceb8fc)).

## Contrast with other treasury patterns

| Pattern | Example | Release trigger |
|---------|---------|-----------------|
| Milestone escrow + oversight board | [[proposals/pebble-ecosystem-maintenance-2026]] | Deliverable acceptance per milestone |
| Intersect TRSC/PSSC + assurer | [[proposals/tweag-core-cardano-infrastructure-2026-2028]] | Contract milestones + 3rd-party assurance |
| Operational grant + revenue payback | [[proposals/eternl-path-to-sustainability-2026-2027]] | Calendar surplus assessments vs Pro revenue |
| Transition escrow + future NFP revenue to treasury | [[proposals/blockfrost-transformation-to-not-for-profit]] | Milestones during subsidy; board-chosen commercial model afterward |
| Initiative DAO sub-grants + unused return | [[proposals/cardano-builder-dao]] | Member-governed allocation; surplus returned after funding rounds |

## Open questions

- How enforceable are voluntary payback commitments without on-chain escrow?
- Should DReps treat Pro revenue projections (~5,500 users at 4.2% conversion) as credible for a ₳1.68M ask?
- Does self-administration by the proposer weaken accountability vs Intersect or independent escrow boards?

## Related

- [[entities/eternl]]
- [[entities/tastenkunst]]
- [[proposals/eternl-path-to-sustainability-2026-2027]]
- [[proposals/blockfrost-transformation-to-not-for-profit]]
- [[proposals/cardano-builder-dao]]
- [[concepts/treasury-escrow-oversight]]
