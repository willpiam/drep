# Cardano Critical Integrations (CCI)

**Cardano Critical Integrations (CCI)** is a Pentad-led treasury program to onboard and sustain tier-one infrastructure that other L1 ecosystems treat as standard utilities: stablecoins, institutional custody, cross-chain bridges, pricing oracles, and on-chain analytics. The program is administered by [[entities/intersect|Intersect]] under the Treasury Reserve Smart Contract Framework with a five-member **Pentad Steering Committee** (IOG, Cardano Foundation, EMURGO, Midnight Foundation; Intersect as non-voting Administrator).

## Position

CCI V1 ([[proposals/cardano-critical-integrations-v1]]) secured **₳70M** over 24 months for initial delivery and launch readiness. CCI V2 ([[proposals/cardano-critical-integrations-v2]]) requests **₳23M** for 12 months of Year 2 maintenance, enhancement tooling, and one new integration (Fireblocks). The proposers frame V2 as sustaining live infrastructure whose annual licensing and operational costs recur for as long as each integration remains active.

## Integrations

| Integration | V1 status | V2 scope |
|-------------|-----------|----------|
| **Circle (USDCx)** | Launched / integrating | Year 2 license/platform/attestation fees (confidential amount); attestor ops, monitoring, contract administrator oversight — largest V1 vendor per Intersect status report |
| **LayerZero** | Launched / integrating | Endpoint ops, DVN configuration, protocol-version compatibility |
| **Pyth** | Launched / integrating | Oracle feed continuity, publisher incentives, Cardano infrastructure |
| **Dune Analytics** | Launched / integrating | Subgraph coverage, schema maintenance, dashboard refresh |
| **Fireblocks** | — | New: native ADA/CNT custody, transfer, staking/governance delegation foundations |

## Governance structure

- **Steering Committee:** High-level direction; approves maintenance renewals and enhancement-reserve drawdowns (3/4 quorum of voting members).
- **Working groups:** Operational delivery across commercial, legal, technical, analytics, and communications.
- **Intersect:** Administrator; TRSC/PSSC disbursement; delivery assurance; bi-annual reporting.
- **Oversight multisig:** Sundae Labs, Cardano Foundation, DQuadrant, Xerberus, NMKR on TRSC operations.

## Explicit exclusions (V2)

New integrations (USDT0, LayerZero OFT expansion, other custodial/analytics targets), dapp grants, liquidity programs, and marketing/events are **out of scope** — each intended as a separate governance action.

## DRep context

- V1 budget info action: DRep **YES** ([vote 29](../../vote_context/markdown/29_CriticalIntegrations.md), Nov 2025)
- V1 treasury withdrawal: DRep **YES**, enacted (Dec 2025)
- V2 treasury withdrawal: DRep **NO** ([vote 65](../../vote_context/markdown/65_critical.md), Jun 2026) — concerns over ₳70M → ₳23M cadence, Pentad entity governance, and recurring-cost structure

## Open questions

- What is the expected annual run-rate after V2's 12-month window?
- How much vendor-level cost detail can the Steering Committee disclose in progress reports despite NDAs?
- What is Circle's confidential Year 2 fee within the ₳20.7M maintenance bucket (vs LayerZero, Pyth, Dune, Fireblocks)?
- What measurable adoption metrics (TVL, USDCx circulation, bridge volume) will tie maintenance spend to ecosystem outcomes?
- How does CCI maintenance funding compare to self-sustaining integration models on other chains?
- What treasury actions beyond CCI V2 are required to fund USDCx ops through a two-year horizon? → [[analysis/usdcx-two-year-funding-horizon]]

## Related

- [[proposals/cardano-critical-integrations-v1]]
- [[proposals/cardano-critical-integrations-v2]]
- [[entities/intersect]]
- [[entities/input-output-group]]
- [[entities/cardano-foundation]]
- [[entities/emurgo]]
- [[entities/midnight-foundation]]
- [[concepts/treasury-escrow-oversight]]
- [[concepts/treasury-proposal-bundling]]
