# Research delivery pipeline (IOR / ARC / CBU)

Cardano Vision 2026 describes an **integrated operating model** that replaces a linear “publish then hope” research flow with a staged pipeline from discovery to deployment.

## Three functions

| Unit | Role |
|------|------|
| **IOR** (Input Output Research) | Scientific investigation: protocols, models, security proofs |
| **ARC** (Applied Research & Creative Engineering) | Prototypes, simulations, specifications; feasibility validation |
| **CBU** (Cardano Business Unit) | Product alignment, use cases, go-to-market |

## TRL funnel

- **Fundamental research** — ≤ TRL2: new designs and formal analysis
- **Technology validation** — TRL3–5: prototypes and specs
- **Implementation** — TRL5+: engineering support for production

## Outputs taxonomy (Vision 2026)

1. **Novel science** — ~38 papers/reports (PQ, networking, Plutus, consensus/MEV, ZK, interoperability, economics/governance)
2. **Innovation validation** — ~9 CPS + ~12 prototypes (HSM node, ZK toolkit, Cavefish light client, bridges, identity, etc.)
3. **Implementation-ready** — ~5 CIPs (PQ migration, governance/identity, minUTXO, etc.)

## Governance checkpoints

Quarterly updates; bi-annual reports via Intersect; public **Cardano R&D Sessions**; four funding tranches (25% each) tied to contract execution, mid-year report, Q3 R&D session, year-end report.

## Illustrative example

**Ouroboros** family evolution (Classic → Praos → Genesis → Omega) plus modular **[[concepts/peras|Peras]]** and **[[concepts/leios|Leios]]** upgrades demonstrates the long arc; Peras/Leios 2026 readiness is the near-term pipeline outcome.

## Engineering delivery lane

IOR explicitly excludes production hard-fork work (IO Consensus Initiative). [[entities/tweag|Tweag]]'s [[proposals/tweag-core-cardano-infrastructure-2026-2028|2026–2028 treasury proposal]] represents the complementary **engineering delivery** track: mainnet Peras, History Expiry, conformance/mutation/adversarial testing, Hoarding Node observability, and developer tooling — funded separately from IOR research but positioned as one integrated activation pipeline.

## Related

- [[entities/io-research]]
- [[entities/tweag]]
- [[concepts/cardano-vision]]
- [[concepts/peras]]
- [[sources/cardano-vision-2026-ior]]
- [[sources/tweag-core-cardano-infrastructure-2026-2028]]
