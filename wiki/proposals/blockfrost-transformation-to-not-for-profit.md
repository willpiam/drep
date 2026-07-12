# Blockfrost: Transformation to not-for-profit

**Type:** Treasury withdrawal (developer API infrastructure / public-good transition)  
**Proposer:** [[entities/input-output-group|Input Output Global]]  
**Co-author witness:** [[entities/intersect|Intersect]]  
**Administrator:** Intersect (on behalf of CDH)  
**Source:** [[sources/blockfrost-transformation-to-not-for-profit]]  
**On-chain recipient:** `stake1784sdxt6jjennmstphgdu7l7c2scf5d02a6cve2dgn5s2kq5u3j9v` (2026 TRSC)

IOG requests **₳9,832,979** (~$1,868,266 at $0.19/ADA) over **18 months** to transition **[[entities/blockfrost|Blockfrost]]** into a **free, community-governed not-for-profit public API**, transferring source code, trademarks, and domains to community stewardship.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳9,832,979 |
| USD equivalent | ~$1,868,266 at $0.19/ADA |
| Duration | 18 months (transition + operations) |
| Prior treasury (Blockfrost workstream) | ₳1,137,500 received (88% of prior allocation) |
| Free-tier share | ~90% of API traffic |
| Tx submission share | >50% of mainnet transactions in most epochs (proposer claim) |
| Developer survey share | 71.5% of projects use Blockfrost (2025 CF survey) |
| Decentralization | 100+ Icebreakers; IOG acquisition 2024 from Five Binaries (2020) |

## Strategic framing

Blockfrost is described as the **lingua franca** of Cardano development — a hosted REST API over mainnet, preview, and preprod so builders avoid running their own nodes. The proposer argues the service cannot remain both a **fully commercial** product and a **free public good** without raising prices, eliminating the free tier, and harming ecosystem adoption. Community feedback on an **earlier unfunded proposal** emphasized treasury reluctance to subsidize a commercial venture; this revision commits to a **fully not-for-profit** structure with IP transfer and elected governance.

## Governance model

| Element | Detail |
|---------|--------|
| Final board | 5 seats — 4 for open-source Cardano infrastructure entities; 1 community seat |
| Election | Target end of 2026; seated by end of Q1 2027 |
| Preliminary board | Anihiri (Blockfrost), Gianelloni (BlinkLabs), Weill (TxPipe), Davidson (SundaeLabs), Luz (Masumi/Begin Wallet) |
| IOG role | Non-voting advisory seat during year one |
| Legal host | New entity or existing NFP (PRAGMA under consideration) |
| Transparency | Public usage dashboard; board-approved infrastructure costs; quarterly reports |
| IP transfer | Source, trademarks, domains, and associated assets to governing NFP by Q1 2027 |

## Milestones

| Phase | Target | Deliverables |
|-------|--------|--------------|
| M1 | Q3 2026 | NFP legally established or host agreement signed; transition architecture published; public dashboard live |
| M2 | Q4 2026 | On-chain board election under published rules |
| M3 | Q1 2027 | All public API traffic on new stack; IP legally transferred; performance maintained |
| M4 | Q2–Q3 2027 | Board-led sustainability consultation (commercial NFP tiers vs vendor-backed federation) |
| M5–12 | 2027 | Sustained ops — **99% monthly uptime SLA**; quarterly technical + budget reports |

## Budget allocation

| Component | Share | ADA | USD (ref.) |
|-----------|------:|----:|-----------:|
| Staffing (6 FTE) | 79.1% | ₳7,780,347 | ~$1,478,266 |
| Ops & infrastructure | 19.3% | ₳1,894,737 | ~$360,000 |
| Legal & accounting | 1.6% | ₳157,895 | ~$30,000 |
| **Total** | **100%** | **₳9,832,979** | **~$1,868,266** |

Staffing covers one PM, one community manager, and four developers for transition and ongoing maintenance. Ops budget (~$20k/month) includes compute, hosting, tooling, and DevOps. Unspent post-transition infrastructure budget returns to treasury.

## Post-subsidy sustainability (board discretion)

Two models are outlined for after the 18-month treasury period:

1. **NFP commercial arm** — Paid tiers with SLAs operated by the not-for-profit; profits returned to Cardano Treasury; pricing under board oversight so commercial offerings do not undermine the free tier.
2. **Vendor-backed federation** — NFP retains free API and IP; qualifying vendors become official partners, serve commercial needs, pay membership fees, and may jointly operate federated infrastructure (including existing **[[concepts/blockfrost-decentralization|Icebreakers]]**).

Analogies cited: Drupal, OpenStreetMap.

## Governance and controls

Same Intersect administration pattern as [[proposals/io-hydra|IO: Hydra]] and [[proposals/tweag-core-cardano-infrastructure-2026-2028|Tweag 2026–2028]]:

- Legal contract between Input Output and CDH; milestones via Intersect
- Sundae Labs TRSC/PSSC; 2026 TRSC addresses per [[concepts/treasury-escrow-oversight]]
- Oversight Committee: Sundae Labs, Cardano Foundation, Dquadrant, NMKR, Sundial, Eternl
- 3rd-party assurer; [treasury.sundae.fi](https://treasury.sundae.fi) dashboard
- Funds delegate to auto-abstain DRep; unspent funds returned at delivery end
- NCL guardrail TREASURY-02a compliance at submission

## Vision 2030 alignment

Claims direct/indirect alignment with transaction volume, MAU, TVL, protocol revenue, and throughput KPIs. Pillars 1 (Infrastructure), 2 (Adoption), 4 (Community — partial), and 5 (Ecosystem Sustainability) marked aligned; Pillar 3 (Governance) N/A.

## DRep position

No completed DRep vote context is currently recorded.

## Open questions

- Does the NFP structure adequately address prior community concern about treasury funding a commercial Blockfrost, or does post-subsidy commercial revenue planning reintroduce that tension?
- How independent is governance if IOG retains advisory influence in year one and staffed the preliminary board from ecosystem infrastructure firms?
- Is ₳9.8M for 18 months proportionate given prior ₳1.14M Blockfrost workstream receipt and claimed 100+ Icebreakers already decentralizing operations?
- What enforceable guarantees exist that free-tier quality and >50% transaction-submission path remain stable through Q1 2027 cutover?
- Should DReps treat proposed treasury payback from future NFP commercial tiers as credible without on-chain escrow (contrast [[concepts/treasury-payback-model|Eternl payback]])?
- PRAGMA vs new entity: which minimizes overhead and capture risk?

## Related

- [[entities/blockfrost]]
- [[concepts/blockfrost-decentralization]]
- [[entities/input-output-group]]
- [[entities/intersect]]
- [[concepts/treasury-escrow-oversight]]
- [[concepts/treasury-payback-model]]
- [[concepts/cardano-typescript-tooling]]
- [[proposals/io-hydra]]
