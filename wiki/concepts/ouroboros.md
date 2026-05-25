# Ouroboros

**Ouroboros** is Cardano’s proof-of-stake consensus family: longest-chain PoS with on-chain randomness for slot leader selection. It is the foundation of the ledger and a primary focus of [[entities/io-research|IO Research]].

## Iterations (IOR 2026 proposal)

| Variant | Status | Role |
|---------|--------|------|
| Classic | Deployed (historical) | Provably secure longest-chain PoS; unbiased on-chain randomness |
| Praos | **Production** | Private leader selection; forward-secure key evolution |
| Genesis | **In development** | Secure bootstrapping without trusted checkpoints under dynamic participation |
| Omega | Research | “Final form”: optimistic execution + multi-resource security |

**Near-term upgrades on Praos:** [[concepts/leios|Leios]] (throughput) and **Peras** (settlement latency). IOR targets deployment readiness for Peras and Leios in **2026**; production hard-fork work sits outside IOR scope (IO Consensus Initiative).

## Research themes in Vision 2026 (WP1.1)

- MEV and mempool analysis under **EUTXO** (including Linear Leios)
- Adversarial modelling and operational boundaries for Leios/Peras
- Protocol optimisation (cooldown avoidance, voting certificates, joint deployment)
- Post-quantum Ouroboros analysis ([[concepts/post-quantum-cardano]])

## DRep prior positions

[2025 roadmap feedback](vote_context/markdown/7a_roadmap.md) urged prioritising **Genesis** (near-complete, differentiation from other PoS chains) and **Chronos** (clock sync; parity with PoW security story). The Vision 2026 draft emphasises Genesis as in development but does not list Chronos as a named deliverable.

## Related

- [[concepts/leios]]
- [[concepts/cardano-vision]]
- [[sources/cardano-vision-2026-ior]]
