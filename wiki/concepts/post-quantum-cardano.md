# Post-quantum Cardano

**Post-quantum (PQ) security** for Cardano means migrating protocol cryptography—signatures, VRFs, threshold schemes, and dependent consensus proofs—so the network remains secure against large-scale quantum adversaries. Current primitives (e.g. Ed25519, ECVRF) are not quantum-safe.

## Why it matters for governance

$computerman's [2025 roadmap feedback](../../vote_context/markdown/7a_roadmap.md) stated that including **Post Quantum R&D** in the product roadmap would be enough to change a tentative NO vote to YES, citing Charles Hoskinson's public framing and the need for an inventory of upgrade surfaces, competing hash- and lattice-based approaches, and domain-specific signature design--not only disaster recovery.

Cardano Vision 2026 elevates PQ to a **cross-cutting strategic theme** and dedicates WP1.2 to it.

## External warning signal

[[sources/brace-for-impact-ecdlp-challenges]] proposes a reproducible [[concepts/ecdlp-challenge-ladder]] for tracking [[concepts/quantum-cryptanalysis]] against Bitcoin's secp256k1 curve shape. Its concrete migration discussion is Bitcoin-specific, but its governance lesson applies directly: once public fault-tolerant demonstrations climb from toy rungs toward 160-bit and 256-bit instances, migration timelines become constrained by hardware progress rather than policy preference.

For Cardano, this reinforces the need to finish primitive assessment, quantum-secure Ouroboros modeling, wallet/address compatibility planning, and CIP-level migration design before a cryptographically relevant quantum computer is visible.

[[sources/securing-elliptic-curve-cryptocurrencies]] is more urgent. It estimates secp256k1 ECDLP attacks at fewer than half a million physical qubits under stated superconducting assumptions and warns that public challenge-ladder progress may not be a reliable early signal. It also classifies Cardano as an eUTXO ledger where cautious users can reduce spending-key at-rest exposure, while staking and voting keys remain systemic at-rest vulnerabilities because registration certificates expose public keys onchain.

## IOR 2026 program (WP1.2)

From [[sources/cardano-vision-2026-ior]]:

1. **Primitives** — Evaluate PQ signatures, VRFs, threshold schemes; develop PQ VRF with formal proof (major challenge: proof size, verification cost, leader election).
2. **Protocol integration** — Quantum-secure Ouroboros modelling and formal security under quantum adversaries; prototypes and benchmarks.
3. **Migration** — Strategies (full replacement vs incremental); wallet/SPO/address compatibility; roadmap + CIP pathway.
4. **Cross-cutting** — Node HSM/key management (WP1.3), congestion impact (WP2.1), PQ ZK systems (WP2.4), PQ threshold signatures for bridges (WP4.1).

Deliverables include CPS/report on primitive assessment, papers on PQ VRF and quantum-secure Ouroboros, and a **Cardano Post-Quantum Readiness Roadmap & Migration Strategy** (report + CIP).

## Risks noted in proposal

Performance overhead from PQ designs; limits of on-chain ZK verification; need to re-establish Ouroboros security proofs under new assumptions.

## Exposure surfaces

- **Spending keys:** eUTXO design and hash-hidden addresses can reduce at-rest exposure if users avoid reuse, but on-spend exposure remains until PQ spending paths exist.
- **Staking keys:** stake registration and delegation flows can expose long-lived public keys, creating at-rest risk for consensus and rewards.
- **Voting keys:** decentralized governance introduces public-key exposure and vote-forgery risk that should be included in PQ migration planning.
- **Advanced cryptography:** bridges, threshold signatures, ZK systems, and data-availability schemes can introduce on-setup or reusable-exploit risks if they rely on ECDLP-based commitments or trusted setups.

## Related

- [[concepts/quantum-cryptanalysis]]
- [[concepts/blockchain-quantum-attack-modes]]
- [[concepts/ecdlp-challenge-ladder]]
- [[concepts/ouroboros]]
- [[proposals/cardano-vision-2026]]
- [[entities/io-research]] — Varun Maram listed as PQ research lead (WP1)
