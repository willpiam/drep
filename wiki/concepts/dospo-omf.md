# dOSPO and OMF

The **decentralized Open Source Program Office (dOSPO)** and **Open Maintenance Framework (OMF)** are a paired governance-and-operations model for sustaining Cardano's open source infrastructure as long-term public goods. Architecture is specified in v1.0 whitepapers (March 2026, opensourcecowboy.com) co-developed by [[entities/christian-taylor|Christian Taylor]] with Bitergia, CHAOSS, ASF, LFDT, Intersect, Andamio, Modus Create, and others.

## Position

Cardano's protocol security depends on maintained libraries, wallet SDKs, developer tooling, and indexers — often with low bus factors and episodic grant funding. dOSPO/OMF proposes a **neutral operational layer** that executes sustainability mandates under governance oversight without replacing on-chain governance itself.

The model evolves lessons from Intersect's **[[concepts/paid-open-source-model|Paid Open Source Model (POSM)]]**, which showed demand for maintainer retainers but exposed limitations when committees approve funding but cannot continuously operate programs.

## Four programs

| # | Program | Purpose |
|---|---------|---------|
| 1 | **Maintenance Fund** | Long-term retainer funding for highest-risk infrastructure, selected by dependency centrality data |
| 2 | **Maintainer Development** | Structured mentor–mentee pipelines with on-chain stake-key attestations |
| 3 | **CodeForUs** | Delivery bounties (security fixes, deps, docs, tests) + tooling sustainability stream |
| 4 | **Ecosystem Activation Reserve** | Summer of Code, hackathons, contributor entry funnel |

Selection follows **published dependency centrality and bus-factor data**, not relationships. All programs carry explicit sunset criteria; the operator is replaceable via on-chain governance.

## Governance structure (revised 2026 pilot)

[[proposals/revised-cardano-dospo-and-omf-program-2026]] defines:

| Body | Authority |
|------|-----------|
| **Article II.7.5 administrator** | Christian Taylor / Open Source Cowboy Consulting — sole administrator at withdrawal; final allocation within published parameters |
| **External Open Source Advisory Council** (max 7) | Advisory — retainer rubrics, allocation feedback published before disbursement |
| **Technical Community Advisory Council** (max 7) | Advisory — technical scope, bounty criteria; min 1 SPO |
| **Mill Law Firm** | Independent financial auditor — quarterly + annual |
| **DReps** | Replace administrator or sunset program via Info Action |

Advisory councils are **not** Article II.7.5 administrators and have **no veto**. A US **501(c)(3)** public charity is a month-6 deliverable; transferring administrator authority to it requires a separate on-chain Info Action.

## Dependency-driven maintenance (OMF core)

WP2 Maintenance Fund workflow:

1. Full OSS stack dependency audit (months 1–3) — SBOMs (SPDX/CycloneDX), centrality scores, bus factors
2. Published priority formula (External OS Advisory Council approval)
3. Three retainer tiers by centrality and bus factor
4. CHAOSS-aligned public health dashboard
5. Quarterly portfolio review and end-of-term assessment

**KPI targets (12-month pilot):** 40% of top-50 dependencies funded; bus factor 2+ for top-20; <15% maintainer attrition; <48h security disclosure-to-assessment; 100% quarterly transparency.

## Original vs revised proposal

| Dimension | Original (failed) | Revised (pilot) |
|-----------|-------------------|-----------------|
| Budget | ₳12,000,000 | ₳4,094,000 |
| Duration | 36 months | 12 months |
| Administrator | "Founding Coordinator"; entity from month 7 | Named Article II.7.5 administrator at withdrawal |
| Councils | Constituted before funding; stronger gatekeeping language | Advisory only; feedback before disbursement |
| Council authority | Described as approving rubrics/eligibility | Explicitly no veto |

Original raw: [bafybeialmkgxruw4oigiyv77ixm6yjjrjfh55danwq2u46hqwo4flicrhi.json](../raw/bafybeialmkgxruw4oigiyv77ixm6yjjrjfh55danwq2u46hqwo4flicrhi.json). DRep abstain on original ([vote 57](../../vote_context/markdown/57_dOSPO.md)).

## Related proposals and concepts

- [[proposals/revised-cardano-dospo-and-omf-program-2026]] — 12-month treasury pilot
- [[concepts/paid-open-source-model]] — Intersect predecessor programs
- [[concepts/treasury-escrow-oversight]] — contrasts TRSC, self-admin, and Article II.7.5 patterns
- [[concepts/cardano-typescript-tooling]] — example maintenance target surface
- [[proposals/pebble-ecosystem-maintenance-2026]] — project-specific TypeScript maintenance ask
- [[proposals/blockfrost-transformation-to-not-for-profit]] — hosted API public-good transition

## Open questions

- Can dependency centrality scoring be community-verified and resistant to gaming?
- How does dOSPO/OMF coordinate with — or avoid duplicating — Intersect technical stewardship and existing maintainer grants?
- Does a 12-month pilot produce enough evidence to justify continuation without re-litigating governance structure?
