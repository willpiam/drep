# Eternl: Path to Sustainability (2026-2027)

**Raw:** [../raw/Eternl_-Path-to-Sustainability-(2026-2027).json](../raw/Eternl_-Path-to-Sustainability-(2026-2027).json)  
**Ingested:** 2026-06-11

## Summary

[[entities/eternl|Eternl]] (via [[entities/tastenkunst|Tastenkunst GmbH]]) requests a **12-month treasury withdrawal of ₳1,680,000** (valued at **$0.25/ADA**, **$420,000** total) for August 2026–July 2027 operations. Eternl is a non-custodial Cardano light wallet (web, browser extension, Android, iOS) used for payments, staking, governance, and DApp interaction. The ask funds **6.0 FTE** at **$70,000/FTE** across frontend, backend, support, admin, and audits.

Unlike milestone-escrowed engineering proposals, this is a **non-milestone operational grant** with a self-administration and **[[concepts/treasury-payback-model|treasury payback]]** model: funds convert to stablecoins in a public company wallet; twice yearly (December/June) surplus from Pro-plan revenue plus remaining treasury stablecoins repays the withdrawal until **$420,000 USD equivalent** is returned, then **50% of Pro income above $420k/year** donates up to an additional **$210,000**. If ADA is above $0.25 at conversion, excess ADA returns to treasury immediately.

Eternl plans **Pro subscriptions** ($96/year personal, $384/year company — prices not final) as the path to self-sustainability; ~**5,500 Pro users (4.2%)** of ~130k install base would cover annual costs. The proposal follows a **2025 budget withdrawal of ₳583,000** (Intersect-administered) that left Eternl ~**$133,000 short** due to ADA price decline.

## Key points

- **Budget split:** Frontend 55%, Backend 25%, Support 5%, Admin 14%, Audits 1%.
- **Impact claims:** 10–18% of mainnet transactions via Eternl; only wallet with comprehensive in-app governance UI; DRep voting and proposal creation in-wallet.
- **Income today:** Small service fees on DApp Browser / MonsterSwap txs ≥100 ADA — insufficient in low-volume environment; fees cover office/legal/licenses, not counted toward payback.
- **Roadmap:** Eternl Core rewrite (custom TypeScript CBOR lib, CSL replacement); Eternl Hub (cross-device wallet sharing, future CIP + open source); enhanced HW wallet support (Ledger, Trezor, OneKey, Bluetooth in v2.1); entity-based wallet data export.
- **Open-source stance:** Main UI stays closed; some libraries published to npm (`@eternl` org); Hub planned open-source via CIP.
- **Prior funding:** Six Catalyst grants (Fund 9–10), Intersect CIP-95 grant (₳70k), 2025 treasury withdrawal (₳583k via Intersect).
- **Risk if unfunded:** Scale to maintenance-only, possible team reduction, may remove free tier and focus on paid licenses.
- **Governance note:** Eternl will vote yes on its own proposal; created and posted using upcoming Eternl governance UI.

## Wiki updates

- Created [[proposals/eternl-path-to-sustainability-2026-2027]]
- Created [[entities/eternl]]
- Created [[entities/tastenkunst]]
- Created [[concepts/treasury-payback-model]]
- Updated [[concepts/treasury-escrow-oversight]]
- Updated [[entities/intersect]]
- Updated [[concepts/cardano-typescript-tooling]]
- Updated [[overview]]
