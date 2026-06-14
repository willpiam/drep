# Hydra

**Hydra** is Cardano's **state-channel Layer 2**: participants move ledger state off L1, transact with sub-second finality and near-zero fees inside a **Head**, then settle the final state back on Cardano mainnet. It uses the same **Plutus scripts and EUTXO model** as L1 (isomorphic ledger), so contracts that run on Cardano run in Hydra unchanged.

## How it works

1. **Extract** — Relevant L1 state is committed into a Head (Hydra v2 allows opening heads without immediate fund commitment; funds can be added/removed incrementally).
2. **Process off-chain** — Transactions inside the Head confirm when participants sign snapshots; no L1 block competition.
3. **Reintegrate** — Final Head state is written to L1; mainnet reflects net off-chain activity.

**Safety model:** Every state advance requires signatures from all participants (unanimous consensus). A single honest participant can always reclaim funds on L1 — a **1-of-n honest** assumption, stronger than honest-majority Nakamoto or typical rollup sequencers.

## Setup modes

| Mode | Who runs nodes | Trust profile | Example use cases |
|------|----------------|---------------|-------------------|
| **Direct** | Each participant | No operator trust; co-sign every snapshot | Institutional OTC, agent-to-agent commerce (Masumi), B2B rails |
| **Delegated** | Operators run head; users via app layer | Federated operators; L1 remains settlement backstop | Perpetual DEXes (Delta DeFi), prediction markets, RWA, retail PoS |

Hydra is **not positioned for retail in direct mode**; delegated setup serves consumer-facing apps where application-layer trust already exists.

## Performance claims (proposal, 2026)

| Metric | L1 (cited) | Hydra Head |
|--------|------------|------------|
| Finality | 2+ hours | Sub-second (in-Head) |
| Fees | ~$0.17 payment; $1–3 DeFi | Near-zero (configurable) |
| Throughput | ~7–10 TPS | Up to 1,000+ TPS (payments); lower for script-heavy DeFi |

Aggregate throughput scales roughly linearly with parallel Heads.

## Production status (2026 proposal)

IOG describes Hydra as the **only production-grade L2 on Cardano** with live workloads:

- **Delta DeFi** — Perpetual DEX; entire product on Hydra
- **Masumi** — Agent-to-agent commerce; buyer/seller agents each run hydra-nodes
- **Intersect** — Governance voting infrastructure on Hydra
- **VTech Labs** — HydraHub (managed heads), HydraOne (DApp marketplace)
- **Blockfrost** — Zero-fee instant payments between SPOs and users
- **Glacier Drop** — 30M+ user cross-chain routing stress test
- **Hydra Doom**, **Hydra Vending Machine** — Gaming and PoS demonstrations
- **Midgard** — Fast withdrawals enabled by Hydra

Pipeline integrators cited: Bodega Market, Atlas Defi, Wingriders, Houselink, European Public Network.

**Protocol releases:** v1.3 (stable); v2 alpha (incremental fund management); partial fanout shipped ahead of schedule.

## Relationship to L1 scaling

[[concepts/leios|Leios]] (10–50× throughput target) and [[concepts/peras|Peras]] (~2 min finality) strengthen L1 but, per IOG's scaling-trilemma argument, cannot match zero-fee sub-second interaction envelopes that high-performance apps require. Hydra addresses **finality and cost gaps today**; L1 upgrades expand base-layer capacity in parallel.

L2 activity is framed as **expanding the pie**, not cannibalizing L1: perpetual DEX volume, agent micropayments, and gaming economies are economically impractical on L1 and would otherwise migrate to Solana or Ethereum L2s. Head lifecycle transactions and optional fee routing create L1 settlement revenue as adoption scales.

## Treasury funding

[[proposals/io-hydra|IO: Hydra]] (2026) requests **₳5,100,781** for v2 hardening across four workstreams: performance optimization, operational excellence, ecosystem support, and maintenance/DevX. Administered by [[entities/intersect|Intersect]] via TRSC/PSSC.

## Open questions

- How do Hydra v2 production milestones align with Leios/Peras L1 activation timelines?
- What measurable KPIs (TPS benchmarks, uptime, integrator count) will milestone acceptance enforce?
- How does delegated-setup operator trust compare to competing L2 sequencer models in practice?
- Can permissionless AMM/shared-liquidity DeFi be served by Hydra, or is the realistic segment operator-mediated venues only?

## Related

- [[proposals/io-hydra]]
- [[sources/io-hydra]]
- [[entities/input-output-group]]
- [[concepts/leios]]
- [[concepts/peras]]
