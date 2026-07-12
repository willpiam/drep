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

## Wallet-native TypeScript stacks

[[entities/eternl|Eternl]] is rewriting its core with a **custom TypeScript CBOR library** (planned BUSL-1.1 release to npm under `@eternl`), replacing CSL across the codebase per [[proposals/eternl-path-to-sustainability-2026-2027]]. This is parallel infrastructure to the Harmonic Labs ledger/UPLC stack — wallet-local encoding and transaction building rather than shared protocol libraries — but it expands the TypeScript dependency surface for Cardano client software.

## Downstream dependencies

The proposal names Mesh, Lucid Evolution, and Midgard as downstream projects that depend on the Harmonic Labs stack directly or transitively. It also points to wallet integrations, indexers, dApp backends, and other production projects as affected consumers.

## Hosted API layer (Blockfrost)

[[entities/blockfrost|Blockfrost]] is complementary to in-process TypeScript libraries: it provides a **hosted REST API** for chain reads and transaction submission so teams avoid running nodes. Per [[sources/blockfrost-transformation-to-not-for-profit]], it is the **#1 hosted platform** in the Cardano Foundation developer survey (71.5% in 2025) and carries **>50% of mainnet transaction submissions** in most epochs (proposer claim). [[proposals/blockfrost-transformation-to-not-for-profit]] asks treasury support to keep the **free tier** viable under community-governed not-for-profit stewardship — a public-goods argument parallel to library maintenance, but at the infrastructure/API layer rather than npm packages.

## Governance relevance

The maintenance argument is a public-goods argument: if core library updates are not funded centrally, the proposal says the cost is pushed to each downstream team through emergency work, forks, frozen versions, or migration away from shared infrastructure. This makes the funding question partly about developer experience and partly about keeping protocol upgrades coherent across the ecosystem.

## Ecosystem-wide maintenance (dOSPO/OMF)

[[proposals/revised-cardano-dospo-and-omf-program-2026]] proposes a **cross-stack Maintenance Fund** (WP2) that would fund highest-centrality OSS — protocol libraries, wallet SDKs, developer tooling, indexers — by dependency audit rather than per-project proposals. This is complementary in scope to [[proposals/pebble-ecosystem-maintenance-2026]] (Harmonic Labs–specific) and [[proposals/blockfrost-transformation-to-not-for-profit]] (hosted API layer). The dOSPO proposer commits to deliberate non-overlap with existing programs; overlap risk with Pebble/Blockfrost/Eternl TypeScript stacks remains an open governance question.

## Related proposals

- [[proposals/blockfrost-transformation-to-not-for-profit]] — hosted API public-good transition
- [[proposals/pebble-ecosystem-maintenance-2026]] — TypeScript ledger/UPLC library maintenance
- [[proposals/revised-cardano-dospo-and-omf-program-2026]] — ecosystem-wide dependency-driven retainer fund

## Related votes

- [[proposals/pebble-ecosystem-maintenance-2026]]
- [[proposals/eternl-path-to-sustainability-2026-2027]]

## Open questions

- Which production projects depend on these libraries today, and at what depth?
- What service-level expectation should treasury-funded library maintenance satisfy during hard forks?
- How should Cardano compare direct maintenance funding with grants to downstream SDKs and applications?
