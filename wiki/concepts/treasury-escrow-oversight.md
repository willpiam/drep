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

## Related votes

- [[proposals/pebble-ecosystem-maintenance-2026]]
- [[proposals/cardano-vision-2026]] — Intersect/CDH-administered TRSC/PSSC with Oversight Committee and 3rd-party assurer
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]] — same Intersect administration model as Cardano Vision 2026

## Open questions

- What exact on-chain scripts and parameters are used for each treasury-funded proposal?
- How are technical acceptance criteria independently verified when they require domain expertise?
- What is the practical difference between Intersect/CDH-administered treasury controls and proposer-specific escrow boards (e.g. Pebble's HLabs oversight board)?
