---
tags: [concept]
updated: 2026-05-24
sources: [../sources/brace-for-impact-ecdlp-challenges.md, ../sources/securing-elliptic-curve-cryptocurrencies.md]
---

# ECDLP challenge ladder

An **ECDLP challenge ladder** is a difficulty-graded suite of elliptic-curve discrete logarithm problem instances used to track progress in classical and quantum attacks. In [[sources/brace-for-impact-ecdlp-challenges]], the ladder keeps Bitcoin's secp256k1 curve shape while shrinking the prime field from 256 bits down to 6 bits.

## Position

The DRep relevance is as a warning instrument: public, reproducible benchmarks can turn vague quantum-risk debate into observable milestones. A Cardano migration roadmap should not wait for the economically significant 256-bit rung; the paper frames the 160-bit rung as an important warning point.

## History

The Pauli Group paper constructs each rung deterministically:

- Select a k-bit prime field for the curve `y^2 = x^3 + 7`.
- Require prime group order, so every non-identity point generates the group.
- Derive two nothing-up-my-sleeve points from the labels "Quantum" and "Challenge".
- Publish the task as recovering `kappa` such that `P = [kappa]Q`.

This differs from interval-restricted Bitcoin puzzles, which constrain the secret to a range and map naturally to Pollard's kangaroo. Shor's algorithm for full ECDLP does not gain the same benefit from interval restriction, so the ladder is intended to be a cleaner benchmark for fault-tolerant quantum progress.

## Cardano relevance

The published ladder is secp256k1-specific, not Cardano-specific. Still, the benchmarking pattern is useful for [[concepts/post-quantum-cardano]] because it shows how to make threat progress auditable: define canonical instances, publish reproducible parameters, and tie milestones to migration urgency.

## Tension

[[sources/securing-elliptic-curve-cryptocurrencies]] challenges the ladder's value as an early-warning mechanism. It argues that quantum progress may arrive as a threshold jump: an architecture could solve small ECDLP rungs only shortly before it can solve 256-bit ECDLP, and the most advanced cryptanalytic demonstrations may never be published. Under that view, a public 32-bit or 64-bit ECDLP demonstration might signal that migration is already late, not that there is still comfortable time.

## Related votes

- [[proposals/cardano-vision-2026]] - Cardano Vision includes PQ primitives, quantum-secure Ouroboros modeling, and migration strategy deliverables.

## Open questions

- Whether a comparable challenge ladder is needed for Cardano's Ed25519/ECVRF or related protocol primitives.
- What milestone should trigger governance escalation from research to migration activation.
