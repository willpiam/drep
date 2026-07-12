# Cardano Builder DAO

**Type:** Treasury withdrawal (builder-led Initiative DAO continuation)  
**Proposer:** [[entities/cardano-builder-dao|Cardano Builder DAO]]  
**Administrator:** Independent dRep DAO council multisig (not Intersect TRSC)  
**Source:** [[sources/cardano-builder-dao]]  
**On-chain ID:** `gov_action1fdatlfcdnzzcw5x9pnt9r42v992nqw65zze57s8tyk0jll78eyusqccn9gc`

Continuation funding for the **[[entities/cardano-builder-dao|Cardano Builder DAO]]** — a smart contract-governed **[[concepts/initiative-dao|Initiative DAO]]** that allocates treasury capital to builders advancing **[[concepts/ecosystem-kpi-funding|Vision 2030 KPIs]]** (MAU, monthly transactions, TVL).

## Context

| Item | Detail |
|------|--------|
| Total ask | Not in CIP-108 metadata — see [Milestone and Budget Document](https://docsend.com/view/mfujtmqgnjm567p9) and on-chain withdrawal |
| Prior treasury | Yes — 2025 Cardano treasury funding (₳12M initial ask, Intersect-administered per ecosystem reporting) |
| Prior distribution | ₳11.1M across 34 proposals in 2 internal rounds |
| Unused returned | ₳354,790 to treasury after rounds 1–2 |
| Voting window | Submitted 2026-06-24; expires 2026-07-28 |
| Platform | [clarity.vote](https://www.clarity.vote) — enabled by [[entities/clarity|Clarity]] |

## Strategic framing

CB DAO funds **live builders** whose products can grow real Cardano usage. Unlike broad research or infrastructure asks, the mechanism is **member-governed sub-allocation**: 50+ established projects participate in funding decisions per official developer documentation.

KPI accountability is central:

- **MAU** — adoption and retention of Cardano-based products
- **Monthly transactions** — repeat on-chain activity from apps, protocols, integrations
- **TVL** — liquidity and DeFi participation depth

KPI dashboard **v1** used self-reporting; **v2** ties to live on-chain Cardano data. CB DAO commits to working with dReps on standardized KPI tracking in future versions.

## Track record

### Round 1

- 38 voting members, 27 requesting members
- 20 companies funded; **83%** governance participation
- **₳5,541,335** distributed via smart-contract-governed process
- 56 governance actions; 21 member meetings; 1,285 votes; 1,000+ comment threads (ecosystem reporting)

### Round 2

- 18 new members joined
- Full review → debate → temperature check → final vote cycle
- **14 companies** funded; **88%** participation
- Governance improvements: board self-funding ban, board turnover, checkpoint KPI reporting

### Operational maturity

Bootstrapped builder community; ratified/amended governing documents; elected board; third-party assurance; merit-based proposal review; on-chain multi-output treasury withdrawals to approved addresses at quorum.

## Administration model

**Distinct from Intersect TRSC:** This proposal uses an independent **dRep DAO council** multisig:

| Element | Detail |
|---------|--------|
| Council role | Receive treasury withdrawal; hold funds; validate milestones; disburse to CB DAO |
| Named members | Cardano Yoda (Jaromír Tesař); Marco Grendel Moshi; +1 non-affiliated active dRep |
| Release rule | CB DAO receives funds only after administrator confirms milestone completion |
| Constitutional compliance | Auditable separate accounts; no SPO delegation; auto-abstain DRep delegation (§7) |

The 2025 initial ₳12M round was **Intersect-administered**; this continuation shifts escrow oversight to active dReps.

## Repayment

Unused or unallocated DAO treasury funds return to the Cardano Treasury. Prior return: [₳354,790 tx](https://adastat.net/transactions/dfcf57c8c65c50bb208106db91b2db38c4a7512f9fbf100f9f5e1f6301ceb8fc).

## Clarity relationship

[[entities/clarity|Clarity]] built Initiative DAO tooling and will **not** request funding as a member through CB DAO or sibling Initiative DAOs. Enabling technology was funded by CB DAO in 2025.

## DRep position

Listed in Intersect batch vote context ([vote 72](../../vote_context/markdown/72_many.md)) alongside Blockfrost NFP and others. **No DRep vote recorded yet** in published context.

## Related votes

- [vote 72](../../vote_context/markdown/72_many.md) — batch listing; no conclusion for CB DAO

## Open questions

- What is the exact withdrawal amount and milestone schedule in the DocSend budget document?
- How does dRep council oversight compare to Intersect TRSC + Oversight Committee for the prior round?
- What standardized KPI definitions will dReps and CB DAO agree on for dashboard v3+?
- Will CC ratification follow given current voting posture on related batch actions?
