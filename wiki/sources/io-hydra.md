# IO: Hydra

**Raw:** [../raw/IO_-Hydra.json](../raw/IO_-Hydra.json)  
**Ingested:** 2026-06-14  
**Full proposal (IPFS):** [ipfs://Qmbk3jHKKLQ1VrniKaD7sGMscJxCKvoXqt1sQoEnRLTku4](https://ipnso-com.ipns.inbrowser.link/?cid=Qmbk3jHKKLQ1VrniKaD7sGMscJxCKvoXqt1sQoEnRLTku4)  
**On-chain recipient:** `stake17xzc8pt7fgf0lc0x7eq6z7z6puhsxmzktna7dluahrj6g6ghh5qjr` (Intersect 2025 TRSC)  
**Governance action:** [gov_action1fah9m7dxu99af8jqdc4mkrgs3va790nyh9tfhycq2wsvrm47p4rsqtcm6ry](https://cardanoscan.io/govAction/gov_action1fah9m7dxu99af8jqdc4mkrgs3va790nyh9tfhycq2wsvrm47p4rsqtcm6ry)

## Summary

Treasury withdrawal from **[[entities/input-output-group|Input Output Global]]** (co-authored with [[entities/intersect|Intersect]] witness) requesting **₳5,100,781** (~$816,125 at ₳0.16/USD) to harden and scale **[[concepts/hydra|Hydra]] v2** — Cardano's production state-channel L2. Four workstreams cover performance optimization (2–10× snapshot signing and memory gains), operational excellence (runbooks, observability, TUI), ecosystem support (production-user features, Hydra Alliance, hackathons), and maintenance/DevX (CI, tooling, technical debt) through Q3–Q4 2026.

The proposal argues Hydra is the **only production-grade L2 on Cardano**, already running live workloads for Delta DeFi, Masumi, Intersect voting, VTech Labs, Blockfrost, Glacier Drop, and others. It frames L1 gaps (2+ hour finality, ~$0.17/tx, ~7–10 TPS) as pre-selection filters that exclude high-performance verticals before Cardano's security/EUTXO strengths are evaluated; [[concepts/leios|Leios]] and [[concepts/peras|Peras]] improve L1 but cannot reach zero-fee sub-second envelopes due to the scaling trilemma.

[[entities/intersect|Intersect]] administers on behalf of CDH via the standard Sundae Labs TRSC/PSSC framework, milestone-gated disbursement, 3rd-party assurer, and community dashboard. Unspent funds return to treasury at delivery end.

## Key points

- **Budget:** ₳5,100,781 — Development 86%, Engagement & Ecosystem 6%, Operations 3%, Infrastructure/Security/Legal/Governance/Others 1% each.
- **Delivery:** Milestone-gated legal contract (IO ↔ CDH); independent 3rd-party assurance; KPI-linked portion of funding.
- **Workstreams:** Performance optimization; operational excellence; ecosystem support; maintenance & DevX (Q3–Q4 2026).
- **Hydra positioning:** State channels with isomorphic Plutus/EUTXO; 1-of-n honest custody vs rollup sequencers; direct setup (participants run nodes) vs delegated setup (operators run heads).
- **Production users cited:** Delta DeFi (perpetual DEX on Hydra), Masumi (agent-to-agent commerce), Hydra Doom, Glacier Drop (30M+ users stress test), Intersect voting, VTech Labs (HydraHub, HydraOne), Blockfrost (SPO payments), Midgard (fast withdrawals), Hydra Vending Machine (PoS demo).
- **Use-case verticals:** Institutional/perpetual DEXes, agent commerce, gaming, micropayments, point of sale, verifiable information processing, B2B payment rails, prediction markets, RWA platforms.
- **Protocol maturity:** v1.3 stable; v2 alpha with incremental fund add/remove; partial fanout shipped early.
- **L1 complement:** Head open/close/settlement drives L1 fees; optional head-fee routing to treasury on settlement.
- **KPI alignment:** TVL, monthly transactions, MAU, throughput capacity, reliability/uptime, annual protocol revenue; Pillars 1, 2, 4, 5.
- **Prior IO treasury:** ₳130,708,860 allocated across TSC projects; ₳84,909,073 withdrawn by IOG to date (per this proposal's appendix).
- **Compliance:** NCL guardrail TREASURY-02a at submission; refund conditions for unspent or reduced-scope funds.

## Wiki updates

- Created [[sources/io-hydra]]
- Created [[proposals/io-hydra]]
- Created [[concepts/hydra]]
- Updated [[entities/input-output-group]], [[entities/intersect]], [[concepts/leios]], [[concepts/peras]]
- Updated [[overview]], [[index]]
