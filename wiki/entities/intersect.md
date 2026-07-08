# Intersect

**Intersect** is a member-based organization that administers Cardano treasury execution on behalf of **Cardano Development Holdings (CDH)** under the Constitution. For major IO/IOG withdrawals it typically holds the off-chain legal contract, operates **Treasury Reserve Smart Contracts (TRSC)** and project-specific contracts (PSSC), and coordinates delivery assurance and community reporting.

## Treasury administration pattern (2025–2026 proposals)

Per [[sources/cardano-vision-2026-ior]], [[sources/tweag-core-cardano-infrastructure-2026-2028]], and [[sources/tweag-core-cardano-infrastructure-2026-2027]]:

- Legal contract between proposer and CDH; milestones agreed with Intersect
- Sundae Labs treasury management framework (TRSC/PSSC); audited by TxPipe and MLabs
- 2025 TRSC stake address: `stake17xzc8pt7fgf0lc0x7eq6z7z6puhsxmzktna7dluahrj6g6ghh5qjr`; migration to 2026 TRSC when established
- **Oversight Committee (2025 TRSC):** Sundae Labs, **Cardano Foundation**, Dquadrant, Xerberus, NMKR — co-sign Fund/Modify (2/5), Disperse/Reorganize (3/5), etc.; verify admin actions on-chain **without governance discretion** (not milestone technical acceptance; that is Intersect delivery assurance + 3rd-party assurer)
- **Oversight Committee (2026 TRSC):** Sundae Labs, Cardano Foundation, Dquadrant, NMKR, Sundial, **Eternl** — six trusted entities; same verification role ([[sources/withdraw-hardware-wallet-maintenance-2026]])
- **2026 TRSC stake:** `stake1784sdxt6jjennmstphgdu7l7c2scf5d02a6cve2dgn5s2kq5u3j9v` (per 2026 budget-cycle withdrawals)
- Third-party assurer reviews milestone deliverables; audit costs in proposal overhead
- Community dashboard for TRSC/PSSC tracking; funds delegate to auto-abstain DRep when staked; no SPO delegation

### Administered proposals (ingested)

| Proposal | Proposer | Ask |
|----------|----------|-----|
| [[proposals/cardano-vision-2026]] | [[entities/io-research|IO Research]] | ₳32.9M |
| [[proposals/tweag-core-cardano-infrastructure-2026-2027]] | [[entities/tweag|Tweag]] (Intersect submitter) | ₳18.3M |
| [[proposals/tweag-core-cardano-infrastructure-2026-2028]] | [[entities/tweag|Tweag]] | ₳39.8M |
| [[proposals/io-hydra]] | [[entities/input-output-group|IOG]] | ₳5.1M |
| [[proposals/cardano-critical-integrations-v1|CCI V1]] | Pentad (IOG, CF, EMURGO, Midnight) | ₳70M — enacted Dec 2025 |
| [[proposals/cardano-critical-integrations-v2|CCI V2]] | Pentad + Intersect as Administrator | ₳23M — 12-month maintenance |
| [[proposals/5am-earth-trust-layer-vision-2030-kpis|5am.earth trust layer]] | [[entities/5am-earth-foundation|5am.earth Foundation]] | ₳10M — 18-month agricultural trust layer |
| [[proposals/hardware-wallet-maintenance-2026|Hardware wallet maintenance]] | Vendor (Intersect submitter) | ₳1.31M — 12-month Ledger/Trezor + cardano-hw-cli upkeep |
| [[proposals/wirex-real-world-payments|Wirex real-world payments]] | [[entities/wirex|Wirex]] | ₳3.96M — Visa card + open-source payments infrastructure |
| [[proposals/technical-steering-committee-support-2026|TSC support 2026]] | [[entities/technical-steering-committee|Intersect Technical Steering Committee]] | ₳1.193M — 12-month technical-governance support (WP1/WP2/WP3) |
| [[proposals/intersect-governance-coordination-and-technical-stewardship-2026|Intersect governance coordination + technical stewardship]] | [[entities/intersect|Intersect]] | ₳25.4M — MBO operations, technical stewardship, incident response, critical-process reserve |
| [[proposals/bifrost-road-to-mainnet-phase-1|Bifrost road to mainnet (Phase 1)]] | [[entities/fluidtokens|FluidTokens]] + [[entities/lantr-engineering|Lantr Engineering]] | ₳12.33M — BTC bridge hardening/audits/private-mainnet readiness |
| [[entities/eternl|Eternl]] (2025 budget) | [[entities/tastenkunst|Tastenkunst GmbH]] | ₳583,000 — funding period ends July 2026 |

