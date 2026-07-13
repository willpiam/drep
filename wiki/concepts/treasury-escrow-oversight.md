# Treasury Escrow Oversight

**Treasury escrow oversight** is the governance pattern of holding withdrawn ADA in smart contracts and releasing it against milestone criteria verified by independent reviewers.

## Position

The [[proposals/pebble-ecosystem-maintenance-2026]] proposal uses the SundaeSwap treasury-contract framework as its control model. The proposal says funds are locked in `treasury.ak` when the governance action is enacted and then managed through `vendor.ak` according to a milestone schedule for [[entities/harmonic-labs|Harmonic Labs]].

## Controls in the Pebble proposal

| Control | Description |
|---------|-------------|
| Milestone disbursement | HLabs initiates payment and any one oversight-board member co-signs |
| Early sweep | HLabs and any one board member can return unused funds |
| Pause milestone | Any one board member can pause funding |
| Resume milestone | Board majority required |
| Modify project | HLabs plus board majority required |
| Failsafe sweep | Funds left after expiration automatically return to the Cardano treasury |
| Delegation | Escrowed funds use auto-abstain DRep delegation and no SPO delegation |

## Oversight board

The proposal names Santiago Carmuega, Lucas Rosa, and Chris Gianelloni as the independent oversight board. They are described as having no stake in HLabs, with responsibility to review milestones, co-sign disbursements, and halt funding if delivery is not adequate.

## Reporting artifacts

The proposal commits to:

- monthly lightweight updates;
- quarterly milestone and financial reports;
- a public transaction journal for treasury withdrawal, disbursement, reorganizations, and sweeps;
- acceptance criteria tied to public releases, CI status, benchmark submissions, and documentation artifacts.

## dRep DAO council multisig (Cardano Builder DAO)

[[proposals/cardano-builder-dao]] uses a **third escrow pattern** distinct from both Pebble vendor escrow and Intersect TRSC:

| Element | Detail |
|---------|--------|
| Administrator | Independent **dRep DAO council** multisig — not Intersect/CDH |
| Named council | Cardano Yoda, Marco Grendel Moshi, +1 non-affiliated active dRep |
| Flow | Council receives treasury withdrawal → holds in auditable accounts → validates milestones → disburses to [[entities/cardano-builder-dao|CB DAO]] |
| Delegation | No SPO delegation; auto-abstain DRep delegation (Constitution §7) |
| Sub-allocation | CB DAO's internal **[[concepts/initiative-dao|Initiative DAO]]** smart contracts govern member votes and multi-output distributions to funded builders |

The 2025 CB DAO initial treasury ask (₳12M per ecosystem reporting) used **Intersect TRSC** administration; the 2026 continuation proposal shifts milestone escrow oversight to active dReps while CB DAO retains on-chain governance for sub-grants.

## Article II.7.5 sole administrator (dOSPO revised pilot)

[[proposals/revised-cardano-dospo-and-omf-program-2026]] uses a **fourth custody pattern**: proposer self-administration under **Constitution Article II.7.5**, without Intersect TRSC/PSSC or milestone smart-contract escrow.

| Element | Detail |
|---------|--------|
| Administrator | [[entities/christian-taylor|Christian Taylor]] / Open Source Cowboy Consulting — **sole** Article II.7.5 administrator effective at treasury withdrawal |
| Unconditional | Not contingent on advisory council formation, 501(c)(3) entity formation, or other future deliverables |
| Advisory input | External OS + Technical Community councils publish written feedback on-chain before each disbursement; **no veto** |
| Auditor | Mill Law Firm — quarterly financial reviews + annual audit attached to quarterly reports |
| Replaceability | DReps may pass on-chain Info Action to replace administrator or sunset program; uncommitted funds returned within 30 days |
| Sponsor commitment | Proposer commits to sponsoring Info Action if **15+ DReps** request replacement or shutdown |
| Entity transition | US 501(c)(3) public charity by month 6 is a deliverable; transferring administrator role requires **separate** on-chain Info Action |

This contrasts with the **failed original** dOSPO proposal (₳12M / 36 months), which deferred stronger administrator clarity and gave councils stronger pre-funding gatekeeping language. See [[concepts/dospo-omf]] for original vs revised comparison.

## Self-administered operational grant (Eternl)

