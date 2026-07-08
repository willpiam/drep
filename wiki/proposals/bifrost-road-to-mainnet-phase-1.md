# Bifrost Road to Mainnet (Phase 1)

**Type:** Treasury withdrawal (Bitcoin-Cardano bridge hardening and launch preparation)  
**Proposers:** [[entities/fluidtokens|FluidTokens]] + [[entities/lantr-engineering|Lantr Engineering]]  
**Administrator model:** SundaeSwap treasury-contract escrow with independent board oversight  
**Source:** [[sources/bifrost-unlocking-bitcoin-defi-on-cardano-road-to-mainnet-phase-1-of-2]]

The proposal requests **₳12,332,031** over 9 months to deliver Phase 1 of Bifrost: harden and audit the bridge, run external security validation, deploy to private mainnet in both custody modes, and establish stewardship/economic foundations for a later public launch.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳12,332,031 |
| USD reference | ~$1,973,125 at $0.16/ADA |
| Delivery window | July 2026 to March 2027 (9 months) |
| Scope boundary | Phase 1 only (public launch + 24-month operations moved to Phase 2) |
| Build status at submission | Catalyst-funded testnet live and on track |

## Delivery scope

Three tracks run in parallel:

1. **Bridge hardening & security** — contracts/off-chain hardening, audits, formal verification, QA, runbooks, deployment prep.
2. **Ecosystem readiness & partnerships** — SPO onboarding and dApp integration pipeline before public launch.
3. **Legal, stewardship & economy** — independent stewardship structure plus hardened fee/reserve/incentive model.

Milestones target: audit readiness (M1), audit completion and mainnet prep (M2), and audited private mainnet operations in both custody modes with real BTC under controlled access (M3).

## Budget snapshot

| Track | USD | ADA | Share |
|------|----:|----:|------:|
| Bridge hardening & security | 1,363,750 | 8,523,438 | 76.0% |
| Ecosystem readiness & partnerships | 177,500 | 1,109,375 | 9.9% |
| Legal, stewardship & economy | 252,500 | 1,578,125 | 14.1% |
| **Subtotal** | **1,793,750** | **11,210,938** | **100%** |
| Refundable contingency (10%) | 179,375 | 1,121,094 | - |
| **Total** | **1,973,125** | **12,332,031** | - |

## Technical model

- BTC is locked under a Taproot script and represented on Cardano as **fBTC**.
- Custody authorization targets a large Cardano SPO threshold-signing set, with federated fallback for continuity.
- Watchtowers post Bitcoin confirmations to Cardano; users perform self-service claim and withdrawal flows.
- Proposal includes atomic-swap "fast lane" and SDK/white-label integration path for Cardano dApps.

See [[concepts/bifrost-bitcoin-defi-bridge]] for the bridge-model framing and comparative claims.

## Governance and controls

- **Escrow:** SundaeSwap treasury-contract framework with milestone-gated disbursements.
- **Oversight:** independent board co-signers can pause milestones; independent technical assurer and external financial audit are scoped.
- **Refundability:** unused contingency and end-of-term unspent funds are designed to return to Treasury.
- **Stewardship transition:** an independent long-term stewardship structure is promised as a Phase 1 deliverable before Phase 2 public launch.

## DRep position

No published local vote-context markdown for this proposal is ingested yet, so no DRep position is recorded here.

## Open questions

- What objective thresholds decide readiness to transition from private mainnet (M3) to public launch in Phase 2?
- Which audits/firms are contractually committed vs planned?
- How much private-mainnet BTC exposure is acceptable before public activation?
- How will governance rights be split between stewardship-body decisions and Cardano on-chain governance for structural changes?
- What measurable evidence will validate claimed dApp integration commitments prior to Phase 2 funding?

## Related

- [[concepts/bifrost-bitcoin-defi-bridge]]
- [[entities/fluidtokens]]
- [[entities/lantr-engineering]]
- [[concepts/treasury-escrow-oversight]]
