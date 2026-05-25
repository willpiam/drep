# Cardano Vision 2026 — IO Research (draft)

**Raw:** [../raw/bafybeigixg5u5tmsd7fgwy536wx6apq2cxesrklo47vmywe67nknwyshoy.pdf](../raw/bafybeigixg5u5tmsd7fgwy536wx6apq2cxesrklo47vmywe67nknwyshoy.pdf)  
**Ingested:** 2026-05-24  
**Status:** DRAFT FOR COMMUNITY REVIEW  
**Gov action:** [gov_action1ttgs45ulfxs0jwkfrecystc3flduhszmyzk8wnd7yw5za77tsg9qq4afmus](https://cardanoscan.io/govAction/gov_action1ttgs45ulfxs0jwkfrecystc3flduhszmyzk8wnd7yw5za77tsg9qq4afmus)

## Summary

Year-two treasury proposal from [[entities/io-research|IO Research]] (IOR) for **Cardano Vision 2026**: a ₳32.917M (~$7.9M) research and technology-validation program spanning 36 FTEs across seven work packages. The document reframes IOR’s mission around an integrated **IOR → ARC → CBU** delivery pipeline (fundamental research through prototypes to product alignment), with three cross-cutting themes: **post-quantum security**, **scalable architecture**, and **human-centred design**.

The 2025 Cardano Vision withdrawal passed with ₳4.16B in favour (79.81%). IOR reports 2025 delivery: 20 research streams, 24 peer-reviewed papers (+20% vs target), and eight technology-validation streams (Leios prototype + CIP handoff, Phalanx formalisation, Jolteon prototype, RSnarks on-chain feasibility, etc.). Vision 2026 emphasises improving **research-to-deployment conversion** (~20% of 250+ IOR papers historically implemented).

Funding is administered by [[entities/intersect|Intersect]] via treasury smart contracts; legal contract between Input Output and Cardano Development Holdings (CDH). Four equal 25% tranches tied to service agreement, mid-year report, Q3 R&D session, and year-end report.

## Key points

- **Budget:** ₳32,916,667 total; ~$219.5k/FTE/year; 19.5 IOR + 17.5 ARC FTEs (WP7 delivery absorbed in-kind by IOG).
- **Strategic themes:** Post-quantum migration (signatures, VRFs, Ouroboros analysis); scalability (Leios, Peras, L2/ZK, sharding feasibility, DA); human-centred (Plutus verification, light clients/Cavefish, Babel fees/intents, governance incentives, proof of personhood).
- **WP1 (8.3 FTE):** Consensus/MEV/Leios–Peras analysis; post-quantum primitives and migration roadmap; node security (HSM, MPC). Excludes production hard-fork work (IO Consensus Initiative).
- **WP2 (9.9 FTE):** Fee markets, L2 data availability, sharding study, P2P hardening + pub/sub, ZK verification + Hydra Tail rollup analysis.
- **WP3 (5.7 FTE):** Verifying Plutus compiler, light clients, Babel fee market design (excludes CIP-118 production in separate IO upgrade proposal).
- **WP4 (3.6 FTE):** Bridge formal security, atomic swaps, agent chains (excludes Intersect ZK bridge treasury items).
- **WP5 (3.7 FTE):** SPO incentive recalibration, multi-resource consensus/PoUW, utility-weighted throughput metrics.
- **WP6 (2.5 FTE):** Governance incentives + DAO DSL; Sybil-resistant identity and verifiable credentials.
- **WP7:** Program management and dissemination (R&D sessions, CIP translation); in-kind.
- **Ecosystem KPIs cited:** 27M monthly transactions, 3× throughput, 2030 adoption objectives.
- **Ouroboros roadmap in doc:** Classic → Praos (prod) → Genesis (in dev) → Omega (research); Peras/Leios deployment readiness targeted 2026.
- **Prior IOR treasury:** ₳26.84M allocated (100% of prior workstream); ₳78.46M total IOG withdrawals from ₳130.7M allocated across workstreams.
- **Compliance:** NCL guardrail TREASURY-02a; unspent funds returned; IPFS immutable hosting with blake2b-256 hash on-chain.

## Wiki updates

- Created [[sources/cardano-vision-2026-ior]]
- Created [[proposals/cardano-vision-2026]]
- Created [[entities/io-research]], [[entities/input-output-group]], [[entities/intersect]]
- Created [[concepts/cardano-vision]], [[concepts/post-quantum-cardano]], [[concepts/ouroboros]], [[concepts/leios]], [[concepts/research-delivery-pipeline]]
- Updated [[overview]], [[index]]
