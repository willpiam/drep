# Pebble & Ecosystem Maintenance 2026

**Type:** Treasury withdrawal (developer tooling and ecosystem maintenance)  
**Proposer:** [[entities/harmonic-labs|Harmonic Labs]]  
**Administrator / escrow:** SundaeSwap treasury-contracts with independent oversight board  
**Source:** [[sources/pebble-ecosystem-maintenance-typescript-core-cardano]]

This proposal asks for **4,600,000 ADA** over 12 months to fund [[concepts/pebble|Pebble]], a TypeScript-shaped imperative smart-contract language for Cardano, and ongoing maintenance of [[concepts/cardano-typescript-tooling|Harmonic Labs' TypeScript stack]]. The proposal argues that Pebble expands Cardano's developer on-ramp beyond functional-first tooling, while the maintenance track keeps production projects aligned with protocol upgrades.

## Context

| Item | Detail |
|------|--------|
| Total ask | 4,600,000 ADA |
| Base budget | $1,000,000 / 4,000,000 ADA |
| Contingency | 600,000 ADA, described as refundable |
| Duration | 12 months, Q2 2026 through Q1 2027 after kickoff |
| Staffing model | 5 FTE total: 3.5 Pebble, 1.5 hard-fork/tooling maintenance |
| Conversion rate | 0.25 ADA/USD |

## Workstreams

### Pebble language and tooling

Pebble is presented as a missing imperative smart-contract language for Cardano. The proposal claims Pebble is better suited than Aiken for developers who think in TypeScript, Solidity, Rust, Go, or other imperative languages, while still compiling to UPLC. Planned outputs include type-system completion, Plutus V4 codegen, a built-in test framework, standard library expansion, UPLC-CAPE benchmark coverage, REPL support, sourcemaps, LSP/IDE improvements, documentation, and end-to-end tutorials.

### TypeScript ecosystem maintenance

The maintenance track covers hard-fork and protocol-upgrade support for:

- `cardano-ledger-ts`
- `ouroboros-miniprotocols-ts`
- `plutus-machine`
- `uplc`

The proposal frames these libraries as dependencies for Mesh, Lucid Evolution, Midgard, wallet integrations, indexers, and dApp backends. Its central risk claim is that underfunded maintenance would push upgrade costs to many downstream teams through forks, frozen versions, or emergency migrations.

## Milestones

| Milestone | Window | Focus | Payment |
|-----------|--------|-------|---------|
| M0 | Kickoff / enactment | Escrow deployment and project initialization | 400,000 ADA |
| M1.A | Q2 2026 | Pebble type system, example contracts | 840,000 ADA |
| M1.B | Q2 2026 | Hard-fork-ready library releases | 210,000 ADA |
| M2 | Q3 2026 | Language completeness, Plutus V4 codegen, benchmarks | 1,050,000 ADA |
| M3 | Q4 2026 | REPL, sourcemaps, Buildooor integration, maintenance | 1,050,000 ADA |
| M4 | Q1 2027 | Reference docs, tutorials, TS/Solidity onboarding | 1,050,000 ADA |

Acceptance criteria generally point to public artifacts: npm releases, GitHub releases, CI status, committed logs or transaction links, UPLC-CAPE entries, benchmark write-ups, and published documentation.

## Governance and controls

Funds would be held through the SundaeSwap treasury-contract framework using `treasury.ak` and `vendor.ak`, with milestone disbursement controlled by [[concepts/treasury-escrow-oversight|escrow and oversight rules]]. The named oversight board is Santiago Carmuega, Lucas Rosa, and Chris Gianelloni. The proposal says board members have no stake in HLabs, can co-sign or pause milestone releases, and review monthly updates, quarterly reports, and public transaction-journal entries.

The escrow policy includes auto-abstain DRep delegation and no SPO delegation for funds held in escrow, so treasury funds do not influence governance votes or staking.

## DRep position

No completed DRep vote context is currently recorded. `vote_context/markdown/54_pebble.md` exists as a placeholder with empty summary and conclusion fields, so the wiki should not infer a vote until the published context is filled.

## Open questions

- What is the exact governance action ID once the action is on-chain?
- How should DRep evaluation weigh Pebble's claimed UPLC-CAPE performance against the current completeness of benchmark coverage?
- Are the adoption targets for Pebble, such as >=20 developers and >=3 tutorials, sufficient for a 4.6M ADA ask?
- How independently can the oversight board verify technical acceptance criteria like Plutus V4 support and hard-fork readiness?
- What refund mechanics apply to unused contingency after milestone completion or expiration?

## Related

- [[entities/harmonic-labs]]
- [[concepts/pebble]]
- [[concepts/cardano-typescript-tooling]]
- [[concepts/treasury-escrow-oversight]]
