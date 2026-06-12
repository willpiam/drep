# Intersect

**Intersect** is a member-based organization that administers Cardano treasury execution on behalf of **Cardano Development Holdings (CDH)** under the Constitution. For major IO/IOG withdrawals it typically holds the off-chain legal contract, operates **Treasury Reserve Smart Contracts (TRSC)** and project-specific contracts (PSSC), and coordinates delivery assurance and community reporting.

## Treasury administration pattern (2025–2026 proposals)

Per [[sources/cardano-vision-2026-ior]] and [[sources/tweag-core-cardano-infrastructure-2026-2028]]:

- Legal contract between proposer and CDH; milestones agreed with Intersect
- Sundae Labs treasury management framework (TRSC/PSSC); audited by TxPipe and MLabs
- 2025 TRSC stake address: `stake17xzc8pt7fgf0lc0x7eq6z7z6puhsxmzktna7dluahrj6g6ghh5qjr`; migration to 2026 TRSC when established
- **Oversight Committee (2025 TRSC):** Sundae Labs, **Cardano Foundation**, Dquadrant, Xerberus, NMKR — co-sign Fund/Modify (2/5), Disperse/Reorganize (3/5), etc.; verify admin actions on-chain **without governance discretion** (not milestone technical acceptance; that is Intersect delivery assurance + 3rd-party assurer)
- Third-party assurer reviews milestone deliverables; audit costs in proposal overhead
- Community dashboard for TRSC/PSSC tracking; funds delegate to auto-abstain DRep when staked; no SPO delegation

### Administered proposals (ingested)

| Proposal | Proposer | Ask |
|----------|----------|-----|
| [[proposals/cardano-vision-2026]] | [[entities/io-research|IO Research]] | ₳32.9M |
| [[proposals/tweag-core-cardano-infrastructure-2026-2028]] | [[entities/tweag|Tweag]] | ₳39.8M |
| [[entities/eternl|Eternl]] (2025 budget) | [[entities/tastenkunst|Tastenkunst GmbH]] | ₳583,000 — funding period ends July 2026 |

The 2026–2027 [[proposals/eternl-path-to-sustainability-2026-2027]] proposal shifts Eternl fund administration from Intersect to Tastenkunst self-administration with a [[concepts/treasury-payback-model|revenue payback]] model.

## Governance parameter proposals

Intersect also coordinates **parameter-change** governance actions through internal committees:

| Committee | Role |
|-----------|------|
| [[entities/civics-committee|Civics Committee]] | Constitutional process and CC operations |
| [[entities/technical-steering-committee|Technical Steering Committee]] | Technical approval for protocol-impacting actions |
| [[entities/parameter-committee|Parameter Committee]] | PCP review and recommendations |

**[[proposals/committee-min-size-7-to-5]]** (2026): Intersect proposes reducing [[concepts/committee-min-size|`committeeMinSize`]] from 7 to 5 for [[concepts/constitutional-committee|Constitutional Committee]] operational resilience. Civics approved 2026-03-13; TSC approved 2026-06-03. Resubmission after a prior action collided with another parameter change. Intersect also facilitates periodic CC elections targeting **7 seats**.

## Related

- [[proposals/cardano-vision-2026]]
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]]
- [[entities/input-output-group]]
- [[entities/tweag]]
- [[entities/eternl]]
- [[entities/tastenkunst]]
- [[entities/civics-committee]]
- [[entities/technical-steering-committee]]
- [[entities/parameter-committee]]
- [[proposals/committee-min-size-7-to-5]]
- [[concepts/constitutional-committee]]
