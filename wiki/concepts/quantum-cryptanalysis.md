---
tags: [concept]
updated: 2026-05-24
sources: [../sources/brace-for-impact-ecdlp-challenges.md, ../sources/securing-elliptic-curve-cryptocurrencies.md]
---

# Quantum cryptanalysis

**Quantum cryptanalysis** is the use of quantum algorithms, especially Shor's algorithm for factoring and discrete logarithms, to break cryptographic assumptions that are infeasible to attack with known classical algorithms. For Cardano governance, it is the threat model that motivates [[concepts/post-quantum-cardano]].

## Position

$computerman's DRep stance is that quantum cryptanalysis should be treated as an engineering coordination problem before it becomes a chain emergency. The priority is not panic, but a complete inventory of vulnerable primitives, candidate replacements, formal security analysis, and migration pathways that can be governed in time.

## History

Shor's algorithm gives an exponential quantum speedup for discrete logarithms in abelian groups, placing elliptic-curve signature systems in the long-term risk set. [[sources/brace-for-impact-ecdlp-challenges]] turns that abstract risk into a public benchmark: a secp256k1-shaped ECDLP challenge ladder calibrated against both classical records and fault-tolerant quantum resource estimates.

The paper's calibrated warning window, roughly 2027-2033 for cryptographically relevant quantum computers under explicit assumptions, should be read as a planning horizon rather than a prediction.

[[sources/securing-elliptic-curve-cryptocurrencies]] sharpens the resource side: it reports secp256k1 ECDLP circuits at about 1,200 logical qubits / 90M Toffoli gates or 1,450 logical qubits / 70M Toffoli gates, with fewer than half a million physical qubits under stated superconducting assumptions. It also argues that detailed attack circuits should be handled under responsible disclosure, using a ZK proof to substantiate the estimates without publishing the circuit.

## Cardano relevance

Cardano's exposed surfaces include signatures, VRFs, threshold schemes, bridge signatures, hardware/key-management assumptions, and the formal proofs around Ouroboros-family protocols. Quantum cryptanalysis therefore connects directly to IO Research's WP1.2 work in [[concepts/cardano-vision]] and to the migration questions tracked in [[concepts/post-quantum-cardano]].

The newer resource-estimate paper adds a governance-useful taxonomy in [[concepts/blockchain-quantum-attack-modes]] and explicitly flags Cardano staking and voting keys as at-rest risk surfaces because registration certificates expose public keys onchain.

## Related votes

- [[proposals/cardano-vision-2026]] - DRep YES; includes post-quantum R&D and a Cardano PQ readiness roadmap.

## Open questions

- Which Cardano primitives are most urgent to benchmark against quantum attacks?
- What public challenge suite would best track Cardano-relevant progress, rather than Bitcoin/secp256k1 progress alone?
- How should governance define readiness thresholds before hardware demonstrations reach higher-risk rungs?
- What disclosure norm should Cardano use for quantum cryptanalysis results that are important for governance but potentially harmful if weaponized.
