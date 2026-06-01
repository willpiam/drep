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

## Intersect TRSC model (Cardano Vision, Tweag)

For [[proposals/cardano-vision-2026]] and [[proposals/tweag-core-cardano-infrastructure-2026-2028]], withdrawn ADA flows through Intersect’s **Treasury Reserve Smart Contract (TRSC)** and project-specific **PSSC** contracts (Sundae Labs framework). This is a different pattern from Pebble’s vendor-specific `treasury.ak` / `vendor.ak` board above.

### Oversight Committee (includes Cardano Foundation)

Per on-chain proposal metadata ([[sources/tweag-core-cardano-infrastructure-2026-2028]], same text as Cardano Vision admin):

| Member | Role |
|--------|------|
| Sundae Labs | One of five **trusted entities** on TRSC/PSSC |
| **Cardano Foundation** | Same — independent verification of admin actions |
| Dquadrant | Same |
| Xerberus | Same |
| NMKR | Same |

**What the Foundation does here:** Co-sign selected on-chain TRSC/PSSC operations (e.g. two of five trusted entities for Fund/Modify; three of five for Disperse and Reorganize) alongside Intersect admins and leadership. Purpose: verify administrative actions for accuracy and consistency **without discretion over governance decisions**.

**What the Foundation does not do in this proposal:**

- Not proposer, contractor, or delivery party (those are Tweag and Intersect/CDH respectively)
- Not metadata author (Intersect witnesses governance metadata)
- Not the **third-party assurer** who signs off technical milestones against the legal contract (separate role, funded from proposal overhead)
- Not named in the Tweag PDF body for technical workstreams (no TSC/delivery role documented there)

## Related votes

- [[proposals/pebble-ecosystem-maintenance-2026]]
- [[proposals/cardano-vision-2026]] — Intersect/CDH-administered TRSC/PSSC with Oversight Committee and 3rd-party assurer
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]] — same Intersect administration model as Cardano Vision 2026

## Open questions

- What exact on-chain scripts and parameters are used for each treasury-funded proposal?
- How are technical acceptance criteria independently verified when they require domain expertise?
- What is the practical difference between Intersect/CDH-administered treasury controls and proposer-specific escrow boards (e.g. Pebble's HLabs oversight board)?
