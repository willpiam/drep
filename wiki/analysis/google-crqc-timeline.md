# Google CRQC Timeline

**From query:** 2026-05-25
**Question:** When does the Google paper say we will have cryptographically relevant quantum computers?

## Answer

The Google/Ethereum/Stanford paper does **not** give a specific calendar date or forecast window for when cryptographically relevant quantum computers (CRQCs) will exist. Its timeline claim is qualitative: CRQC arrival is uncertain, may depend on which hardware architecture scales first, and could become less publicly visible as systems approach commercial or cryptanalytic relevance.

The paper recommends planning around two scenarios: fast-clock architectures, such as superconducting, silicon, or photonic systems, may make on-spend and at-rest attacks viable at roughly the same time; slower neutral-atom or ion-trap systems may make at-rest attacks viable before on-spend attacks. It also warns that public ECDLP challenge demonstrations may not provide comfortable early warning, because quantum progress may arrive through threshold-style scaling jumps and advanced cryptanalytic demonstrations may remain unpublished.

For DRep use, the answer is: **the Google paper says prepare immediately, but it does not say "CRQCs arrive in year X."** The rough 2027-2033 planning window currently tracked in [[concepts/quantum-cryptanalysis]] comes from [[sources/brace-for-impact-ecdlp-challenges]], not from this Google paper.

## Sources

- [[sources/securing-elliptic-curve-cryptocurrencies]]
- [[entities/google-quantum-ai]]
- [[concepts/quantum-cryptanalysis]]
