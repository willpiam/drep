---
tags: [source]
updated: 2026-05-24
sources: [../raw/2508.14011v2.pdf]
---

# Brace for impact: ECDLP challenges for quantum cryptanalysis

**Raw:** [../raw/2508.14011v2.pdf](../raw/2508.14011v2.pdf)
**Ingested:** 2026-05-24

## Summary

Pierre-Luc Dallaire-Demers, William Doyle, and Timothy Foo of [[entities/pauli-group]] propose a difficulty-graded suite of elliptic-curve discrete logarithm problem (ECDLP) challenges for tracking progress toward quantum cryptanalysis. The ladder keeps Bitcoin's secp256k1 curve shape, `y^2 = x^3 + 7`, but lowers the prime field from 256 bits down to 6 bits so that demonstrations can progress across auditable rungs.

The construction is deterministic and uses nothing-up-my-sleeve points derived from the labels "Quantum" and "Challenge" rather than from a preselected private scalar. The task on every rung is to recover the scalar `kappa` such that `P = [kappa]Q`. The paper calibrates classical difficulty against Pollard's rho records and maps Shor ECDLP circuits to surface-code, repetition-cat-code, and LDPC-cat-code resource estimates.

For governance relevance, the paper is a warning signal for [[concepts/post-quantum-cardano]]: public-key cryptography can move from "long-term research risk" to "migration deadline" once fault-tolerant quantum hardware reaches the middle and upper rungs of the ladder. Its concrete case study is Bitcoin, but the planning lesson transfers to Cardano's signature, VRF, threshold, and protocol-proof upgrade surfaces.

## Key points

- The challenge ladder spans 6, 8, 12, 16, 24, 32, 48, 64, 80, 96, 112, 128, 144, 160, 176, 192, 208, 224, 240, and 256-bit instances on secpkk1-style curves.
- Each rung provides the field prime, prime group order, and two deterministic compressed SEC1 points; no private challenge scalar is sampled or hidden by the authors.
- Classical calibration treats Pollard's rho as the generic baseline, with practical records clustering around 112-120 bits for full ECDLP. Interval-restricted Bitcoin puzzles are useful engineering signals but are not equivalent to full 256-bit ECDLP under Shor's algorithm.
- Quantum calibration uses HJNRS-style Shor ECDLP logical circuits and maps them to multiple physical assumptions. The 256-bit rung ranges from aggressive surface-code estimates below one million physical qubits to cat-code estimates around `1.26e5` repetition cat qubits or `3.86e4` LDPC cat qubits, with hours-to-days runtimes depending on assumptions.
- The paper frames 6-bit ECDLP as an early end-to-end fault-tolerant demonstration target, 160 bits as a serious warning milestone, and 256 bits as the economically consequential target.
- The authors place a plausible cryptographically relevant quantum computer window around 2027-2033, while stressing that this is a calibrated overlay rather than a prediction.
- Bitcoin migration discussion highlights exposed public keys, BIP 360/P2QRH, commit-then-upgrade patterns, hybrid signatures, and staged migration. For Cardano, the analogous lesson is to complete primitive assessment and protocol migration planning before visible hardware milestones force emergency governance.

## Wiki updates

- Created [[entities/pauli-group]]
- Created [[concepts/quantum-cryptanalysis]]
- Created [[concepts/ecdlp-challenge-ladder]]
- Updated [[concepts/post-quantum-cardano]]
- Updated [[concepts/cardano-vision]]
