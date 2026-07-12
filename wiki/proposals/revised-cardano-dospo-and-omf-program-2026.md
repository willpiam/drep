# Revised Cardano dOSPO and OMF Program (2026)

**Type:** Treasury withdrawal (open source sustainment pilot)  
**Proposer:** [[entities/christian-taylor|Christian Taylor]] / Open Source Cowboy Consulting  
**Administrator:** Open Source Cowboy Consulting — sole Article II.7.5 administrator at withdrawal  
**Auditor:** Mill Law Firm (independent; quarterly + annual)  
**Source:** [[sources/revised-cardano-dospo-and-omf-program-proposal]]  
**Prior version:** *Cardano dOSPO and OMF Program* — ₳12M / 36 months ([raw](../raw/bafybeialmkgxruw4oigiyv77ixm6yjjrjfh55danwq2u46hqwo4flicrhi.json)); DRep **abstain** when >98% NO ([vote 57](../../vote_context/markdown/57_dOSPO.md))

Christian Taylor requests **₳4,094,000** over **12 months** to pilot a **[[concepts/dospo-omf|dOSPO/OMF]]** stack: data-driven maintenance funding, contributor pipelines, bounties, and activation programs for Cardano open source infrastructure — operated independently of IOG, Cardano Foundation, and EMURGO.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳4,094,000 |
| Duration | 12 months (pilot to prove model) |
| Deposit | ₳100,000 |
| Withdrawal stake | `stake1uxgkzrl5sj2j2s934nj8lqxq9f5wey4w4r2r0k2xcez67ucmt09vd` |
| Administrator | Christian Taylor / Open Source Cowboy Consulting — effective at withdrawal |
| Legal entity target | US 501(c)(3) public charity by month 6 (M1.2) |
| Predecessor program | [[concepts/paid-open-source-model|POSM]] at Intersect (treasury to Intersect MBO, not proposer personally) |
| Whitepapers | dOSPO v1.0, OMF v1.0 (March 2026) |

## Work packages

| WP | Name | Budget (ADA) | Core deliverable |
|----|------|-------------:|------------------|
| WP1 | Operations and governance infrastructure | 760,000 | Councils, 501(c)(3), quarterly reporting |
| WP2 | Maintenance Fund | 2,000,000 | Dependency audit, tiered retainers, CHAOSS dashboard |
| WP3 | Maintainer Development | 1,000,000 | Mentor–mentee cohorts, on-chain attestations |
| WP4 | CodeForUs bounty program | 167,000 | Merged-work bounties + shared tooling stream |
| WP5 | Ecosystem Activation Reserve | 167,000 | Summer of Code, hackathons, contributor funnel |
| **Total** | | **4,094,000** | |

### WP2 — Maintenance Fund (core)

Months 1–3: full Cardano OSS dependency audit — SBOMs (SPDX/CycloneDX), centrality scores, bus-factor analysis, coverage gap report. Retainer selection follows a published priority formula approved by the External Open Source Advisory Council.

| Tier | Centrality / bus factor | Projects | Annual range (ADA) |
|------|-------------------------|----------|-------------------|
| 1 | 70+, bus factor 1–2 | ~10 | 80,000–120,000 |
| 2 | 40–70, bus factor 2–3 | 6–8 | 40,000–70,000 |
| 3 | <40 | up to 8 | 20,000–40,000 |

**Portfolio reserve:** ₳175,000 for mid-cycle additions; returned if undeployed.

Targets: **15+** high-centrality projects funded by month 12; bus factor **2+** for all top-20 centrality projects.

### WP3 — Maintainer Development

Two tracks (Core infrastructure, Tooling) with four-stage ladder: New Contributor → Committer → Trusted Committer → Core Maintainer. Completions recorded as on-chain attestations against Cardano stake keys. One cohort per track in the 12-month pilot.

### WP4 — CodeForUs

Standing bounty pool (individual cap ₳30,000) plus tooling sustainability stream for shared CI/SDK infrastructure. Payment after merge + 30-day post-integration monitoring.

### WP5 — Ecosystem Activation

Cardano Summer of Code (1 cycle), 2 hackathons, operations — top-of-funnel for WP3/WP4. **Reserve:** ₳44,000 returned if undeployed.

## Governance and oversight

### Article II.7.5 administrator

Unlike the original ₳12M proposal (which deferred entity formation and gave councils stronger pre-funding gatekeeping), the revised proposal **names the administrator unconditionally at withdrawal**:

