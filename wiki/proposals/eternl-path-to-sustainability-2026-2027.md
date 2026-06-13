# Eternl: Path to Sustainability (2026-2027)

**Type:** Treasury withdrawal (wallet operations and ecosystem access)  
**Proposer:** [[entities/eternl|Eternl]] / [[entities/tastenkunst|Tastenkunst GmbH]]  
**Administrator:** Tastenkunst GmbH (self-administered; not Intersect TRSC)  
**Source:** [[sources/eternl-path-to-sustainability-2026-2027]]

Eternl requests **₳1,680,000** over **12 months** (August 2026–July 2027) to keep a major Cardano wallet secure, compatible, and available while introducing **Pro subscriptions** as a path to self-sustainability. The ask uses **[[concepts/treasury-payback-model|scheduled treasury payback]]** rather than milestone-based escrow.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳1,680,000 |
| USD valuation | $420,000 at $0.25/ADA |
| Duration | 12 months (Aug 2026 – Jul 2027) |
| Staffing | 6.0 FTE at $70,000/FTE (10-person team total) |
| Install base | ~100k browser extension; ~30k Android + iOS |
| Transaction share | 10–18% of mainnet transactions (proposer claim) |
| Prior treasury | ₳583,000 (2025 budget, Intersect-administered) — ~$133k short vs expected USD |

## Budget allocation

| Category | Amount (ADA) | Share |
|----------|-------------:|------:|
| Frontend | ₳924,000 | 55% |
| Backend | ₳420,000 | 25% |
| Support | ₳84,000 | 5% |
| Admin | ₳235,200 | 14% |
| Audits | ₳16,800 | 1% |

## Sustainability and payback

Eternl introduces **Pro plans** (prices not final): **$96/year personal**, **$384/year company**. ~**5,500 Pro users (4.2%)** would cover $420k/year. A free basic tier remains.

Payback mechanics (December/June): surplus from remaining stablecoins plus Pro revenue repays up to **$420k**; thereafter **50% of Pro income above $420k/year** donates until **$210k** additional. Pro purchases on-chain with metadata; public reports and tx hashes. Service fees on large DApp txs are excluded from payback calculations.

## Delivery scope

### Infrastructure and operations

Multi-region backend, Cardano nodes (hardfork upgrades), DBSync indexers, application servers (sync, translations, stake pool/governance/scam-token data, tx submission), metadata aggregation, Eternl Hub backend, 24/7 monitoring.

### Frontend and platforms

Chrome extension, web/PWA, iOS, Android, public beta channel; CIP-30 and emerging standards; Dijkstra/Leios hardfork support; multisig flows; hardware wallet support (Ledger, Trezor, OneKey, Keystone, Bluetooth expansion).

### Governance tooling

DRep dashboards, proposal browser, in-wallet voting, governance proposal creation in Eternl (this proposal was authored in the upcoming governance UI).

### Upcoming product lines

- **Eternl Core** — rewrite with custom TypeScript CBOR library; CSL removed
- **Eternl Hub** — cross-device wallet sharing and signing; future CIP + open source
- **Entity export** — combined multi-entity accounting views

## Governance and controls

| Aspect | Eternl model |
|--------|----------------|
| Milestones | **None** — 12-month operational availability |
| Fund custody | Stablecoins in public Tastenkunst company wallet after conversion |
| Administrator | Tastenkunst GmbH (not [[entities/intersect|Intersect]] TRSC) |
| Oversight | Transparency via public wallet, on-chain Pro metadata, biannual reports |
| Self-voting | Proposer will vote yes; delegates expect Eternl continuity |

Contrast: 2025 Eternl funding used Intersect administration ([adastat governance record](https://adastat.net/governances/8ad3d454f3496a35cb0d07b0fd32f687f66338b7d60e787fc0a22939e5d8833e10)).

## Impact framing

Partial alignment claimed with Cardano Vision 2030 KPIs (TVL, transactions, MAU) and Pillars 1–4 (infrastructure, adoption, governance, ecosystem growth). Pillar 5 (sustainability) marked not applicable.

## DRep position

No completed DRep vote context is currently recorded.

## Open questions

- The proposal states **6.0 FTE at $70k** across a **10-person** team but does not justify that headcount with a role breakdown or workload model — see [[analysis/eternl-fte-staffing-justification]].
- Is voluntary payback without smart-contract escrow sufficient accountability for ₳1.68M?
- How should DReps weigh closed-source UI vs npm-published libraries and planned Hub open source?
- Does the ~$133k shortfall from 2025 funding justify a larger 2026 ask, or indicate treasury execution risk?
- If Pro uptake fails, what is the realistic degraded-service scenario (maintenance-only, paid-only, team cuts)?
- Conflict of interest: self-voting and in-wallet governance tooling used to submit the proposal

## Related

- [[entities/eternl]]
- [[entities/tastenkunst]]
- [[concepts/treasury-payback-model]]
- [[concepts/treasury-escrow-oversight]]
- [[concepts/cardano-typescript-tooling]]
