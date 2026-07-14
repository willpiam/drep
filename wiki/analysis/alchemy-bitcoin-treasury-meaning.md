# Alchemy “Bitcoin treasury protocol” — meaning

**From query:** 2026-07-14  
**Question:** What do they mean by Bitcoin treasury protocol? Would this be controlled by smart contracts on Cardano? Or is the idea to extend Cardano’s built-in treasury to support assets other than ADA?

## Answer

**“Bitcoin treasury protocol” is product/category language**, modeled on *corporate and DeFi Bitcoin-treasury structured exposure* — not a change to Cardano’s constitutional ADA treasury.

Proposers cite Strategy (MSTR) common/preferreds, Strive SATA, and on-chain Apyx/Saturn-style products as demand for **senior/junior BTC-backed claims**. Alchemy’s version: a **shared BTC vault** plus two composable assets (**FIRE** junior / **ICE** senior-style), with reserve-ratio safety zones and public reporting — conceptually closer to a DJED-like two-token DeFi system than to governance accounting ([[concepts/cardano-btcfi]], [[proposals/alchemy-cardano-native-bitcoin-treasury]]).

### Not Cardano’s governance treasury (non-ADA)

Alchemy does **not** propose extending the L1 **Cardano Treasury** to hold or account for BTC or other non-ADA assets.

The governance treasury only appears as:

| Role | What happens |
|------|----------------|
| Funding source | ADA treasury **withdrawal** (₳10M) pays Alchemy delivery + launch liquidity |
| Beneficiary of returns | Launch-liquidity profits/yield converted to ADA on Cardano DEXs and returned to the **Cardano Treasury** quarterly; principal return optional after $60M TVL + further governance action |

### Where control lives (as specified)

| Layer | Role in Alchemy |
|-------|-----------------|
| **Alchemy protocol** | Reserve math, mint/redeem constraints, FIRE/ICE economic design, dashboards/reporting |
| **[[entities/charms\|Charms]]** | Bitcoin-native issuance / meta-protocol path so assets can circulate as Cardano-native |
| **Cardano DeFi surface** | FIRE/ICE used in wallets, DEXs, adapters; launch liquidity on Cardano DEXs |
| **[[entities/intersect\|Intersect]] (interim admin)** | Accounting/custody of *withdrawn ADA grant funds*, not L1 treasury multi-asset support |

The proposal markets **“transparent, on-chain Bitcoin-backed structured exposure”** and **“protocol mechanics”** with formulaic mint/redeem gates. It does **not** spell out that Plutus scripts on Cardano exclusively enforce vault accounting. Enforcement is presented as Charms + Alchemy protocol stack (Bitcoin-side vault BTC + Cardano-circulating FIRE/ICE), with acknowledged Charms bridge/oracle/accounting risk.

**Gap:** Exact split of on-chain Cardano script control vs Bitcoin/Charms client-side validation vs off-chain/admin controls is under-specified in the treasury-action metadata.

## Sources

- [[sources/alchemy-sundial-charms-cardano-native-bitcoin-treasury-protocol]]
- [[proposals/alchemy-cardano-native-bitcoin-treasury]]
- [[concepts/cardano-btcfi]]
- [[entities/charms]]
- [[analysis/alchemy-what-theyre-building]]
