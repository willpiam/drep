# Wirex Real-World Payments

**Type:** Treasury withdrawal (payments infrastructure / Visa card integration)  
**Submitter:** [[entities/intersect|Intersect]] (on behalf of [[entities/wirex|Wirex]])  
**Administrator:** Intersect (2026 TRSC/PSSC)  
**Source:** [[sources/withdraw-wirex-real-world-payments]]  
**On-chain action:** `gov_action1k02990lhw6wh74t7c6ufw3mqaek9ujtvyan99dj5qv5kvcs7pn8sqcw2nc5`  
**On-chain recipient:** `stake1784sdxt6jjennmstphgdu7l7c2scf5d02a6cve2dgn5s2kq5u3j9v` (2026 TRSC)

Intersect requests **₳3,961,538** for **WP1 — Enabling Onchain Payments & Card Infrastructure**: open-source payments rails connecting Cardano to banking, stablecoins, and wallets, with **Visa card issuance** linked directly to onchain balances.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳3,961,538 |
| Work package | WP1 — Enabling Onchain Payments & Card Infrastructure |
| Intersect admin fee | ₳115,385 |
| Budget process | Passed 67% Hydra voting threshold in 2026 Intersect Budget Process |
| Vendor | [[entities/wirex|Wirex]] |
| Prior treasury funding | None in prior 24 months |

## Scope

**In scope:** Full-stack open-source payments infrastructure — smart contract settlement, account abstraction, batched transactions, settlement logic, wallet and API ecosystem layer; Visa card issuance backed by onchain balances; banking-rail and stablecoin connectivity; self-custody wallet native integration.

**Strategic framing:** Addresses Cardano's gap in everyday spending, merchant acceptance, and fiat-connected financial activity. Wirex brings 7M+ users, 1.5M+ issued cards, $20B+ processed volume, and Visa Principal Member status.

All components released as **public goods** for wallet providers, fintechs, stablecoin issuers, and developers.

## Budget

| Work package | Amount (₳) |
|--------------|----------:|
| WP1 — Enabling Onchain Payments & Card Infrastructure | 3,846,153 |
| Intersect Budget Administration fee | 115,385 |
| **Total** | **3,961,538** |

## Strategic alignment

- **Pillar 1:** Core open-source on-chain infrastructure — smart contracts, account abstraction, batched transactions, settlement logic, wallet/API layer.
- **Pillar 2:** Payments is an explicitly identified high-value vertical; Wirex brings regulated, enterprise-grade financial utility (Visa cards, stablecoin-backed banking rails, compliance architecture).

Both pillars are treated as a single integrated initiative: Pillar 2 adoption outcomes depend on Pillar 1 infrastructure delivery.

## Governance and controls

**2026 TRSC/PSSC** ([[entities/sundae-labs|Sundae Labs]] framework):

| Address | Role |
|---------|------|
| `stake1784sdxt6jjennmstphgdu7l7c2scf5d02a6cve2dgn5s2kq5u3j9v` | 2026 TRSC stake |
| `addr1x84sdxt6jjennmstphgdu7l7c2scf5d02a6cve2dgn5s2k8tq6vh499n88hqkrwsmealas4psng674m4sej5638fq4vqmxs59w` | 2026 TRSC payment |
| `addr1x9d6k9z6t6fvsetj2djmerargk475lef9gfvshy4rwh4h7jm4v295h5jepjhy5m9hj86x3dtafljj2sjepwf2xa0t0aq048cay` | 2026 PSSC payment |

**Oversight Committee (2026 roster):** Sundae Labs, [[entities/cardano-foundation|Cardano Foundation]], Dquadrant, NMKR, Sundial, **[[entities/eternl|Eternl]]**.

Process: enactment → funds to TRSC stake → Fund action to PSSC when legal contract ready → milestone-gated disbursement. Dashboard: [treasury.sundae.fi budget 51486a2f…](https://treasury.sundae.fi/budgets/51486a2f1496d4d3a688a9b111971aa9b731ed045d900b601345ca4e).

**NCL:** TREASURY-02a compliant at submission (350M net change limit, epochs 613–713).

## Ecosystem context

This proposal complements but differs from **[[concepts/cardano-critical-integrations|CCI]]** stablecoin infrastructure (Circle USDCx attestor rails) and **[[concepts/hydra|Hydra]]** micropayment/L2 throughput work. Wirex targets **merchant-facing spend rails** (Visa cards, banking connectivity) rather than protocol-level stablecoin issuance or L2 scaling.

See [[concepts/real-world-payments]] for the broader payments-vertical framing.

## DRep position

Published vote context records **Interesting** (non-committal) on this action in the Intersect-managed batch ([vote 72](../../vote_context/markdown/72_many.md)). The batch rationale focuses primarily on TxPipe maintenance proposals; no dedicated Wirex conclusion text is recorded yet.

## Open questions

- What is the public milestone schedule and timeline for Visa card launch on Cardano?
- How does open-source infrastructure relate to Wirex's proprietary regulated card-issuing business?
- What stablecoin rails are in scope — native Cardano stablecoins, USDCx from CCI, or Wirex-issued balances?
- How does ₳3.96M compare to Wirex's existing $20B+ volume business case — is treasury funding catalytic or subsidizing a commercial product?
- Card-issuing compliance and geographic licensing — which jurisdictions are targeted first?

## Related

- [[concepts/real-world-payments]]
- [[entities/wirex]]
- [[entities/intersect]]
- [[entities/sundae-labs]]
- [[concepts/treasury-escrow-oversight]]
- [[concepts/cardano-critical-integrations]]
- [[concepts/hydra]]
- [[proposals/hardware-wallet-maintenance-2026]]
- [[proposals/cardano-critical-integrations-v2]]
