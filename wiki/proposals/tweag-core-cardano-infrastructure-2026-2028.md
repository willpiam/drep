# Tweag Core Cardano Infrastructure 2026–2028

**Type:** Treasury withdrawal (core L1 engineering)  
**Proposer:** [[entities/tweag|Tweag by Modus Create]]  
**Administrator:** [[entities/intersect|Intersect]] (on behalf of CDH)  
**Source:** [[sources/tweag-core-cardano-infrastructure-2026-2028]]  
**On-chain recipient:** `stake17xzc8pt7fgf0lc0x7eq6z7z6puhsxmzktna7dluahrj6g6ghh5qjr` (Intersect 2025 TRSC)

Tweag requests **₳39,787,316** (~$9.95M) over two years to deliver 17 work packages focused on **[[concepts/peras|Peras]] mainnet deployment** and the engineering scaffolding required to safely activate Peras, [[concepts/history-expiry|History Expiry]], and related protocol upgrades alongside [[concepts/leios|Leios]] throughput growth.

This is **not** an IOG or IOR proposal: Tweag is the contracting party; Intersect administers on behalf of CDH. Long-standing IOG contractor history and CBU/ARK crypto subcontracts do not change proposer identity — see [[analysis/tweag-proposer-vs-iog]].

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳39,787,316 |
| USD equivalent | ~$9,946,829 at ₳0.25/USD |
| Duration | 2026–2028 (2 years) |
| Work packages | 17 across 9 infrastructure areas |
| Rate basis | $176/hr senior Cardano infrastructure engineers |
| Prior Tweag allocation | ₳11,070,322.68 (TSC ID `680d1b63565577986442d24e`) |
| Admin model | Intersect TRSC/PSSC; Sundae Labs framework; 3rd-party assurer |

## Work packages (summary)

| Area | Packages | Focus |
|------|----------|-------|
| Peras | v1, v2 | Mainnet cryptography, KillSwitch, pre-agreement, cooldown recovery |
| Node economics | History Expiry | Partial-history nodes; SPO storage cost mitigation |
| Resilience | Conformance testing, adversarial fork testing, mutation testing, block cost investigation | CTC for Peras/Leios; Genesis fork simulation; test adequacy |
| Observability | Hoarding Node (4 packages) | Live deployment, distributed mode, consensus validation, tx collection |
| Developer tooling | Plutus Script Re-Executor, Canonical Ledger State & Mithril | DApp debugging; CIP-0165 state snapshots |
| Incident response | Hard Fork Mempool Bridger | Transaction preservation during fork incidents |
| Maintenance | Genesis Sync Accelerator, Cardano Node Emulator | Protocol-version compatibility |

Per-package budgets, milestones, and acceptance criteria: [[analysis/tweag-2026-2028-work-package-deliverables]]. Individual work-package PDFs are linked from the source JSON references (IPFS bundle `QmNcegfkH3WFf8xgjrKKTH9YoMRdmkAYUvCwmJy514XxdK`). Full compiled proposal: `wiki/raw/tweag.pdf`.

| Work package | Budget (₳) |
|--------------|------------|
| Peras v1 | 4,954,688 |
| Peras v2 | 8,240,040 |
| Plutus Script Re-Executor | 6,724,024 |
| CTC Peras & Leios | 4,860,760 |
| Hoarding Node (live) | 2,969,336 |
| History Expiry | 2,816,016 |
| Canonical ledger state & Mithril | 2,464,014 |
| Hard Fork Mempool Bridger | 1,478,408 |
| Other packages (8) | 5,259,777 |
| **Total** | **39,787,316** |

## Relationship to IOR research

[[proposals/cardano-vision-2026|Cardano Vision 2026]] explicitly excludes production hard-fork work (IO Consensus Initiative scope). Tweag fills the complementary **engineering delivery** lane: mainnet Peras, History Expiry, testing infrastructure, and operational tooling. The proposal argues the 17 packages form one pipeline — Hoarding Node and testing scaffolding validate Peras/History Expiry changes that cannot be safely separated.

## Governance and controls

Same Intersect administration pattern as Cardano Vision 2026:

- Legal contract between Tweag and CDH; milestones via Intersect
- Sundae Labs TRSC/PSSC; 2025 TRSC stake address; migration to 2026 TRSC when established
- Oversight Committee: Sundae Labs, Cardano Foundation, Dquadrant, Xerberus, NMKR
- Funds delegate to auto-abstain DRep; no SPO delegation
- 3rd-party assurer signs off milestones; community dashboard
- Unspent funds returned at delivery end; proportional refund on scope reduction

## DRep position

Published vote context: [vote 56](../../vote_context/markdown/56_tweag.md) — **YES** on *Tweag Core Cardano Infrastructure: Treasury Withdrawal 2026–2028* (2026-06-01). Source summary: [[sources/vote-56-tweag-core-cardano-infrastructure-2026-2028]].

**Rationale (summary):** Many delegates vote NO because of the **two-year timeline** and **bundled 17-package** structure. $computerman previously disfavored bundling but now accepts it when workstreams are interdependent ([[concepts/treasury-proposal-bundling]]). The two-year horizon is reasonable if continuous development through 2028 is required; proposer-stated success conditions should weigh in delegate judgment. The integrated pipeline argument (Peras + testing + History Expiry) aligns with the proposal's own framing and with prior wiki emphasis on **Peras/Leios deployment readiness** in [[concepts/ouroboros]].

**On-chain:** [gov_action14u26vcn3wmcnhc5pqrt6494ypugr7c7f3e2ns60r32cntl6zjtxsqqgeu8p](https://cardanoscan.io/govAction/gov_action14u26vcn3wmcnhc5pqrt6494ypugr7c7f3e2ns60r32cntl6zjtxsqqgeu8p) · [vote record](https://cardanoscan.io/vote/e0d3fa958f8ecd0369ffc81b81cb4bcafea3b6a042f4981ddb231fd6f91d0ce0) · IPFS [bafkreidmxs5qzicttakxdeafwdl27cie5k4wgp3cvlkx7sdaoxsalwmfju](https://ipfs.io/ipfs/bafkreidmxs5qzicttakxdeafwdl27cie5k4wgp3cvlkx7sdaoxsalwmfju)

## Open questions
- How do Peras v1/v2 HFC windows align with IO Consensus Initiative and IOR research timelines?
- Is ₳39.8M appropriately scoped relative to the broader IOG 2026 withdrawal bundle?
- What measurable mainnet KPIs (finality latency, SPO storage reduction, conformance coverage) will milestones enforce?
- How does Tweag's prior ₳11M delivery record compare to acceptance criteria for this expanded portfolio?

## Related

- [[entities/tweag]]
- [[concepts/peras]], [[concepts/history-expiry]], [[concepts/hoarding-node]]
- [[concepts/ouroboros]], [[concepts/leios]]
- [[concepts/research-delivery-pipeline]] — IOR research vs engineering delivery split
- [[concepts/treasury-escrow-oversight]]
- [[proposals/cardano-vision-2026]]
- [[analysis/tweag-2026-2028-work-package-deliverables]]
- [[concepts/treasury-proposal-bundling]]
- [[sources/vote-56-tweag-core-cardano-infrastructure-2026-2028]]
- Legacy vote artifact: `vote_context/markdown/56_tweag.md`
