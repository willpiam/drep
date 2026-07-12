# Cardano Builder DAO

**Raw:** [../raw/Cardano-Builder-DAO.json](../raw/Cardano-Builder-DAO.json)  
**Ingested:** 2026-07-10

## Summary

The **[[entities/cardano-builder-dao|Cardano Builder DAO]]** (CB DAO) requests a **treasury withdrawal** to continue an ecosystem-wide, **smart contract-governed** funding mechanism for builders advancing **[[concepts/cardano-vision|Vision 2030]]** KPIs — monthly active users (MAU), monthly on-chain transactions, and TVL. The DAO is operated by established Cardano projects (50+ per official developer documentation) using **[[entities/clarity|Clarity]]**'s **[[concepts/initiative-dao|Initiative DAO]]** tooling on [clarity.vote](https://www.clarity.vote).

This is a **continuation** of prior Cardano treasury funding. The CB DAO has already distributed **₳11.1M** across **34 proposals** in two internal funding rounds, returned **₳354,790** unused ADA to the treasury, and evolved governance (board election, third-party assurance, board self-funding ban, KPI dashboard v1→v2).

**Administration (this proposal):** An independent **dRep DAO council multisig** — not the Intersect TRSC pattern used for the 2025 ₳12M initial ask. Named administrators: Cardano Yoda (Jaromír Tesař) and Marco Grendel Moshi, plus one additional non-affiliated active dRep. Council holds withdrawn ADA, validates milestones, and disburses to the DAO only after completion. Funds use auditable separate accounts, no SPO delegation, and auto-abstain DRep delegation per Constitution §7.

**Amount:** Not stated in CIP-108 metadata; specified in the on-chain treasury withdrawal and the external [Milestone and Budget Document](https://docsend.com/view/mfujtmqgnjm567p9).

**On-chain:** `gov_action1fdatlfcdnzzcw5x9pnt9r42v992nqw65zze57s8tyk0jll78eyusqccn9gc` — submitted 2026-06-24; voting deadline 2026-07-28. Listed in DRep batch context ([vote 72](../../vote_context/markdown/72_many.md)); no vote recorded yet.

## Key points

- **KPI accountability:** Funded projects must track MAU, on-chain transactions, and TVL. KPI dashboard v1 was self-reported; v2 ties to live on-chain Cardano data. CB DAO offers to work with dReps on standardized KPI tracking cadence.
- **Round 1 track record:** 38 voting members, 27 requesting members, 20 companies funded, 83% governance participation, **₳5,541,335** distributed via transparent smart-contract process.
- **Round 2 track record:** 18 new members; full review/debate/temperature-check/final-vote cycle; **14 companies** funded, 88% member participation (₳6M round allocation per ecosystem reporting).
- **Operational proof points:** governing documents ratified/amended, elected board, third-party assurance, merit-based review, on-chain treasury withdrawals with multi-output distribution to approved addresses once quorum reached.
- **Clarity conflict policy:** Clarity (Initiative DAO enabler) will **not** seek funding as a requesting member through any Initiative DAO; enabling tools were funded by CB DAO in 2025.
- **Repayment:** Unused or unallocated DAO treasury funds return to Cardano Treasury (prior practice: ₳354,790 returned after rounds 1–2).
- **References:** Medium retrospectives (Clarity, CB DAO), [clarity.vote governance portals](https://www.clarity.vote/organizations/cardano/CardanoBuilderDAO/governance), Code of Conduct, KPI dashboard.

## Wiki updates

- Created [[proposals/cardano-builder-dao]]
- Created [[entities/cardano-builder-dao]]
- Created [[entities/clarity]]
- Created [[concepts/initiative-dao]]
- Created [[concepts/ecosystem-kpi-funding]]
- Updated [[concepts/cardano-vision]]
- Updated [[concepts/treasury-escrow-oversight]]
- Updated [[concepts/treasury-payback-model]]
- Updated [[overview]]
