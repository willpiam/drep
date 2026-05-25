# Post-quantum Cardano

**Post-quantum (PQ) security** for Cardano means migrating protocol cryptography—signatures, VRFs, threshold schemes, and dependent consensus proofs—so the network remains secure against large-scale quantum adversaries. Current primitives (e.g. Ed25519, ECVRF) are not quantum-safe.

## Why it matters for governance

$computerman’s [2025 roadmap feedback](vote_context/markdown/7a_roadmap.md) stated that including **Post Quantum R&D** in the product roadmap would be enough to change a tentative NO vote to YES, citing Charles Hoskinson’s public framing and the need for an inventory of upgrade surfaces, competing hash- and lattice-based approaches, and domain-specific signature design—not only disaster recovery.

Cardano Vision 2026 elevates PQ to a **cross-cutting strategic theme** and dedicates WP1.2 to it.

## IOR 2026 program (WP1.2)

From [[sources/cardano-vision-2026-ior]]:

1. **Primitives** — Evaluate PQ signatures, VRFs, threshold schemes; develop PQ VRF with formal proof (major challenge: proof size, verification cost, leader election).
2. **Protocol integration** — Quantum-secure Ouroboros modelling and formal security under quantum adversaries; prototypes and benchmarks.
3. **Migration** — Strategies (full replacement vs incremental); wallet/SPO/address compatibility; roadmap + CIP pathway.
4. **Cross-cutting** — Node HSM/key management (WP1.3), congestion impact (WP2.1), PQ ZK systems (WP2.4), PQ threshold signatures for bridges (WP4.1).

Deliverables include CPS/report on primitive assessment, papers on PQ VRF and quantum-secure Ouroboros, and a **Cardano Post-Quantum Readiness Roadmap & Migration Strategy** (report + CIP).

## Risks noted in proposal

Performance overhead from PQ designs; limits of on-chain ZK verification; need to re-establish Ouroboros security proofs under new assumptions.

## Related

- [[concepts/ouroboros]]
- [[proposals/cardano-vision-2026]]
- [[entities/io-research]] — Varun Maram listed as PQ research lead (WP1)
