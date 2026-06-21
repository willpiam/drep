# Tweag Core Cardano Infrastructure: Treasury Withdrawal 2026–2028

**Raw (PDF):** [../raw/tweag.pdf](../raw/tweag.pdf) — *Cardano Budget 2026-2028 - Tweag's Proposals* (2025-03-31)  
**Raw (on-chain JSON):** [../raw/bafkreifdoitcxw4anxadosoqi5y5ny647hym4u62gpyvkkuyg7wpnq6gbi.json](../raw/bafkreifdoitcxw4anxadosoqi5y5ny647hym4u62gpyvkkuyg7wpnq6gbi.json)  
**Ingested:** 2026-05-30 (JSON); **2026-06-01** (PDF milestones and budgets)  
**Full proposal (IPFS):** [ipfs://QmeXB2ZgyDSStkhPTCMwPTHCfTWU8RJJnVLc6KRKFQY4Ca](ipfs://QmeXB2ZgyDSStkhPTCMwPTHCfTWU8RJJnVLc6KRKFQY4Ca)  
**On-chain recipient:** `stake17xzc8pt7fgf0lc0x7eq6z7z6puhsxmzktna7dluahrj6g6ghh5qjr` (Intersect 2025 TRSC)  
**Deliverables map:** [[analysis/tweag-2026-2028-work-package-deliverables]]

## Summary

Treasury withdrawal from **[[entities/tweag|Tweag]] by Modus Create** requesting **₳39,787,316** (~$9.95M at ₳0.25/USD) to deliver 17 interdependent work packages across nine core infrastructure areas over **2026–2028**. The primary objective is **mainnet deployment of [[concepts/peras|Peras]]** (target ~2 min finality vs ~12 min today), supported by resilience testing, SPO storage economics ([[concepts/history-expiry|History Expiry]]), network observability ([[concepts/hoarding-node|Hoarding Node]]), developer tooling, and ongoing maintenance of Genesis Sync Accelerator and Cardano Node Emulator.

[[entities/intersect|Intersect]] is requested as proposal and contract administrator on behalf of CDH, using the same Sundae Labs TRSC/PSSC framework documented in [[sources/cardano-vision-2026-ior]]. Author witness on the JSON metadata is Intersect. All deliverables are open-source with public milestone tracking.

Tweag positions this as the engineering complement to IOR research: where [[proposals/cardano-vision-2026|Cardano Vision 2026]] funds analysis and validation, this proposal funds production-grade mainnet delivery, conformance/mutation/adversarial testing scaffolding, and operational tooling required to safely activate Peras, History Expiry, and related protocol changes.

## Key points

- **Budget:** ₳39,787,316; $176/hr average for senior Cardano infrastructure engineers; ₳0.25/USD (5-year conservative average); CBU/ARK Peras cryptography subcontracts as fixed-price line items.
- **Duration:** 2 years (2026–2028); staggered Peras v1/v2 delivery aligned with Hard Fork Combinator windows.
- **Delivery model:** Single integrated pipeline — 17 packages treated as interdependent, not a modular menu.
- **Peras v1:** Production cryptography, KillSwitch, mainnet readiness.
- **Peras v2:** Pre-agreement algorithm, cooldown recovery, performance optimizations.
- **History Expiry:** Partial-history nodes to mitigate SPO disk growth (~1 GB/hour projected at 100–1000 TPS under [[concepts/leios|Leios]]).
- **Resilience stack:** CTC conformance testing (Peras & Leios), adversarial fork testing (Genesis), mutation testing, block cost investigation.
- **Observability:** Hoarding Node — live deployment, distributed mode, embedded consensus validation, transaction collection.
- **Developer tools:** Plutus Script Re-Executor; Canonical Ledger State & Mithril (CIP-0165).
- **Incident response:** Hard Fork Mempool Bridger preserves transactions during fork incidents.
- **Maintenance:** Genesis Sync Accelerator and Cardano Node Emulator ongoing compatibility work.
- **Governance separation:** Tweag commits to "ready-for-activation" deliverables; ecosystem activation (HFC, CIP progression) reported separately with owners and risks.
- **Prior Tweag treasury:** ₳11,070,322.68 allocated via Treasury Smart Contract ID `680d1b63565577986442d24e`.
- **Compliance:** NCL guardrail TREASURY-02a; unspent funds returned at delivery end; 3rd-party assurer for milestones; audit costs in overhead.
- **Community:** Public demos every 2 months at [tweag.github.io/cardano-website](https://tweag.github.io/cardano-website/); dedicated Discord; program Slack with IOG and ecosystem contributors.
- **Strategic pillars cited:** Pillar 1 (Infrastructure and Research Excellence); Pillar 5 (Ecosystem Sustainability and Resilience).
- **PDF detail (2026-06-01):** Per-package budgets and milestone acceptance criteria; Peras v1 targets ≤5 min median settlement and ≤30% storage vs Praos; KillSwitch stability metric (no activation first 6 epochs); Plutus Script Re-Executor is largest line item (₳6.7M); History Expiry requires new CIP; Mempool Bridger targets ≥80% orphaned-tx re-inclusion in testnet scenarios; TSC multi-supplier coordination; EURL Tweag since 2013, Modus Create acquisition 2022.

## Wiki updates

- Created [[sources/tweag-core-cardano-infrastructure-2026-2028]]
- Created [[proposals/tweag-core-cardano-infrastructure-2026-2028]]
- Created [[entities/tweag]]
- Created [[concepts/peras]], [[concepts/history-expiry]], [[concepts/hoarding-node]]
- Updated [[entities/intersect]], [[concepts/ouroboros]], [[concepts/leios]], [[concepts/treasury-escrow-oversight]], [[concepts/research-delivery-pipeline]]
- Updated [[overview]], [[index]]
- **2026-06-01:** PDF ingest — [[analysis/tweag-2026-2028-work-package-deliverables]]; enriched [[concepts/peras]], [[concepts/history-expiry]], [[entities/tweag]], [[proposals/tweag-core-cardano-infrastructure-2026-2028]]
- **2026-06-04:** Vote 56 ingest — [[sources/vote-56-tweag-core-cardano-infrastructure-2026-2028]]; DRep YES; [[concepts/treasury-proposal-bundling]]
- **2026-06-21:** Narrower successor ingested — [[sources/tweag-core-cardano-infrastructure-2026-2027]] (₳18.3M, 3 WPs); see [[proposals/tweag-core-cardano-infrastructure-2026-2027]]
