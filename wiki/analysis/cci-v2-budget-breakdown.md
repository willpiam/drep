# CCI V2 — What the ₳23M Buys

**From query:** 2026-06-18  
**Question:** What is the ₳23M in Cardano Critical Integrations V2 actually going to be spent on?

## Answer

CCI V2 is a **12-month operations budget**, not a second build-out. Roughly **90% (₳20.7M)** pays recurring vendor fees and Cardano-side ops to keep four V1 integrations live, plus **Fireblocks Year 1** (integration fee + first annual platform fee). The remaining **~10%** splits evenly between a ring-fenced enhancement/tooling reserve (returned if unused) and legal/audit/admin.

### Public budget (vendor splits confidential)

| Category | ₳ | % | What it pays for |
|----------|---:|--:|------------------|
| Integration & maintenance | 20,700,000 | ~90% | Year 2 licensing/platform/attestation fees to Circle, LayerZero, Pyth, Dune; Cardano-side attestor/DVN/oracle/subgraph ops; protocol-upgrade compatibility; Fireblocks blockchain integration + Year 1 platform fee |
| Enhancement & tooling reserve | 1,150,000 | ~5% | SDKs (e.g. USDCx SDK), monitoring, reconciliation, observability — Steering Committee drawdowns; **returned to treasury if unused** |
| Legal, audit, contract admin | 1,150,000 | ~5% | Article II.7.4 audits, due diligence, contract administration |
| **Total** | **23,000,000** | 100% | |

### Per-integration maintenance (within the ₳20.7M line)

| Integration | V2 spend (conceptual) |
|-------------|----------------------|
| **Circle USDCx** | Attestor infrastructure and operations, monitoring, contract-administrator oversight |
| **LayerZero** | Cardano endpoint ops, DVN configuration/validator support, upstream protocol-version compatibility |
| **Pyth** | Oracle feed continuity, publisher incentives, Cardano-specific infrastructure |
| **Dune** | Subgraph coverage, schema maintenance, Cardano dashboard refresh |
| **Fireblocks** *(new in V2)* | Native ADA/CNT custody and transfer; foundations for staking and governance delegation; integration fee + Year 1 platform fee |

### V1 vs V2 framing

| | CCI V1 | CCI V2 |
|--|--------|--------|
| Ask | ₳70M | ₳23M |
| Window | 24 months | 12 months |
| Primary purpose | Initial delivery and launch readiness | Sustain live integrations + one new integration |
| Implied annual pace | ~₳35M/year (build-heavy) | ~₳23M/year (run-rate + Fireblocks Y1) |

The proposal states V1 contracts run through 2025 into early 2026; **Year 2 vendor fees** for Circle, LayerZero, Pyth, and Dune are contracted and due within the V2 window. Without V2, each maintenance renewal would need its own treasury action.

### Explicitly **not** in this ₳23M

- USDT0, LayerZero OFT expansion, other new tier-1 integrations
- Dapp grants, liquidity programs, marketing/events
- Application-layer investments

Each is reserved for separate governance actions.

### Recurring-cost implication

The rationale frames **annual licensing and platform fees as baseline operating expense** for as long as each integration stays live. V2 covers one 12-month window; the proposal does not commit a Year 3 figure on-chain, but the narrative implies **future treasury actions** unless integrations become self-funding (they are not modeled that way here).

### What voters cannot see

Partner NDAs block **per-vendor dollar/ADA splits**. Oversight relies on Pentad Steering Committee allocation, Intersect TRSC disbursement, bi-annual reports, and independent audits — not a public line-item budget per Circle/LayerZero/Pyth/Dune/Fireblocks.

## Sources

- [[sources/cardano-critical-integrations-v2]]
- [[proposals/cardano-critical-integrations-v2]]
- [[proposals/cardano-critical-integrations-v1]]
- [[concepts/cardano-critical-integrations]]
