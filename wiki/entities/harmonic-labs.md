# Harmonic Labs

**Harmonic Labs** is a Cardano-focused R&D and engineering firm that maintains TypeScript infrastructure and develops [[concepts/pebble|Pebble]], an imperative smart-contract language targeting UPLC.

## Position

In [[sources/pebble-ecosystem-maintenance-typescript-core-cardano]], Harmonic Labs argues that Cardano needs both a production-ready imperative smart-contract language and reliable maintenance of the TypeScript libraries many downstream projects depend on. Its stated mission is to make decentralization the baseline of application development rather than an optional feature.

## Treasury proposals

- [[proposals/pebble-ecosystem-maintenance-2026]] — 4,600,000 ADA ask for Pebble and TypeScript ecosystem maintenance.
- The source also notes a separate Gerolamo light-node proposal funded and voted on independently.

## Maintained / proposed work

| Area | Role in proposal |
|------|------------------|
| Pebble | Production-ready imperative smart-contract language and developer tooling |
| `cardano-ledger-ts` | Cardano ledger data structures and protocol semantics |
| `ouroboros-miniprotocols-ts` | TypeScript implementation of Ouroboros networking protocol pieces |
| `plutus-machine` | CEK machine implementation for UPLC evaluation |
| `uplc` | TypeScript/JavaScript representation of UPLC |

## Related votes

- [[proposals/pebble-ecosystem-maintenance-2026]] — DRep position not yet recorded; local vote context is still a placeholder.

## Open questions

- How much current ecosystem dependency on Harmonic Labs libraries is direct versus transitive?
- What hard-fork support has Harmonic Labs delivered historically, and how quickly did downstream projects adopt those releases?
- How should the DRep compare this ask with other 2026 developer-platform and language-tooling proposals?
