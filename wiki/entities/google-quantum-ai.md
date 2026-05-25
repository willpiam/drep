---
tags: [entity]
updated: 2026-05-24
sources: [../sources/securing-elliptic-curve-cryptocurrencies.md]
---

# Google Quantum AI

**Google Quantum AI** is Google's quantum computing research organization. In [[sources/securing-elliptic-curve-cryptocurrencies]], most authors are affiliated with Google Quantum AI and present updated resource estimates for quantum attacks on secp256k1 ECDLP.

## Position

The paper argues that CRQC risk to cryptocurrency systems is close enough to require immediate post-quantum migration planning. It also argues for a responsible-disclosure posture in quantum cryptanalysis: publish enough resource data to motivate defense, but withhold detailed attack circuits that could accelerate misuse.

## History

The 2026 paper reports secp256k1 ECDLP circuits with about 1,200 logical qubits and 90M Toffoli gates or about 1,450 logical qubits and 70M Toffoli gates, then maps those estimates to a superconducting surface-code setting with fewer than half a million physical qubits under stated assumptions.

## Related votes

- [[proposals/cardano-vision-2026]] - external support for the urgency of Cardano post-quantum planning.

## Open questions

- Whether future Google Quantum AI resource estimates will include Ed25519, ECVRF, BLS, or Cardano-specific protocol primitives.
- How much detail can be disclosed responsibly for Cardano-relevant cryptanalysis while still enabling governance to assess urgency.
