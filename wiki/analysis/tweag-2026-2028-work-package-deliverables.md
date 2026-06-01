# Tweag 2026–2028 Work Package Deliverables

**From ingest:** 2026-06-01  
**Source:** [[sources/tweag-core-cardano-infrastructure-2026-2028]] (full PDF `wiki/raw/tweag.pdf`, dated 2025-03-31)

## Budget by work package

| Work package | Budget (₳) |
|--------------|------------|
| Peras v1 ready for mainnet | 4,954,688 |
| Peras v2 improvements and resilience | 8,240,040 |
| History Expiry | 2,816,016 |
| Hard Fork Incident Mempool Bridger | 1,478,408 |
| Conformance Testing of Consensus: Peras and Leios | 4,860,760 |
| Conformance Testing: adversarial fork branches | 1,408,008 |
| Canonical ledger state & Mithril integration | 2,464,014 |
| Plutus Script Re-Executor ecosystem integration | 6,724,024 |
| Mutation Testing for Cardano | 1,408,008 |
| Hoarding Node: live deployment | 2,969,336 |
| Hoarding Node: distributed mode | 469,336 |
| Hoarding Node: embedded consensus validation | 469,336 |
| Hoarding Node: transaction collection | 352,002 |
| Block Cost Investigation Extensions | 469,336 |
| Cardano-node-emulator maintenance | 469,336 |
| Genesis Sync Accelerator maintenance | 234,668 |
| **Total** | **39,787,316** |

Per-package PDFs are linked from the on-chain JSON reference bundle (`ipfs://QmNcegfkH3WFf8xgjrKKTH9YoMRdmkAYUvCwmJy514XxdK`).

## Delivery model

Nine infrastructure areas, **17 work packages**, treated as one **non-modular pipeline**. Hoarding Node deployments plus conformance, mutation, and audit testing provide scaffolding to validate Peras v1/v2, History Expiry, and block-cost changes.

**Governance separation:** Vendor commits to **ready-for-activation** outputs (merged code, releases, runbooks, benchmarks, governance-action packages). Mainnet activation (HFC, CIP progression) is tracked separately with owners and risks.

**Duration:** 2 years (2026–2028), aligned with HFC cadence; Peras v2 starts in parallel with v1 finalization.

## Per-package summary

| # | Package | Nature | Core deliverables / milestones |
|---|---------|--------|--------------------------------|
| 1 | **Peras v1** | Continuation | Historical certificates; production crypto (BLS placeholder until research finalizes); KillSwitch; on-chain parameters; `cardano-cli` certificate tooling; preprod → mainnet HFC readiness (T1.1–T1.5) |
| 2 | **Peras v2** | Continuation | Pre-agreement (pre-vote / BA / vote) to avoid cooldown under &lt;25% adversarial stake; faster cooldown recovery; N2N and memory/CPU optimizations; committee selection refinements |
| 3 | **History Expiry** | New | CIP for partial-history nodes; production node implementation; operator migration tooling; full header chain retained, truncated block history |
| 4 | **Hard Fork Mempool Bridger** | New | Cross-chain tx propagation during fork incidents; docker image + runbook; ≥80% orphaned-fork txs re-included in canonical chain (private testnet metric) |
| 5 | **CTC: Peras & Leios** | Continuation | Extend Cardano Testing Conformance framework for Peras and Leios |
| 6 | **CTC: adversarial forks** | Continuation | Generate forks from adversarial branches; Genesis property-based test improvements |
| 7 | **Canonical ledger state & Mithril** | Continuation | Build on CIP-0165; new CIP for snapshot generation; SCLS integration in snapshot-converter; Mithril verification demo (success if public integration demo, not full Mithril ownership) |
| 8 | **Plutus Script Re-Executor** | Continuation | Largest single line item; CIP pathway; UI, CLI, cookbook; leashed-node debugging without separate ledger replica |
| 9 | **Mutation Testing** | New | Mutation engine for Haskell/Cardano tests; mutation score reporting |
| 10–13 | **Hoarding Node** (4 packages) | Continuation / new extensions | Live network deployment; distributed mode; embedded consensus validation; transaction collection |
| 14 | **Block Cost Investigation** | Continuation | Empirical/analytical block cost models under higher throughput |
| 15 | **Cardano Node Emulator** | Maintenance | Protocol-version compatibility |
| 16 | **Genesis Sync Accelerator** | Maintenance | Ongoing compatibility (PDF spells "Genesys" in places) |

## Peras v1 success metrics (vendor vs governance)

Vendor-controlled engineering targets; **mainnet activation** depends on governance:

| Metric | Target |
|--------|--------|
| Median settlement time | ≤ 5 minutes under non-degraded conditions and ≤25% adversarial stake (vs ~12 min Praos baseline) |
| Storage overhead vs Praos | ≤ 30% increase under same conditions |
| KillSwitch | No emergency activation in first 6 epochs (~30 days) after mainnet activation |
| Finality (expected value narrative) | ~2 minutes with overwhelming probability under standard assumptions |

Cryptography subcontract: **₳1.2M** CBU/ARK research line items appear in Peras v1 and v2 budgets.

## Strategic pillars (proposal)

- **Pillar 1:** Infrastructure and Research Excellence  
- **Pillar 5:** Ecosystem Sustainability and Resilience  

## Sources

- [[sources/tweag-core-cardano-infrastructure-2026-2028]]
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]]
- `wiki/raw/tweag.pdf`
