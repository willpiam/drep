# IO: Hydra

**Type:** Treasury withdrawal (L2 scaling / Hydra v2 hardening)  
**Proposer:** [[entities/input-output-group|Input Output Global]]  
**Co-author witness:** [[entities/intersect|Intersect]]  
**Administrator:** Intersect (on behalf of CDH)  
**Source:** [[sources/io-hydra]]  
**On-chain recipient:** `stake17xzc8pt7fgf0lc0x7eq6z7z6puhsxmzktna7dluahrj6g6ghh5qjr` (Intersect 2025 TRSC)

IOG requests **₳5,100,781** (~$816,125 at ₳0.16/USD) to deliver a feature-complete, production-hardened **[[concepts/hydra|Hydra]] v2** across four workstreams through Q3–Q4 2026.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳5,100,781 |
| USD equivalent | ~$816,125 at ₳0.16/USD |
| Duration | Through Q3–Q4 2026 (milestone-gated) |
| Workstreams | 4 — performance, ops excellence, ecosystem support, maintenance/DevX |
| Admin model | Intersect TRSC/PSSC; Sundae Labs framework; 3rd-party assurer |
| Full proposal | [IPFS PDF](https://ipnso-com.ipns.inbrowser.link/?cid=Qmbk3jHKKLQ1VrniKaD7sGMscJxCKvoXqt1sQoEnRLTku4) |

## Workstreams

| Workstream | Focus | Expected impact |
|------------|-------|-----------------|
| Performance optimization | Snapshot signing speed, memory profile, on-chain contract optimization, benchmarking suite | 2–10× runtime gains; lower L1 settlement costs |
| Operational excellence | Runbooks, node configuration, TUI, observability, logging | Production operability for Delta DeFi, Masumi, pipeline integrators |
| Ecosystem support | Production-user feature requests, Hydra Alliance/Working Group, hackathons, DevRel | Builder pipeline and shipped user-requested capabilities |
| Maintenance & DevX | CI, tooling, technical debt (Q3–Q4 2026) | Long-term protocol health |

## Budget breakdown

| Category | Amount (₳) | Share |
|----------|------------|-------|
| Development | 4,386,671 | 86% |
| Engagement & Ecosystem support | 306,047 | 6% |
| Operations & Delivery | 153,023 | 3% |
| Infrastructure | 51,008 | 1% |
| Security & Audits | 51,008 | 1% |
| Legal & Compliance | 51,008 | 1% |
| Governance | 51,008 | 1% |
| Others | 51,008 | 1% |
| **Total** | **5,100,781** | |

A portion of funding is tied to demonstrating measurable impact on Cardano KPIs and strategic pillars.

## Strategic framing

The proposal argues Cardano L1's **finality gap** (2+ hours), **cost gap** (~$0.17/tx vs sub-cent competitors), **developer burden** (UTXO concurrency/batching), and **throughput ceiling** (~7–10 TPS) cause high-performance builders to exclude Cardano at selection stage. [[concepts/hydra|Hydra]] closes finality and fee constraints **today** while [[concepts/leios|Leios]] and [[concepts/peras|Peras]] improve L1 over longer horizons.

Production dependencies cited: Delta DeFi, Masumi, Intersect voting, VTech Labs, Blockfrost, Glacier Drop. Failure to fund risks migration to competing chains and reputational damage to Cardano's L2 trajectory.

## Governance and controls

Same Intersect administration pattern as [[proposals/cardano-vision-2026|Cardano Vision 2026]] and [[proposals/tweag-core-cardano-infrastructure-2026-2028|Tweag 2026–2028]]:

- Legal contract between Input Output and CDH; milestones via Intersect
- Sundae Labs TRSC/PSSC; 2025 TRSC stake address; migration to 2026 TRSC when established
- Oversight Committee: Sundae Labs, Cardano Foundation, Dquadrant, Xerberus, NMKR
- Funds delegate to auto-abstain DRep; no SPO delegation
- 3rd-party assurer signs off milestones; community dashboard
- Unspent funds returned at delivery end; proportional refund on scope reduction
- NCL guardrail TREASURY-02a compliance at submission

## Prior IO treasury receipts (proposal appendix)

| Workstream | Ada received | % of allocation |
|------------|--------------|-----------------|
| Blockfrost | ₳1,137,500 | 88% |
| Catalyst (Hermes/UX) | ₳3,095,400 | 60% |
| IOE | ₳53,487,088 | 55% |
| IOR | ₳26,840,000 | 100% |
| Governance | ₳349,085 | 59% |

Total IOG allocation across TSC projects: **₳130,708,860**; withdrawn to date: **₳84,909,073**.

## DRep position

Published vote context: [vote 62](../../vote_context/markdown/62_ioHydra.md) — **YES** on *IO: Hydra* (2026-06-14). Rationale text in vote context is still a placeholder; position recorded on-chain only.

**On-chain:** [gov_action1fah9m7dxu99af8jqdc4mkrgs3va790nyh9tfhycq2wsvrm47p4rsqtcm6ry](https://cardanoscan.io/govAction/gov_action1fah9m7dxu99af8jqdc4mkrgs3va790nyh9tfhycq2wsvrm47p4rsqtcm6ry)

## Open questions

- How do Hydra v2 milestone deliverables map to production SLAs for Delta DeFi and Masumi?
- Is ₳5.1M appropriately scoped relative to the broader IOG 2026 withdrawal bundle?
- What public benchmarking suite outputs will define the 2–10× performance claims?
- How does this L2 investment complement vs overlap with L1 work in [[proposals/tweag-core-cardano-infrastructure-2026-2028|Tweag Peras/Leios delivery]]?

## Related

- [[concepts/hydra]]
- [[entities/input-output-group]]
- [[entities/intersect]]
- [[concepts/leios]]
- [[concepts/peras]]
- [[concepts/treasury-escrow-oversight]]
