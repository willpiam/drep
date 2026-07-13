# Alchemy: Cardano-Native Bitcoin Treasury Protocol

**Type:** Treasury withdrawal (BTCfi infrastructure + launch liquidity)  
**Proposers:** [[entities/sundial-protocol|Sundial Protocol]] + [[entities/charms|Charms]]  
**Administrator model:** [[entities/intersect|Intersect]] as interim fund administrator (subject to confirmation; 30-day fallback nomination)  
**Source:** [[sources/alchemy-sundial-charms-cardano-native-bitcoin-treasury-protocol]]

The proposal requests **₳10,000,000** (~$2.0M at $0.20/ADA) to deploy **Alchemy** — reusable Cardano **[[concepts/cardano-btcfi|BTCfi]]** infrastructure with FIRE/ICE composable assets, public reporting, ecosystem integrations, and treasury-supported launch liquidity.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳10,000,000 |
| USD reference | ~$2.0M at $0.20/ADA |
| ADA price cap | $0.35 — excess ADA returned or milestone withdrawals reduced |
| Pool 1 | ~$1.0M — infrastructure + staged launch liquidity (treasury-owned) |
| Pool 2 | ~$1.0M — delivery, audit, integrations, GTM, legal, admin |
| Liquidity deployment | 3 monthly tranches; target ~$800k FIRE / ~$200k ICE side |
| Principal return trigger | $60M 30-day TWAP TVL → governance proposal for principal return |

## Technical model

- **Shared BTC reserve** backs FIRE (residual upside / first-loss) and ICE (USD-denominated lower-volatility exposure).
- **Reserve ratio:** (V × P) / L; target 5.0× at launch with overcollateralization.
- **Safety zones:** >4× normal; 2–4× constrained minting/redemption; <2× pause risky activity.
- **Charms** provides Bitcoin-native issuance logic circulating as Cardano-native assets.
- **Public infrastructure:** SDKs/adapters, always-on dashboards, monthly governance reports, reporting standards for future BTCfi projects.

## Treasury protections

- Separated pools; Pool 1 cannot fund delivery overruns or personal compensation.
- Quarterly return of launch-liquidity profits/yield to Treasury via Cardano DEX conversion.
- Rollover: external Alchemy investment rolls development budget into extra treasury-supported liquidity.
- Milestone gating, pause rules, audit allocation, independent administration with auditable accounts.
- Administrator ADA: auto-abstain DRep delegation; no SPO delegation.

## Relationship to other BTC-on-Cardano work

| Approach | Focus |
|----------|-------|
| [[proposals/bifrost-road-to-mainnet-phase-1|Bifrost Phase 1]] | Permissionless BTC bridge → native fBTC via SPO threshold custody |
| **Alchemy** | Structured BTC-backed exposure (FIRE/ICE), reserve architecture, BTCfi reporting layer |

These are complementary in proposer framing: bridge liquidity vs. structured-product infrastructure. The Alchemy text does **not** say FIRE/ICE reserves use Bifrost **fBTC**; Charms is the stated Cardano/Bitcoin issuance path ([[concepts/cardano-btcfi]]).

## DRep position

No published local vote-context markdown for this proposal is ingested yet, so no DRep position is recorded here.

## Related

- [[concepts/cardano-btcfi]]
- [[concepts/bifrost-bitcoin-defi-bridge]]
- [[entities/sundial-protocol]]
- [[entities/charms]]
- [[entities/intersect]]