[[proposals/eternl-path-to-sustainability-2026-2027]] uses neither milestone escrow nor Intersect TRSC. [[entities/tastenkunst|Tastenkunst GmbH]] self-administers a **non-milestone** 12-month operational withdrawal: funds convert to stablecoins in a public company wallet, with **[[concepts/treasury-payback-model|biannual surplus repayments]]** tied to Pro subscription revenue rather than deliverable acceptance.

Transparency commitments include on-chain Pro-plan metadata, public earnings reports, and published repayment transaction hashes. There is no independent oversight board or smart-contract release schedule in this proposal.

The prior 2025 Eternl treasury withdrawal (₳583,000) was **Intersect-administered**; the 2026–2027 proposal shifts administration to Tastenkunst directly.

## Off-chain budget administrator (Minswap Labs)

[[proposals/global-order-book-defi-kernel]] uses **[[entities/minswap-labs|Minswap Labs]]** as budget administrator (1% fee) for milestone review and disbursement — **not** Intersect TRSC/PSSC. This is a lighter-weight accountability pattern than smart-contract escrow or TRSC custody.

## Intersect interim administration (Alchemy)

[[proposals/alchemy-cardano-native-bitcoin-treasury]] proposes **Intersect as interim fund administrator** for Sundial/Charms Alchemy — accounting, fund separation, milestone verification, and custody controls. If Intersect does not confirm within 30 days of enactment, proposer nominates an alternative independent administrator. Administrator-held ADA: auditable accounts, auto-abstain DRep delegation, no SPO delegation.

## Pentad CCI model (Critical Integrations V2)

[[proposals/cardano-critical-integrations-v2|CCI V2]] uses Intersect TRSC administration with a **Pentad Steering Committee** layer above standard Oversight Committee multisig:

| Layer | Role |
|-------|------|
| Pentad Steering Committee | IOG, Cardano Foundation, EMURGO, Midnight (voting); Intersect (Administrator, non-voting). Approves maintenance renewals and enhancement-reserve drawdowns (3/4 quorum). |
| Intersect Administrator | TRSC custody, SOW verification, delivery assurance, bi-annual reporting |
| TRSC multisig | Sundae Labs, Cardano Foundation, DQuadrant, Xerberus, NMKR — same pattern as Vision/Tweag |

Enhancement-reserve drawdowns require Steering Committee scope approval; maintenance drawdowns tie to continuation of V1 operational SLAs. Unused enhancement reserve and end-of-period balances return to treasury. Vendor costs are confidential; public reporting is by category.

## Intersect TRSC model (Cardano Vision, Tweag)

For [[proposals/cardano-vision-2026]], [[proposals/tweag-core-cardano-infrastructure-2026-2027]], [[proposals/tweag-core-cardano-infrastructure-2026-2028]], [[proposals/io-hydra]], [[proposals/blockfrost-transformation-to-not-for-profit]], [[proposals/5am-earth-trust-layer-vision-2030-kpis]], [[proposals/hardware-wallet-maintenance-2026]], [[proposals/wirex-real-world-payments]], [[proposals/technical-steering-committee-support-2026]], [[proposals/intersect-governance-coordination-and-technical-stewardship-2026]], and [[proposals/bifrost-road-to-mainnet-phase-1]], withdrawn ADA flows through Intersect's **Treasury Reserve Smart Contract (TRSC)** and project-specific **PSSC** contracts ([[entities/sundae-labs|Sundae Labs]] framework). This is a different pattern from Pebble's vendor-specific `treasury.ak` / `vendor.ak` board above.

[[proposals/5am-earth-trust-layer-vision-2030-kpis]] adds a **delivery/administration separation** explicit in constitutional terms: 5am.earth delivers; Intersect administers; Oversight Committee verifies admin actions; 3rd-party assurer reviews milestone deliverables. Payment schedule: ₳5M approval / ₳2M M1 / ₳3M M2 (M3 is evidence-only self-sustain gate).

### Oversight Committee (2025 vs 2026 rosters)

Per on-chain proposal metadata ([[sources/tweag-core-cardano-infrastructure-2026-2028]], [[sources/tweag-core-cardano-infrastructure-2026-2027]], same text as Cardano Vision admin for **2025 TRSC**):

| Member | Role |
|--------|------|
| [[entities/sundae-labs|Sundae Labs]] | One of five **trusted entities** on TRSC/PSSC |
| **Cardano Foundation** | Same — independent verification of admin actions |
| Dquadrant | Same |
| Xerberus | Same (2025 roster only) |
| NMKR | Same |

