# History Expiry

**History Expiry** is a Cardano node feature enabling **partial-history nodes** that retain only recent ledger history instead of the full chain. It addresses SPO storage economics as throughput increases under [[concepts/leios|Leios]].

## Problem

Per [[sources/tweag-core-cardano-infrastructure-2026-2028]], Leios-scale throughput could drive SPO disk usage to roughly **~1 GB/hour at 100–1000 TPS**. Without History Expiry, full-history requirements may become economically prohibitive, threatening decentralization.

## Design (PDF)

Partial-history nodes retain the **full header chain** while truncating block history to a configurable depth — analogous to Ethereum-style pruning, with precedent cited for **Amaru** on mainnet. Goal: a spectrum from lightweight partial-history nodes to full archival nodes without compromising security assumptions.

## Tweag delivery (2026–2028)

History Expiry (**₳2.82M**) is one of 17 work packages in [[proposals/tweag-core-cardano-infrastructure-2026-2028]], delivered as part of an integrated pipeline with [[concepts/peras|Peras]] and testing scaffolding. Tweag argues partial-history nodes must ship alongside throughput upgrades to preserve sustainable node operation.

**Core objectives:** Submit a **CIP** enabling partial-history operation; define network configuration parameters (minimum history window, protocol behavior); production node implementation; operator migration and monitoring tooling.

**Success metrics:** Share of mainnet nodes in partial-history mode; reduced per-node storage growth vs full-history under equivalent load; no increase in fork rate or validation errors vs baseline.

See [[analysis/tweag-2026-2028-work-package-deliverables]].

## Related

- [[concepts/leios]]
- [[concepts/peras]]
- [[entities/tweag]]
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]]

## Open questions

- Minimum history retention parameters and security implications for light clients and indexers
- Adoption path for SPOs transitioning from full-history to partial-history operation
- Coordination with [[concepts/hoarding-node|Hoarding Node]] and Canonical Ledger State (CIP-0165) for network observability
