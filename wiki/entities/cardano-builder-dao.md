# Cardano Builder DAO

The **Cardano Builder DAO** (CB DAO) is a smart contract-governed, builder-led treasury allocation mechanism on Cardano. Member projects review proposals, debate, vote, and distribute funds to teams whose work can advance **[[concepts/cardano-vision|Vision 2030]]** ecosystem KPIs — MAU, monthly on-chain transactions, and TVL.

## Position

CB DAO targets **live, user-facing builders** rather than greenfield grants alone. Funding decisions run through internal governance cycles (temperature checks, merit review, final votes) with on-chain treasury withdrawals executed as multi-output transactions once member quorum is reached. Official Cardano developer documentation describes CB DAO as a smart contract-governed mechanism with 50+ established projects participating in funding decisions.

## Track record (through mid-2026)

| Metric | Value |
|--------|-------|
| Total distributed (2 rounds) | ₳11.1M across 34 proposals |
| Round 1 | 38 voting / 27 requesting members; 20 funded; 83% participation; ₳5,541,335 |
| Round 2 | 18 new members; 14 companies funded; 88% participation |
| Unused returned to treasury | ₳354,790 (after rounds 1–2) |
| Governance actions executed (R1) | 56 |

Governance matured across cycles: elected board, third-party assurance, governing-document amendments, and a rule preventing board members from receiving funding in later rounds.

## Technology and operations

Enabled by **[[entities/clarity|Clarity]]** Initiative DAO tooling ([clarity.vote](https://www.clarity.vote)). Public KPI reporting via a DAO dashboard — v1 self-reported, v2 on-chain-verified metrics.

## Treasury proposals

| Proposal | Model |
|----------|-------|
| 2025 initial ask | ₳12M; **Intersect-administered** TRSC (per ecosystem reporting) |
| [[proposals/cardano-builder-dao|2026 continuation]] | **dRep DAO council multisig** administrator; milestone-gated disbursement to DAO |

## Related

- [[proposals/cardano-builder-dao]]
- [[sources/cardano-builder-dao]]
- [[entities/clarity]]
- [[concepts/initiative-dao]]
- [[concepts/ecosystem-kpi-funding]]

## Open questions

- What is the exact on-chain withdrawal amount for the 2026 continuation proposal?
- How will dRep-administered escrow compare in practice to Intersect TRSC oversight for the prior ₳12M round?
