# Pebble

**Pebble** is a Cardano smart-contract language developed by [[entities/harmonic-labs|Harmonic Labs]] that targets UPLC and is presented as a TypeScript-shaped, imperative-first alternative to functional-first tooling such as Aiken.

## Position

The Pebble treasury proposal argues that Cardano lacks a polished imperative smart-contract option for developers coming from TypeScript, JavaScript, Solidity, Rust, Go, or similar ecosystems. It positions Pebble as complementary to Aiken rather than a replacement: both compile to UPLC, but each serves a different developer mental model.

## Claimed advantages

- **Paradigm fit:** naturally imperative algorithms can be written with explicit state, control flow, and stepwise transformations instead of being encoded into functional patterns.
- **Developer onboarding:** TypeScript-shaped syntax is meant to reduce friction for Web2 and EVM/Solidity developers learning Cardano's eUTxO model.
- **Performance:** the proposal says published UPLC-CAPE benchmarks show Pebble strictly outperforming equivalent Aiken contracts and approaching hand-tuned Plutarch while staying readable.
- **Tooling:** planned work includes LSP support, autocompletion, go-to-definition, inline diagnostics, watch-mode CLI, REPL, sourcemaps, and blueprint generation.

## Delivery path

In [[proposals/pebble-ecosystem-maintenance-2026]], Pebble receives 3.5 of the 5 proposed FTEs. Milestones cover type-system completion, example contracts, Plutus V4 codegen, standard library/test framework expansion, benchmark submissions, developer tooling, documentation, tutorials, and onboarding guides for TypeScript and Solidity developers.

## Notes and contradictions

The proposal predominantly describes Pebble as **imperative-first**. In the detailed budget section, it also calls Pebble "a simple, yet rock solid, functional language with an imperative bias." This should be treated as a wording inconsistency unless clarified by Harmonic Labs.

## Related votes

- [[proposals/pebble-ecosystem-maintenance-2026]]

## Open questions

- Which UPLC-CAPE benchmark categories currently include Pebble, and which are still missing?
- How mature are Pebble's compiler, standard library, docs, and LSP today compared with the proposed end state?
- What production contracts, if any, are already written in Pebble?