The 2026–2027 [[proposals/eternl-path-to-sustainability-2026-2027]] proposal shifts Eternl fund administration from Intersect to Tastenkunst self-administration with a [[concepts/treasury-payback-model|revenue payback]] model.

## Governance parameter proposals

Intersect also coordinates **parameter-change** governance actions through internal committees:

| Committee | Role |
|-----------|------|
| [[entities/civics-committee|Civics Committee]] | Constitutional process and CC operations |
| [[entities/technical-steering-committee|Technical Steering Committee]] | Technical approval for protocol-impacting actions |
| [[entities/parameter-committee|Parameter Committee]] | PCP review and recommendations |

**[[proposals/committee-min-size-7-to-5]]** (2026): Intersect proposes reducing [[concepts/committee-min-size|`committeeMinSize`]] from 7 to 5 for [[concepts/constitutional-committee|Constitutional Committee]] operational resilience. Civics approved 2026-03-13; TSC approved 2026-06-03. Resubmission after a prior action collided with another parameter change. Ratification depends temporally on [[proposals/update-plutus-cost-models]]. Intersect also facilitates periodic CC elections targeting **7 seats**.

**[[proposals/update-plutus-cost-models]]** (2026): Intersect (Parameter Committee) proposes updating [[concepts/plutus-cost-models|Plutus V1/V2/V3 cost models]] for the **[[concepts/van-rossem-hard-fork|van Rossem hard fork]]** (Protocol Version 11). Parameter Committee recommended 2026-03-05/19; TSC confirmed 2026-05-13. Tested on SanchoNet, Preview, and Preprod before mainnet submission.

## Related

- [[proposals/cardano-vision-2026]]
- [[proposals/tweag-core-cardano-infrastructure-2026-2027]]
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]]
- [[proposals/io-hydra]]
- [[proposals/cardano-critical-integrations-v1]]
- [[proposals/cardano-critical-integrations-v2]]
- [[proposals/5am-earth-trust-layer-vision-2030-kpis]]
- [[proposals/hardware-wallet-maintenance-2026]]
- [[proposals/wirex-real-world-payments]]
- [[proposals/technical-steering-committee-support-2026]]
- [[proposals/intersect-governance-coordination-and-technical-stewardship-2026]]
- [[proposals/bifrost-road-to-mainnet-phase-1]]
- [[entities/wirex]]
- [[entities/fluidtokens]]
- [[entities/lantr-engineering]]
- [[entities/sundae-labs]]
- [[entities/vacuumlabs]]
- [[concepts/hardware-wallet-interoperability]]
- [[concepts/agricultural-trust-layer]]
- [[concepts/cardano-critical-integrations]]
- [[concepts/hydra]]
- [[entities/input-output-group]]
- [[entities/cardano-foundation]]
- [[entities/emurgo]]
- [[entities/midnight-foundation]]
- [[entities/tweag]]
- [[entities/eternl]]
- [[entities/tastenkunst]]
- [[entities/civics-committee]]
- [[entities/technical-steering-committee]]
- [[entities/parameter-committee]]
- [[proposals/committee-min-size-7-to-5]]
- [[concepts/constitutional-committee]]
