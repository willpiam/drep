# Cardano TypeScript Tooling

**Cardano TypeScript tooling** refers to the JavaScript/TypeScript libraries, SDKs, protocol encoders, ledger types, and UPLC evaluators used by Cardano wallets, dApps, indexers, and infrastructure projects.

## Position

[[sources/pebble-ecosystem-maintenance-typescript-core-cardano]] frames [[entities/harmonic-labs|Harmonic Labs']] TypeScript stack as load-bearing infrastructure for the Cardano application ecosystem. The proposal argues that maintenance is especially important around hard forks, when protocol parameter changes, Plutus version changes, and ledger semantics must be reflected in libraries before downstream projects can safely upgrade.

## Libraries named in the proposal

| Library | Role |
|---------|------|
| `cardano-ledger-ts` | Cardano ledger data structures and protocol semantics |
| `ouroboros-miniprotocols-ts` | TypeScript implementation of Ouroboros networking mini-protocols |
| `plutus-machine` | CEK machine implementation for UPLC evaluation |
| `uplc` | TypeScript/JavaScript representation of UPLC |

## Downstream dependencies

The proposal names Mesh, Lucid Evolution, and Midgard as downstream projects that depend on the Harmonic Labs stack directly or transitively. It also points to wallet integrations, indexers, dApp backends, and other production projects as affected consumers.

## Governance relevance

The maintenance argument is a public-goods argument: if core library updates are not funded centrally, the proposal says the cost is pushed to each downstream team through emergency work, forks, frozen versions, or migration away from shared infrastructure. This makes the funding question partly about developer experience and partly about keeping protocol upgrades coherent across the ecosystem.

## Related votes

- [[proposals/pebble-ecosystem-maintenance-2026]]

## Open questions

- Which production projects depend on these libraries today, and at what depth?
- What service-level expectation should treasury-funded library maintenance satisfy during hard forks?
- How should Cardano compare direct maintenance funding with grants to downstream SDKs and applications?
