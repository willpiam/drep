# Hoarding Node

The **Hoarding Node** is network observability infrastructure for detecting and attributing anomalous Cardano network behavior — orphaned blocks, invalid slot leader claims, mempool anomalies, and adversarial patterns that are difficult to observe from standard node deployments.

## Role in core infrastructure

Per [[sources/tweag-core-cardano-infrastructure-2026-2028]], the Hoarding Node fills an observability gap required to safely validate [[concepts/peras|Peras]], [[concepts/history-expiry|History Expiry]], and block-cost changes. Tweag treats Hoarding Node work as part of the correctness scaffolding for the broader 17-package delivery pipeline.

## Work packages (Tweag 2026–2028)

Four related packages in [[proposals/tweag-core-cardano-infrastructure-2026-2028]]:

1. **Live network deployment**
2. **Distributed mode**
3. **Embedded consensus validation** of blocks and headers
4. **Transaction collection**

## Related

- [[entities/tweag]]
- [[concepts/peras]]
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]]

## Open questions

- Operational deployment model: who runs Hoarding Nodes and how is data shared with SPOs and developers?
- Relationship to existing monitoring tooling and MEV analysis in IOR research ([[proposals/cardano-vision-2026]])