| Property | Detail |
|----------|--------|
| Designation | Christian Taylor / Open Source Cowboy Consulting |
| Effective | Moment of treasury withdrawal through month 12 |
| Replaceability | On-chain DRep Info Action at any time |
| Sunset | Same Info Action route; uncommitted funds returned within 30 days |
| Sponsor commitment | Proposer will sponsor Info Action if **15+ DReps** request replacement or shutdown |

Month 7+ transition to the 501(c)(3) entity is **advisory-only** from councils; requires separate on-chain Info Action approval.

### Advisory councils (non-administrator)

| Council | Max members | Role |
|---------|------------:|------|
| External Open Source Advisory Council | 7 | OS experts (min 3 non-Cardano); retainer rubrics |
| Technical Community Advisory Council | 7 | Cardano contributors, min 1 SPO; DReps eligible |

Both are **advisory only** — written feedback published on-chain before each disbursement; **no veto**. Administrator makes final allocation within published parameters. Constituted by week 6 (M1.1); zero founding-entity employees on councils.

### Four-layer assurance

1. **Financial audit** — Mill Law Firm quarterly + annual  
2. **Program effectiveness audit** — annual KPI assessment by independent party  
3. **On-chain transparency** — withdrawals and disbursements publicly verifiable  
4. **Advisory council oversight** — published feedback; either council may request special audit (administrator responds within 14 days)

## Treasury repayment

| Reserve | Amount (ADA) | Condition |
|---------|-------------:|-----------|
| WP2 portfolio reserve | 175,000 | Returned at term end if undeployed |
| WP5 activation reserve | 44,000 | Returned if undeployed |
| Operational contingency | 100,000 | Returned after final Mill Law audit |
| Early termination | All uncommitted | Within 30 days of successful Info Action |

If M1.2 (501(c)(3) formation) not achieved by month 6, WP2 portfolio reserve **frozen** until milestone or governance alternative — does not affect administrator authority under Article II.7.5.

## Strategic alignment

**Pillars 1, 4, 5** — infrastructure sustainment, contributor growth, operational resilience layer between governance and maintenance execution.

Cites Harvard D3 (96% of codebases depend on OSS with <10 contributors), Linux Foundation maintainer risk, Tidelift burnout data, CNCF LFX mentorship outcomes, CHAOSS metrics framework.

## Proposer track record

Taylor founded Open Source Cowboy Consulting after serving as **Senior Manager of Open Source Governance and Head of OSPO at [[entities/intersect|Intersect]]**, where he designed the OSPO, contribution governance frameworks, and initial maintainer support model leading to POSM. Claims Intersect open source ops ran lean (two-person team for most of its existence). Independent of IOG, CF, EMURGO — no contractual ties to founding entities.

## DRep position

No vote context recorded for this **revised** action. The **original** ₳12M proposal: **abstain** ([vote 57](../../vote_context/markdown/57_dOSPO.md), 2026-06-06) — delegate declined deep review given >98% NO with 8 days remaining.

## Open questions

- Does naming a sole Article II.7.5 administrator at withdrawal adequately address delegate concerns that doomed the original proposal, or do structural objections (centralization, overlap with Intersect OSPO/POSM, proposer self-administration) persist?
- How will "deliberate non-overlap" with existing programs be enforced — especially vs [[proposals/pebble-ecosystem-maintenance-2026]], [[proposals/blockfrost-transformation-to-not-for-profit]], and Intersect technical stewardship?
- Is ₳4.09M over 12 months sufficient to fund 15+ high-centrality retainers plus ops, or does the budget assume significant undeployed reserves?
- What projects would Tier 1 retainers target — and how does dependency centrality scoring interact with proposer-named examples (Charli3, Taptools)?
- Council "advisory only" vs original "councils before funding" — does this weaken the decentralization claim or correctly separate constitutional administrator duty from community input?
- 501(c)(3) US entity: appropriate jurisdiction for a global Cardano program?
- Relationship to Intersect's ₳25.4M operations proposal — complementary ops layer or competing open source stewardship?

## Related

- [[entities/christian-taylor]]
- [[concepts/dospo-omf]]
- [[concepts/paid-open-source-model]]
- [[concepts/treasury-escrow-oversight]]
- [[concepts/cardano-typescript-tooling]]
- [[entities/intersect]]
- [[proposals/pebble-ecosystem-maintenance-2026]]
- [[proposals/blockfrost-transformation-to-not-for-profit]]
