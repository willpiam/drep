# Tweag Core Cardano Infrastructure 2026–2027

**Type:** Treasury withdrawal (core L1 engineering)  
**Contractor:** [[entities/tweag|Tweag by Modus Create]]  
**Submitter / administrator:** [[entities/intersect|Intersect]] (on behalf of CDH)  
**Source:** [[sources/tweag-core-cardano-infrastructure-2026-2027]]  
**On-chain recipient:** `stake17xzc8pt7fgf0lc0x7eq6z7z6puhsxmzktna7dluahrj6g6ghh5qjr` (Intersect 2025 TRSC)

Tweag requests **₳18,263,496** (~$4.57M) over 2026–2027 to deliver **3 work packages** focused on **[[concepts/peras|Peras]] v1 mainnet deployment**, **[[concepts/history-expiry|History Expiry]]**, and **CTC conformance testing** for Peras and [[concepts/leios|Leios]]. Intersect submits and administers; Tweag is the delivery contractor — not IOG or IOR. See [[analysis/tweag-proposer-vs-iog]].

## Relationship to 2026–2028 proposal

| Item | 2026–2027 (this action) | [[proposals/tweag-core-cardano-infrastructure-2026-2028|2026–2028]] (vote 56) |
|------|-------------------------|-------------------------------------------------------------------------------|
| Ask | ₳18.3M | ₳39.8M |
| Horizon | 2026–2027 | 2026–2028 |
| Work packages | 3 | 17 |
| Peras scope | v1 only | v1 + v2 |
| Dropped vs 17-WP | Peras v2, Hoarding Node, Plutus Re-Executor, mutation/adversarial testing, maintenance WPs | Full pipeline |

Both proposals argue the remaining packages form one **non-modular pipeline**; the 2026–2027 version is a reduced scope within the same strategic lane (Peras mainnet + SPO economics + testing scaffolding).

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳18,263,496 |
| USD equivalent | ~$4,565,874 at ₳0.25/USD |
| Duration | 2026–2027 |
| Work packages | 3 |
| Rate basis | $176/hr senior Cardano infrastructure engineers |
| Prior Tweag allocation | ₳11,070,322.68 (TSC ID `680d1b63565577986442d24e`) |
| 3rd-party assurer | No Witness Labs |
| Code review | Mandatory IOG review on target Cardano repositories |

## Work packages

| Package | Focus |
|---------|-------|
| **Peras v1** | Production cryptography (CBU/ARK subcontracts), KillSwitch, mainnet readiness, support and maintenance |
| **History Expiry** | Partial-history nodes; SPO storage cost mitigation under Leios throughput |
| **Conformance Testing** | CTC framework extended for Peras and Leios |

Work-package detail PDFs: IPFS bundle `QmNcegfkH3WFf8xgjrKKTH9YoMRdmkAYUvCwmJy514XxdK` (History Expiry, CTC). Per-package budgets are not itemized in the JSON abstract; see full IPFS document `QmPJxnx5jTqvqnKXPgqpoH5yvL6xgBFTkvEjF4np3k8eHr`.

## Relationship to IOR research

[[proposals/cardano-vision-2026|Cardano Vision 2026]] funds IOR research and validation; production hard-fork work is out of IOR scope. This proposal funds the complementary **engineering delivery** lane for Peras v1 mainnet, History Expiry, and conformance infrastructure — the minimum set Tweag frames as required before Peras and Leios deliver ecosystem value.

## Governance and controls

Same Intersect administration pattern as Cardano Vision 2026 and the prior Tweag proposal:

- Legal contract between Tweag and CDH; milestones via Intersect
- Sundae Labs TRSC/PSSC; 2025 TRSC stake address; migration to 2026 TRSC when established
- Oversight Committee: Sundae Labs, Cardano Foundation, Dquadrant, Xerberus, NMKR
- Funds delegate to auto-abstain DRep; no SPO delegation
- No Witness Labs signs off milestones; IOG code review on deliverables
- Community dashboard; unspent funds returned at delivery end

## DRep position

Vote context placeholder: [vote 69](../../vote_context/markdown/69_tweag.md) — summary only (₳18.3M); **conclusion not yet recorded**.

**On-chain:** [gov_action1zljrlljt9cxlz7ra2nep43nxg0r54wcnrgexyuhuam9ah0ws607qq2vcg4x](https://cardanoscan.io/govAction/gov_action1zljrlljt9cxlz7ra2nep43nxg0r54wcnrgexyuhuam9ah0ws607qq2vcg4x)

## Open questions

- How does this reduced scope relate to enactment or withdrawal of the vote-56 2026–2028 action?
- Are Peras v2, Hoarding Node, and other dropped WPs deferred to a future proposal or funded elsewhere?
- What per-package budget split and milestone acceptance criteria apply in the Legal Contract?
- Does the narrower 3-WP bundle address prior community objections to 17-WP bundling while preserving the integrated-pipeline argument?

## Related

- [[entities/tweag]], [[entities/intersect]]
- [[concepts/peras]], [[concepts/history-expiry]], [[concepts/leios]]
- [[concepts/treasury-proposal-bundling]], [[concepts/treasury-escrow-oversight]]
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]], [[sources/vote-56-tweag-core-cardano-infrastructure-2026-2028]]
- [[proposals/cardano-vision-2026]], [[analysis/tweag-proposer-vs-iog]]
- Legacy vote artifact: `vote_context/markdown/69_tweag.md`
