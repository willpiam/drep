---
tags: [source]
updated: 2026-05-24
sources: [../raw/2603.28846v2.pdf]
---

# Securing Elliptic Curve Cryptocurrencies against Quantum Vulnerabilities: Resource Estimates and Mitigations

**Raw:** [../raw/2603.28846v2.pdf](../raw/2603.28846v2.pdf)
**Ingested:** 2026-05-24

## Summary

Ryan Babbush, Adam Zalcman, Craig Gidney, Michael Broughton, Tanuj Khattar, Hartmut Neven, Thiago Bergamaschi, Justin Drake, and Dan Boneh analyze how cryptographically relevant quantum computers (CRQCs) affect cryptocurrencies that rely on elliptic-curve cryptography. The authors provide updated resource estimates for breaking secp256k1 ECDLP and survey practical attack surfaces across Bitcoin, Ethereum, Cardano, privacy chains, stablecoins, real-world asset tokenization, and post-quantum blockchain deployments.

The headline technical claim is that Shor's algorithm against 256-bit secp256k1 can be compiled to either about 1,200 logical qubits and 90 million Toffoli gates, or about 1,450 logical qubits and 70 million Toffoli gates. Under stated superconducting surface-code assumptions, the authors estimate execution in minutes using fewer than half a million physical qubits. They publish a zero-knowledge proof attesting to point-addition circuit resource bounds without disclosing the full attack circuit.

For [[concepts/post-quantum-cardano]], the most relevant contribution is the paper's taxonomy of blockchain quantum attack modes. It distinguishes fast-clock CRQCs that could enable on-spend attacks from slow-clock CRQCs that may first enable at-rest attacks. It also calls out Cardano as an eUTXO ledger where users can often avoid long-term spending-key exposure, while staking and voting keys create systemic at-rest risk because they are exposed through registration certificates.

## Key points

- **Resource estimate:** secp256k1 ECDLP is estimated at about 1,200 logical qubits / 90M Toffoli gates or 1,450 logical qubits / 70M Toffoli gates, with fewer than 500k physical qubits under the authors' stated superconducting assumptions.
- **Responsible disclosure:** the paper argues that improved quantum cryptanalysis should move toward responsible disclosure; it uses a ZK proof to substantiate resource claims while withholding attack-circuit details.
- **Attack modes:** [[concepts/blockchain-quantum-attack-modes]] separates on-spend attacks against transactions in flight, at-rest attacks against long-exposed public keys, and on-setup attacks against fixed cryptographic parameters such as trusted setups.
- **Architecture matters:** fast-clock platforms such as superconducting, silicon, or photonic CRQCs are treated as plausible on-spend attackers, while slower neutral-atom and ion-trap platforms may initially be limited to at-rest attacks.
- **Timeline posture:** the paper does not give a calendar forecast for CRQC arrival; it frames timing as uncertain, architecture-dependent, and potentially opaque as cryptanalytic capabilities approach deployment.
- **Bitcoin risk:** public-key exposure through P2PK, P2TR, address reuse, public mempools, and offchain reuse creates both at-rest and on-spend risk; dormant assets create unresolved policy questions around burn, hourglass, and digital salvage.
- **Ethereum risk:** the account model, admin keys, smart-contract code, BLS validator signatures, and KZG data-availability commitments create broad at-rest and on-setup vulnerabilities affecting funds, validators, L2s, RWAs, and stablecoins.
- **Cardano note:** the paper places Cardano in the category of UTXO/eUTXO ledgers where spending-key exposure can be minimized, but flags staking and voting keys as at-rest vulnerabilities with consensus and governance implications.
- **Migration lesson:** PQC migration is feasible but costly; larger signatures, new libraries, governance coordination, and long-tail dormant assets mean the process must begin before CRQCs are publicly confirmed.
- **Tension with ladders:** the paper cites the [[concepts/ecdlp-challenge-ladder]] but warns that ladder demonstrations may not be reliable early warnings if quantum progress arrives through threshold-style scaling jumps or remains non-public.

## Wiki updates

- Created [[entities/google-quantum-ai]]
- Created [[entities/ethereum-foundation]]
- Created [[concepts/blockchain-quantum-attack-modes]]
- Updated [[concepts/quantum-cryptanalysis]]
- Updated [[concepts/ecdlp-challenge-ladder]]
- Updated [[concepts/post-quantum-cardano]]
- Updated [[concepts/cardano-vision]]
