# Dijkstra hard fork

The **Dijkstra hard fork** is a planned Cardano protocol upgrade cited in 2026 developer-infrastructure proposals as the next major hard-fork cycle after **[[concepts/van-rossem-hard-fork|van Rossem]]** (Protocol Version 11).

## Position

[[sources/scalus-2026-maintenance-dijkstra-readiness]] lists expected Dijkstra capabilities affecting smart contract development and ledger rules:

- **Plutus V4** support
- **Nested transactions**
- **Guard script types**
- **Accounts**

These changes impact Plutus evaluation, transaction building, testing workflows, and cost models. Developer platforms ([[concepts/scalus|Scalus]], wallets, SDKs) must track conformance ahead of activation.

## Relationship to van Rossem

| Fork | Wiki framing |
|------|--------------|
| **van Rossem** | Protocol Version 11; new Plutus builtins (CIP-109/132/133/138/153); [[proposals/update-plutus-cost-models]] |
| **Dijkstra** | Next-cycle upgrade per Scalus/Eternl proposals; Plutus V4, nested tx, accounts, guard scripts |

Exact governance action IDs and enactment sequencing for Dijkstra are not yet ingested in this wiki beyond proposer references.

## Ecosystem dependencies

- [[concepts/scalus]] — funded Dijkstra readiness and conformance testing ([[proposals/scalus-2026]])
- [[concepts/cardano-typescript-tooling]] — Mesh/Lucid/Evolution stacks embed Scalus evaluation components
- [[proposals/eternl-path-to-sustainability-2026-2027]] — wallet hard-fork support includes Dijkstra/Leios

## Related

- [[concepts/van-rossem-hard-fork]]
- [[concepts/plutus-cost-models]]
- [[concepts/scalus]]
- [[proposals/scalus-2026]]
