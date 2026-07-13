# Alchemy — what they are trying to make

**From query:** 2026-07-13  
**Question:** What is "Alchemy by Sundial x Charms: Cardano-Native Bitcoin Treasury Protocol" about? What are they trying to make?

## Answer

**Alchemy** is a proposed Cardano-native **BTCfi infrastructure layer** — not a BTC bridge. [[entities/sundial-protocol|Sundial Protocol]] and [[entities/charms|Charms]] ask for **₳10M** to ship reusable tools so wallets, DEXs, and DeFi apps can hold, compose, and report on Bitcoin-backed structured exposure on Cardano.

### What they are building

| Deliverable | Intent |
|-------------|--------|
| Shared BTC reserve | Transparent vault backing both tokens; target **5.0×** reserve ratio with overcollateralization and pause zones |
| **FIRE** (BTC+) | Volatility-absorbing / first-loss claim — amplified BTC upside |
| **ICE** (BTC−) | USD-denominated, lower-volatility BTC-backed exposure |
| Dashboards + SDKs/adapters | Public reserve reporting and wallet/DEX integration surfaces |
| Treasury launch liquidity | Staged Pool 1 capital (~$1M) on Cardano DEXs; profits/yield returned to Treasury quarterly |

**Charms** supplies the Bitcoin meta-protocol issuance path so FIRE/ICE can be Bitcoin-native in logic while circulating as Cardano-native assets. **Sundial** owns product design, GTM, reporting, and controlled liquidity deployment. **[[entities/intersect|Intersect]]** is proposed as interim fund administrator.

Funding is split: Pool 1 (treasury-owned liquidity + infrastructure, ring-fenced) and Pool 2 (~$1M delivery/audit/GTM/admin).

### What it is not

It is **not** [[concepts/bifrost-bitcoin-defi-bridge|Bifrost]] (bridge → fBTC). Bifrost moves BTC onto Cardano; Alchemy builds structured products and reserve/reporting infrastructure around BTC-backed exposure. Proposer framing: complementary layers.

**fBTC:** The Alchemy source text does **not** use or require Bifrost fBTC. Reserve accounting is in BTC via Charms; any future fBTC composability is unspecified ([[concepts/cardano-btcfi]]).

### Motivation (proposer)

Cardano lacks production BTCfi at ecosystem scale while Ethereum, BNB, Solana, and off-chain BTC treasury products capture that activity. Alchemy aims to close that gap with reusable, auditable Cardano-native primitives.

## Sources

- [[sources/alchemy-sundial-charms-cardano-native-bitcoin-treasury-protocol]]
- [[proposals/alchemy-cardano-native-bitcoin-treasury]]
- [[concepts/cardano-btcfi]]
- [[entities/sundial-protocol]]
- [[entities/charms]]