**2026 TRSC** deployments ([[sources/withdraw-hardware-wallet-maintenance-2026]]) use a **six-member** Oversight Committee: Sundae Labs, Cardano Foundation, Dquadrant, NMKR, Sundial, **[[entities/eternl|Eternl]]** — Xerberus replaced. Sign-off thresholds scale to 2/6 and 3/6 for Fund/Modify and Disburse respectively.

**What the Foundation does here:** Co-sign selected on-chain TRSC/PSSC operations (e.g. two of five trusted entities for Fund/Modify; three of five for Disperse and Reorganize) alongside Intersect admins and leadership. Purpose: verify administrative actions for accuracy and consistency **without discretion over governance decisions**.

**What the Foundation does not do in this proposal:**

- Not proposer, contractor, or delivery party (those are Tweag and Intersect/CDH respectively)
- Not metadata author (Intersect witnesses governance metadata)
- Not the **third-party assurer** who signs off technical milestones against the legal contract (separate role, funded from proposal overhead; **No Witness Labs** named in [[sources/tweag-core-cardano-infrastructure-2026-2027]])
- Not named in the Tweag PDF body for technical workstreams (no TSC/delivery role documented there)

## Related votes

- [[proposals/pebble-ecosystem-maintenance-2026]]
- [[proposals/cardano-vision-2026]] — Intersect/CDH-administered TRSC/PSSC with Oversight Committee and 3rd-party assurer
- [[proposals/tweag-core-cardano-infrastructure-2026-2027]] — same Intersect administration model; No Witness Labs as 3rd-party assurer
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]] — same Intersect administration model as Cardano Vision 2026
- [[concepts/treasury-proposal-bundling]] — governance-action granularity vs milestone-level escrow control
- [[proposals/eternl-path-to-sustainability-2026-2027]] — self-administered operational grant with revenue payback (no milestone escrow)
- [[proposals/cardano-critical-integrations-v2]] — Pentad Steering Committee + Intersect TRSC for recurring integration maintenance
- [[proposals/5am-earth-trust-layer-vision-2030-kpis]] — Intersect TRSC; 5/2/3 milestone schedule; public on-chain KPI dashboard
- [[proposals/hardware-wallet-maintenance-2026]] — Intersect 2026 TRSC; Ledger/Trezor + cardano-hw-cli maintenance; updated six-member Oversight Committee
- [[proposals/wirex-real-world-payments]] — Intersect 2026 TRSC; Wirex Visa card + open-source payments infrastructure; same six-member Oversight Committee
- [[proposals/technical-steering-committee-support-2026]] — Intersect 2026 TRSC; 12-month TSC governance support and pilot independent technical review
- [[proposals/intersect-governance-coordination-and-technical-stewardship-2026]] — Intersect 2026 TRSC; ₳25.4M operations + technical stewardship + incident response
- [[proposals/bifrost-road-to-mainnet-phase-1]] — Intersect-administered escrow pattern is referenced; proposal also details milestone gates, independent oversight, and refundable contingency mechanics
- [[proposals/cardano-builder-dao]] — dRep DAO council multisig administrator; CB DAO smart-contract sub-allocation to funded builders
- [[proposals/revised-cardano-dospo-and-omf-program-2026]] — Article II.7.5 sole administrator; advisory councils + Mill Law audit; no TRSC escrow
- [[proposals/scalus-2026]] — SundaeSwap vendor escrow; Gianelloni/Benkort/Kilgore oversight board; No.Witness Labs assurance
- [[proposals/global-order-book-defi-kernel]] — Minswap Labs off-chain budget administrator (no TRSC)
- [[proposals/alchemy-cardano-native-bitcoin-treasury]] — Intersect interim administrator; separated liquidity/delivery pools
- [[concepts/hardware-wallet-interoperability]] — CIP-21 signing constraints maintained by treasury-funded tooling
- [[concepts/real-world-payments]] — merchant spend rails complementing stablecoin and L2 layers

## Open questions

- What exact on-chain scripts and parameters are used for each treasury-funded proposal?
- How are technical acceptance criteria independently verified when they require domain expertise?
- What is the practical difference between Intersect/CDH-administered treasury controls and proposer-specific escrow boards (e.g. Pebble's HLabs oversight board)?
