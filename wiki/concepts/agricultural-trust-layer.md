# Agricultural Trust Layer

An **agricultural trust layer** is shared verification infrastructure for smallholder farming: farmer identity, farm boundaries, crop history, AE credentials, and application events (credit, traceability, compliance) anchored on Cardano so multiple use cases can **verify once, use many times** instead of each building isolated databases.

## Problem framing

~500 million smallholder farmers grow much of the world's food but sit outside formal trust infrastructure that lenders, buyers, insurers, certifiers, and governments rely on. Each application today verifies and stores separately — duplicated cost, repeated onboarding, limited interoperability.

## Three-layer architecture (5am.earth model)

| Layer | Function |
|-------|----------|
| **Source** | AEs, farmers, land/crop records, satellite observations, credentials, application events |
| **Trust (Cardano)** | Verifiable claims, on-chain proofs/records, privacy/permissions, audit trail |
| **Application** | Partners connect via APIs, credentials, selective disclosure — no rebuild of farmer onboarding |

## Cardano components (operational in Project Swaminathan)

- Smart contracts / integration — AIQuant, Anastasia Labs
- Satellite oracle — DigiFarm (12-year crop history, NDVI, land boundaries)
- Self-sovereign identity — Veridian DID stack
- AE credentials — Andamio
- Tokenisation — NMKR

## Funded application paths (2026 proposal)

During the [[proposals/5am-earth-trust-layer-vision-2030-kpis|5am.earth 18-month programme]]:

| Path | Partner | Use case |
|------|---------|----------|
| WP3 | Andamio | AE training, certification, reputation linked to farmer DIDs |
| WP4 | Zengate Global | EUDR traceability and compliance against verified farm origin |
| WP5 | Seedstars SIGMA | Credit scoring, Cardano stablecoin-rail loans and farmer payments |

Future paths named without new infrastructure: DeFi lending, parametric insurance, carbon markets, government subsidies, cooperative governance.

## Vision 2030 KPI alignment

[[proposals/5am-earth-trust-layer-vision-2030-kpis]] cites contribution to all five [[concepts/cardano-vision|Cardano Vision 2030]] pillars, with 2030 projections of 3M farmers, 112.5M annual on-chain transactions, $900M TVL, and 16–20M ADA annual protocol revenue.

## Stewardship

[[entities/5am-earth-foundation|5am.earth Foundation]] is neutral steward; [[entities/syngenta-foundation-india|Syngenta Foundation India]] provides field distribution via [[concepts/project-swaminathan|Project Swaminathan]].

## Related

- [[proposals/5am-earth-trust-layer-vision-2030-kpis]]
- [[sources/5am-earth-trust-layer-vision-2030-kpis]]
- [[entities/5am-earth-foundation]]
- [[concepts/project-swaminathan]]
- [[concepts/cardano-vision]]
