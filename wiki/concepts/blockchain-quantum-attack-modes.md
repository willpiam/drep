---
tags: [concept]
updated: 2026-05-24
sources: [../sources/securing-elliptic-curve-cryptocurrencies.md]
---

# Blockchain quantum attack modes

**Blockchain quantum attack modes** classify how a cryptographically relevant quantum computer can exploit quantum-vulnerable cryptography in distributed ledgers. [[sources/securing-elliptic-curve-cryptocurrencies]] defines three operational categories: on-spend, at-rest, and on-setup attacks.

## Position

For Cardano governance, this taxonomy is useful because different attack modes imply different mitigations and deadlines. A full PQ migration remains the durable fix, but near-term controls should be matched to the attack class: minimize public-key exposure, rotate exposed keys, harden staking and voting credentials, and avoid quantum-vulnerable trusted setups in new protocol features.

## Attack classes

- **On-spend attacks** target transactions in flight after a public key is revealed but before settlement. Fast-clock CRQCs such as superconducting, silicon, or photonic architectures are the main concern.
- **At-rest attacks** target public keys exposed onchain or offchain for long periods. Slow-clock CRQCs may still be sufficient because the attacker has days or longer.
- **On-setup attacks** target fixed public protocol parameters, such as trusted setup outputs or ECDLP-based commitment parameters. A one-time quantum computation can produce a reusable classical exploit.

## Cardano relevance

The paper classifies Cardano with UTXO/eUTXO ledgers where careful users can often keep spending public keys hidden until use, reducing at-rest exposure for ordinary funds. It still flags systemic at-rest risk from staking and voting keys exposed in registration certificates. That makes Cardano's PQ scope broader than payment signatures: it includes consensus, governance, stake credentials, voting credentials, bridge signatures, and any ZK or commitment systems adopted for scaling.

## Related votes

- [[proposals/cardano-vision-2026]] - includes PQ primitives, quantum-secure Ouroboros analysis, wallet/SPO/address compatibility, and a migration strategy.

## Open questions

- Which Cardano key types can be rotated quickly enough to mitigate at-rest exposure before full PQ migration.
- Whether governance voting keys need emergency rotation or sunset mechanisms as part of PQ readiness.
- Which planned ZK, bridge, or data-availability features might introduce on-setup risk.
