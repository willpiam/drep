# Eternl

**Eternl** is a non-custodial Cardano light wallet available on web, browser extension, Android, and iOS. Users rely on it for payments, staking, governance, and DApp interaction. The product is developed by [[entities/tastenkunst|Tastenkunst GmbH]]; Marcel Baumberg leads the proposal team.

## Position

Eternl positions itself as a primary Cardano gateway and the only wallet with a comprehensive in-app governance UI — DRep dashboards, proposal browsing, in-wallet voting, and (in upcoming releases) governance proposal creation. The [[proposals/eternl-path-to-sustainability-2026-2027]] treasury ask frames Eternl as infrastructure for adoption: ~100k browser-extension installs, ~30k mobile installs, 10–18% of mainnet transactions, 66 languages, and multi-platform availability.

## Sustainability model

Eternl is transitioning from transaction service fees (DApp Browser, MonsterSwap on txs ≥100 ADA) to **Pro subscription plans** as the primary revenue path. Annual operating cost is stated at **~$420,000**. Pro pricing (not final): **$96/year personal**, **$384/year company**. A free basic tier remains; Pro is the target best experience.

## Technical direction (2026–2027)

| Initiative | Description |
|------------|-------------|
| Eternl Core | Full rewrite; custom TypeScript CBOR library (BUSL-1.1, npm later); CSL replaced across codebase |
| Eternl Hub | Cross-app wallet/settings sharing, forwarded signing; future CIP + open source |
| Hardware wallets | Expanded vendor support; Bluetooth on mobile (Ledger, OneKey, Trezor in v2.1) |
| Governance tooling | DRep dashboards, proposal browser, in-wallet voting and proposal authoring |
| Backend | Multi-region nodes, DBSync indexers, governance/scam-token metadata, 24/7 monitoring |

Main UI is **not** open-source; selected libraries publish under `@eternl` on npm.

## Funding history

| Source | Amount / note |
|--------|----------------|
| Catalyst Fund 9 (×3) | $90k + $90k + $46k |
| Catalyst Fund 10 (×3) | ₳554k + ₳69.2k + ₳20.8k |
| Intersect CIP-95 | ₳70,000 |
| 2025 treasury (Intersect-administered) | ₳583,000 ask — ~$133k short vs USD expectation at $0.70/ADA |
| **2026–2027 proposal** | ₳1,680,000 — see [[proposals/eternl-path-to-sustainability-2026-2027]] |

## Related votes

- [[proposals/eternl-path-to-sustainability-2026-2027]] — pending DRep position

## Open questions

- Will Pro conversion reach the ~4.2% / 5,500-user threshold for self-sustainability?
- How will DReps evaluate self-voting and closed-source UI vs ecosystem dependency?
- What on-chain governance action ID applies once submitted?
