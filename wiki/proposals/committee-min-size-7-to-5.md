# Reduce committeeMinSize from 7 to 5

**Type:** Parameter change (`parameter_change_action`)  
**Proposer:** [[entities/intersect|Intersect]] (Civics Committee + Technical Steering Committee; Parameter Committee recommendation)  
**Source:** [[sources/reduce-committeeminsize-7-to-5]]

Intersect proposes lowering **`committeeMinSize`** from **7** to **5** to add operational resilience while keeping constitutional safeguards. The action does **not** reduce the number of elected Constitutional Committee seats; it only lowers the on-chain minimum required for governance to remain operable.

## On-chain details

| Item | Value |
|------|-------|
| Parameter update | `committee_min_size` → **5** |
| Deposit | ₳100,000 |
| Transaction ID | `c82f3834898e4d70d3605fa0d92ffe31345701075b107a54309c1525f9581f62` |
| Gov action index | 0 |
| [Explorer](https://explorer.cardano.org/governance-action/c82f3834898e4d70d3605fa0d92ffe31345701075b107a54309c1525f9581f6200) | Cardano Foundation governance explorer |

## Motivation

The Constitutional Committee currently has **7 members**, equal to `committeeMinSize` = **7**. If membership drops below the minimum — resignation, term expiration, or other departure — **all governance actions requiring CC approval become ineligible**, stalling parameter changes, constitution updates, treasury withdrawals, and hard forks.

Setting the minimum to **5** allows the committee to keep operating with up to two fewer members while elections or replacements proceed.

## Dependencies

**Temporal dependency only:** ratification requires enactment of a separate Plutus cost-model parameter change for the **van Rossem** hard fork (`gov_action1eqhnsdyf3exhp5mqt7sdjtl7xy69wqg8tvg854psns2jt72cra3qqrcnr8r`). No technical interaction between the parameter updates.

## Approvals and process

| Body | Action | Date |
|------|--------|------|
| [[entities/civics-committee|Civics Committee]] | Approved submission | 2026-03-13 |
| [[entities/technical-steering-committee|TSC]] | Approved submission | 2026-06-03 |
| [[entities/parameter-committee|Parameter Committee]] | PCP-005 recommendation | Forum post 2025-11-11 |

Guardrails **CMS-01/02/03** satisfied at value 5. **PARAM-06a** (90-day off-chain lead for critical governance parameters) cited.

## Resubmission history

A prior action (`gov_action1mldvtys6ketjg87wtpvr6cd77kdrd8sp62a8sxgadhmxx2s8lh7sqp2qedq`) was **invalidated** before lifetime expiry due to a technical **collision** with another parameter change (Increase Transaction and Block Memory Units, Part 1 of 2). Intersect resubmitted after coordination to avoid repeat collision and gather DRep/CC feedback.

## Trade-offs

- **Pro:** Governance continues if membership falls to 5 or 6 while refilling seats.
- **Con:** At 5 active members (2/3 threshold), only **2** dissenting votes block ratification (vs **3** at size 7). One inactive member plus one dissenter can veto.

Intersect states this is **not** an attempt to centralize governance or shrink the elected committee; elections still target **7 seats**.

## Reversion

Reversible by a future parameter change back to **7**, but reversion only halts governance if fewer than 7 members are registered at that time. Risk deemed minimal given continued 7-seat election intent.

## DRep position

Vote context placeholder exists ([vote 60](../../vote_context/markdown/60_committeeMinSize.md)); **no recorded DRep position yet**.

## Open questions

- Is a buffer of two seats (7 elected, min 5) sufficient given CC election cadence and term lengths?
- How should delegates weigh easier blocking at effective size 5 vs catastrophic governance halt at size 6 with min 7?
- Does temporal bundling with the van Rossem cost-model action affect voter strategy?

## Related

- [[concepts/committee-min-size]]
- [[concepts/constitutional-committee]]
- [[entities/intersect]]
- [[entities/civics-committee]]
- [[entities/technical-steering-committee]]
- [[entities/parameter-committee]]
