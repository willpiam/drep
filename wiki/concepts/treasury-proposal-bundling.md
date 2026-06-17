# Treasury proposal bundling

**Bundled treasury proposals** combine multiple work packages, budgets, or delivery streams into a **single governance action** rather than separate on-chain votes per line item. Cardano DReps and the community are still calibrating when bundling is appropriate versus when it obscures democratic choice.

## Tension

| Concern | Counter-argument |
|---------|------------------|
| Voters cannot approve or reject individual workstreams | Some pipelines are **interdependent** — splitting votes may fund incomplete activation paths (e.g. Peras without conformance testing or History Expiry under Leios load) |
| Large multi-year asks reduce milestone-level accountability | Multi-year continuity may match **real delivery horizons** when proposers need sustained engineering, not annual re-litigation |
| Less granular DRep control | Governance may need to operate at a **higher level of abstraction** while escrow/milestone frameworks handle detail |

## $computerman position (evolving)

Per [[sources/vote-56-tweag-core-cardano-infrastructure-2026-2028]] (2026-06-01):

- Bundled packages were once viewed skeptically; that view has **softened** for cases where integration is genuine.
- Many voters opposed [[proposals/tweag-core-cardano-infrastructure-2026-2028]] on **two-year timeline** and **bundling** grounds; the published YES vote accepts Tweag's framing that 17 packages form one pipeline and that a 2026–2028 horizon matches continuous development needs.
- **Proposer-stated success conditions** (timeline, scope shape) should inform delegate votes when the contractor is communicating what they need to deliver.

## Examples in this wiki

| Proposal | Bundling note |
|----------|----------------|
| [[proposals/tweag-core-cardano-infrastructure-2026-2028]] | 17 WPs, ₳39.8M, 2 years — DRep YES despite bundling objections in the community |
| [[proposals/cardano-vision-2026]] | 7 WPs under one IOR ask — separate engineering delivery via Tweag |
| IOG 2026 bundle | Broader multi-action withdrawal pattern — see legacy [vote 49](../../vote_context/markdown/49_iog_funding_2026.md) |
| [[proposals/cardano-critical-integrations-v2|CCI V2]] | Bundles maintenance for Circle, LayerZero, Pyth, Dune, Fireblocks, enhancement reserve, and admin — DRep **NO** ([vote 65](../../vote_context/markdown/65_critical.md)) partly on ₳70M→₳23M cadence and recurring-cost structure |

## Open questions

- When should Intersect or proposers split actions for voter granularity vs keep integrated pipelines?
- Do TRSC/PSSC milestone controls adequately substitute for per-WP governance votes?
- Does NCL or community policy eventually standardize maximum bundle size or duration?

## Related

- [[concepts/treasury-escrow-oversight]] — milestone and escrow detail below governance-action level
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]]
- [[proposals/cardano-critical-integrations-v2]]
- [[concepts/cardano-critical-integrations]]
- [[sources/vote-56-tweag-core-cardano-infrastructure-2026-2028]]
