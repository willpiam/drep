# Pebble & Ecosystem Maintenance: TypeScript Core of Cardano

**Raw:** [../raw/bafybeieue5eog4liyxefxvtkft3nw42eshx447l4h6x43vf2r235ypviqi.json](../raw/bafybeieue5eog4liyxefxvtkft3nw42eshx447l4h6x43vf2r235ypviqi.json)  
**Ingested:** 2026-05-25

## Summary

Harmonic Labs proposes a 12-month treasury withdrawal of **4,600,000 ADA** for two connected workstreams: making [[concepts/pebble|Pebble]] a production-ready imperative smart-contract language for Cardano, and maintaining the [[concepts/cardano-typescript-tooling|TypeScript infrastructure]] used by downstream projects such as Mesh, Lucid Evolution, and Midgard. The proposal frames Pebble as a TypeScript-shaped on-ramp for Web2, EVM, and Solidity developers, while positioning hard-fork maintenance as non-optional ecosystem infrastructure.

The ask is based on **5 FTEs** at **$200k/year**, converted at **0.25 ADA/USD**, plus a **15% refundable contingency**. Funds would be released through SundaeSwap treasury-contract escrows under milestone oversight from an independent board.

## Key points

- **Scope:** 3.5 FTE for Pebble language/tooling; 1.5 FTE for hard-fork and TypeScript library maintenance.
- **Budget:** $1,000,000 base / 4,000,000 ADA, plus 600,000 ADA refundable contingency, for a total of 4,600,000 ADA.
- **Milestones:** kickoff plus four quarterly engineering milestones from Q2 2026 through Q1 2027.
- **Pebble deliverables:** type-system finalization, Plutus V4 codegen, standard library/test framework expansion, UPLC-CAPE benchmark submissions, REPL, sourcemaps, documentation, tutorials, and migration guides.
- **Maintenance deliverables:** hard-fork-ready releases for `cardano-ledger-ts`, `ouroboros-miniprotocols-ts`, `plutus-machine`, and `uplc`.
- **Governance controls:** SundaeSwap `treasury.ak` / `vendor.ak` escrow, independent oversight board, pause/resume controls, public reports, public transaction journal, and auto-abstain/no-SPO delegation while funds are escrowed.
- **Constitutional framing:** the proposal argues that it meets treasury withdrawal standards on purpose, auditability, administrators, delegation, ADA denomination, and Net Change Limit constraints.

## Wiki updates

- Created [[proposals/pebble-ecosystem-maintenance-2026]]
- Created [[entities/harmonic-labs]]
- Created [[concepts/pebble]]
- Created [[concepts/cardano-typescript-tooling]]
- Created [[concepts/treasury-escrow-oversight]]
- Updated [[overview]]
