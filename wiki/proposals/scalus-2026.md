# Scalus 2026: Maintenance, Dijkstra Readiness, Interoperability & Application Runtime

**Type:** Treasury withdrawal (developer platform continuation)  
**Proposer:** [[entities/lantr-engineering|Lantr Engineering]]  
**Administrator model:** [[entities/sundae-labs|Sundae Labs]] treasury-contract escrow + independent oversight board  
**Source:** [[sources/scalus-2026-maintenance-dijkstra-readiness]]

The proposal requests **₳2,464,844** (~$394,375 at $0.16/ADA) over **9 months** (Jul 2026–Mar 2027) to maintain and extend **[[concepts/scalus|Scalus]]** through the **[[concepts/dijkstra-hard-fork|Dijkstra]]** hard-fork transition, deepen JVM/JS interoperability, and ship a scoped first application runtime.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳2,464,844 |
| USD reference | ~$394,375 at $0.16/ADA |
| Duration | 9 months (Jul 2026 – Mar 2027) |
| Staffing | 2.25 FTE (2.0 engineering + 0.25 PM) |
| Contingency | 0% |
| Prior treasury ask (rejected/resized) | ₳8,503,000 / 12 months — full application platform |
| Prior enacted treasury | ₳657,692 (2025 Scalus DApps platform — completed) |

## Scope

| In scope | Out of scope |
|----------|--------------|
| Maintenance, security patches, releases | Standalone production JVM L1 node |
| Dijkstra readiness (Plutus V4, nested tx, accounts, guard scripts) | Full Gummiworm L2 operator integration |
| JVM (Java/Kotlin) + JS/TS interoperability | Broad formal verification track |
| Scoped application runtime (chain follower, scheduler, persistence) | Advanced devnet expansion beyond Dijkstra/emulator needs |

## Milestones (quarterly)

1. **M1 (Q3 2026):** Continuity + Dijkstra developer preview; JS/TS interface improvements; runtime foundations.
2. **M2 (Q4 2026):** Dijkstra conformance progress; Java/Kotlin integration examples; chain follower + task scheduler.
3. **M3 (Q1 2027):** Dijkstra readiness aligned to hard-fork timeline; foundational runtime release; documentation/blueprints.

## Governance and controls

- **Escrow:** SundaeSwap `treasury.ak` / `vendor.ak` framework (audited by TxPipe, MLabs).
- **Oversight board:** Chris Gianelloni (Blink Labs), Matthias Benkort (Cardano Foundation), Riley Kilgore (IOG) — no Lantr stake; can pause milestones.
- **Technical assurer:** No.Witness Labs (quarterly reviews).
- **Financial audit:** External auditor; report targeted Q2 2027.
- **Delegation:** Auto-abstain DRep; no SPO delegation on escrowed funds.
- **Failsafe sweep:** Unspent funds return to Treasury at contract expiration.

## Resubmission rationale

DReps reportedly recognized prior Scalus vision and delivery record but found scope/budget too large. This proposal removes L1 node, L2 integration, and formal verification from the funded path; cuts ask ~71%; uses independent on-chain submission instead of bundled budget action.

## DRep position

No published local vote-context markdown for this proposal is ingested yet, so no DRep position is recorded here.

## Related

- [[concepts/scalus]]
- [[concepts/dijkstra-hard-fork]]
- [[concepts/cardano-typescript-tooling]]
- [[entities/lantr-engineering]]
- [[entities/sundae-labs]]
- [[proposals/bifrost-road-to-mainnet-phase-1]] — Lantr co-proposer; Scalus used in Bifrost stack
