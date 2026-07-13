# Alchemy by Sundial x Charms: Cardano-Native Bitcoin Treasury Protocol

**Raw:** [../raw/Alchemy-by-Sundial-x-Charms_-Cardano-Native-Bitcoin-Treasury-Protocol.json](../raw/Alchemy-by-Sundial-x-Charms_-Cardano-Native-Bitcoin-Treasury-Protocol.json)  
**Ingested:** 2026-07-13

## Summary

Treasury-withdrawal proposal by **[[entities/sundial-protocol|Sundial Protocol]]** and **[[entities/charms|Charms]]** requesting **₳10,000,000** (~$2.0M at $0.20/ADA) to build **Alchemy** — a Cardano-native **[[concepts/cardano-btcfi|BTCfi]]** infrastructure layer with transparent BTC reserve architecture, composable **FIRE** (BTC+, volatility-absorbing) and **ICE** (BTC−, USD-denominated lower-volatility) assets, public dashboards, integration adapters, and treasury-supported launch liquidity.

Funding splits into two separated pools: **Pool 1** (~$1.0M) for protocol infrastructure and staged launch liquidity (treasury-owned; profits/yield returned quarterly); **Pool 2** (~$1.0M) for delivery, audits, integrations, reporting, legal/compliance, and go-to-market. **[[entities/intersect|Intersect]]** is proposed as interim fund administrator (subject to confirmation). The proposal includes ADA price protection ($0.35 cap), rollover clause (external investment rolls into extra launch liquidity), milestone gating, and principal return option after $60M 30-day TWAP TVL.

## Key points

- **Strategic gap:** Cardano lacks production BTCfi infrastructure; Bitcoin-backed structured exposure is consolidating on Ethereum, BNB, Solana, and off-chain capital markets.
- **Reserve model:** Shared BTC reserve backs FIRE and ICE; target **5.0×** reserve ratio with safety zones (normal >4×, constrained 2–4×, pause <2×).
- **Charms role:** Technical partner for Bitcoin-native asset issuance circulating as Cardano-native assets; protocol-layer bridge/oracle risk acknowledged. Treasury funds **Alchemy delivery** (FIRE/ICE, reserve, integrations, GTM, liquidity), not a general Charms protocol grant — though Pool 2 engineering/infrastructure may pay Alchemy-related Charms integration work. No personal compensation to Charms principals.
- **Treasury protections:** No DRep funds or principal compensation; separated pools; deployment pause rules; unused/excess ADA returned; administrator ADA delegated to auto-abstain.
- **NCL compliance:** Self-contained ADA-denominated withdrawal designed within prevailing Net Change Limit.
- **Complements [[concepts/bifrost-bitcoin-defi-bridge|Bifrost]]:** Bifrost targets BTC→Cardano bridge liquidity (fBTC); Alchemy targets structured BTC-backed financial primitives and reserve reporting infrastructure on Cardano.

## Wiki updates

- Created [[sources/alchemy-sundial-charms-cardano-native-bitcoin-treasury-protocol]]
- Created [[proposals/alchemy-cardano-native-bitcoin-treasury]]
- Created [[entities/sundial-protocol]], [[entities/charms]]
- Created/updated [[concepts/cardano-btcfi]]
- Updated [[entities/intersect]], [[concepts/bifrost-bitcoin-defi-bridge]], [[overview]], [[index]]
