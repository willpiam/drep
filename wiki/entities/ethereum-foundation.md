---
tags: [entity]
updated: 2026-05-24
sources: [../sources/securing-elliptic-curve-cryptocurrencies.md]
---

# Ethereum Foundation

**Ethereum Foundation** is the nonprofit organization that supports Ethereum research, development, and ecosystem coordination. In [[sources/securing-elliptic-curve-cryptocurrencies]], coauthor Justin Drake is affiliated with the Ethereum Foundation and the paper discusses Ethereum's active post-quantum research posture.

## Position

The paper presents Ethereum as more exposed than Bitcoin to at-rest quantum attacks because of persistent accounts, smart-contract admin keys, validator BLS signatures, and KZG data-availability commitments. It also presents Ethereum as having stronger coordination capacity for migration due to its research and roadmap institutions.

## History

Ethereum's relevant quantum surfaces include ECDSA externally owned accounts, BLS12-381 validator signatures, KZG commitments for data availability, pairing-based precompiles, bridge/admin multisigs, and L2 proof systems. The paper notes Ethereum Foundation research into post-quantum replacements for validator aggregation and protocol commitments.

## Related votes

- [[proposals/cardano-vision-2026]] - relevant comparison point for how another major PoS ecosystem organizes post-quantum protocol research.

## Open questions

- Which Ethereum post-quantum design patterns, such as hash-based aggregation or PQ precompiles, are transferable to Cardano.
- How Cardano governance should compare its own coordination capacity against Ethereum's foundation-led research model.
