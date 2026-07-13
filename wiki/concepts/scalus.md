# Scalus

**Scalus** is an open-source, JVM-native Cardano development platform built by [[entities/lantr-engineering|Lantr Engineering]] — integrating smart contract language, transaction building, enterprise testing, in-memory node emulation, and (in funded continuation work) an application runtime.

## Position

Scalus targets **mission-critical applications** where correctness, performance, and operational control matter: L2 systems, bridges, DEXs, synthetic assets, and identity protocols. Direct adopters cited in [[sources/scalus-2026-maintenance-dijkstra-readiness]] include Gummiworm L2, Bifrost, SugarRush DEX, Vela stablecoin, and DID/DIDComm.

Many teams depend on Scalus **indirectly** via embedded components in MeshJS, Lucid Evolution, Evolution SDK, Cardano Client Lib, and YaciDevKit (script evaluation, cost calculation, in-memory emulator).

## Platform layers

| Layer | Capability |
|-------|------------|
| Smart contracts | Scala-native type-safe language → Plutus Core; property/scenario/state-machine testing |
| Transaction building | JVM-native; exported to JS/TS |
| Emulation | In-memory Cardano node; local devnet via Yaci Dev Kit |
| Application runtime (2026 scope) | Chain follower, event-driven workers, scheduling, persistence — bounded first release |

## Treasury funding

| Proposal | Amount | Focus |
|----------|--------|-------|
| 2025 Treasury Budget (completed) | ₳657,692 | DApps development platform |
| [[proposals/scalus-2026]] | ₳2,464,844 | Maintenance, Dijkstra readiness, interoperability, scoped runtime |

Prior larger ask (₳8.5M / 12 months full platform) was resized after DRep feedback on scope and budget.

## Competitive framing (proposer)

Lantr positions Scalus as an integrated application platform vs. contract-only DSLs (Aiken, Plutarch) and vs. SDK-only tools (MeshJS, Evolution SDK). Closest application-runtime comparison cited: Balius (Rust/WASM headless dApps).

## Related

- [[entities/lantr-engineering]]
- [[proposals/scalus-2026]]
- [[concepts/dijkstra-hard-fork]]
- [[concepts/cardano-typescript-tooling]]
- [[concepts/bifrost-bitcoin-defi-bridge]] — Bifrost built on Scalus per Phase 1 metadata
