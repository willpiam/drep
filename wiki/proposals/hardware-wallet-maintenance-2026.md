# Hardware Wallet Maintenance 2026

**Type:** Treasury withdrawal (hardware wallet compatibility maintenance)  
**Submitter:** [[entities/intersect|Intersect]] (on behalf of vendor)  
**Administrator:** Intersect (2026 TRSC/PSSC)  
**Source:** [[sources/withdraw-hardware-wallet-maintenance-2026]]  
**On-chain recipient:** `stake1784sdxt6jjennmstphgdu7l7c2scf5d02a6cve2dgn5s2kq5u3j9v` (2026 TRSC)

Intersect requests **₳1,310,960** for **12 months** of production maintenance keeping Cardano **Ledger and Trezor** hardware-wallet flows operational — including **cardano-hw-cli**, **cardano-hw-interop-library**, integrator developer support, and vendor-triggered audits.

## Context

| Item | Detail |
|------|--------|
| Total ask | ₳1,310,960 |
| Duration | 12 months (2026) |
| Work package | WP1 — Hardware Wallet Maintenance & Compatibility Assurance |
| Intersect admin fee | ₳38,183 |
| Budget process | Passed 67% Hydra voting threshold in 2026 Intersect Budget Process |
| Vendor | Not named in on-chain metadata; tooling history suggests [[entities/vacuumlabs|VacuumLabs]] |
| Interop standard | **[[concepts/hardware-wallet-interoperability|CIP-21]]** |

## Scope

**In scope:** Ledger/Trezor compatibility updates; cardano-hw-cli and interop library maintenance; ecosystem integrator support; externally maintained component paths where HW flows intersect; vendor-required audits after firmware/app changes.

**Out of scope:** New wallet product development; core-node, ledger, or general infrastructure maintenance (separate budgets).

## Budget

| Work package | Amount (₳) |
|--------------|----------:|
| WP1 — Hardware Wallet Maintenance & Compatibility Assurance | 1,272,777 |
| Intersect Budget Administration fee | 38,183 |
| **Total** | **1,310,960** |

Delivery uses capped time-and-materials reporting with milestones and evidence for DRep verification.

## Strategic alignment

- **Pillar 1 (primary):** Preserves secure, reliable, interoperable signing as Cardano, Ledger, and Trezor evolve.
- **Pillar 2 (secondary):** Adoption depends on HW flows for DeFi, payments, stablecoins; developers need maintained libraries and CLI tooling.

## Governance and controls

**2026 TRSC/PSSC** ([[entities/sundae-labs|Sundae Labs]] framework):

| Address | Role |
|---------|------|
| `stake1784sdxt6jjennmstphgdu7l7c2scf5d02a6cve2dgn5s2kq5u3j9v` | 2026 TRSC stake |
| `addr1x84sdxt6jjennmstphgdu7l7c2scf5d02a6cve2dgn5s2k8tq6vh499n88hqkrwsmealas4psng674m4sej5638fq4vqmxs59w` | 2026 TRSC payment |
| `addr1x9d6k9z6t6fvsetj2djmerargk475lef9gfvshy4rwh4h7jm4v295h5jepjhy5m9hj86x3dtafljj2sjepwf2xa0t0aq048cay` | 2026 PSSC payment |

**Oversight Committee (2026 roster):** Sundae Labs, [[entities/cardano-foundation|Cardano Foundation]], Dquadrant, NMKR, Sundial, **[[entities/eternl|Eternl]]** — six trusted entities verifying admin actions on-chain (replaces Xerberus from 2025 roster).

Process: enactment → funds to TRSC stake → Fund action to PSSC when legal contract ready → milestone-gated disbursement. Dashboard: [treasury.sundae.fi budget 51486a2f…](https://treasury.sundae.fi/budgets/51486a2f1496d4d3a688a9b111971aa9b731ed045d900b601345ca4e).

**NCL:** TREASURY-02a compliant at submission (350M net change limit, epochs 613–713).

## Prior funding disclosure

| Source | Link |
|--------|------|
| Hardware Wallets Maintenance (2025) | [gov.tools](https://gov.tools/governance_actions/8ad3d454f3496a35cb0d07b0fd32f687f66338b7d60e787fc0a22939e5d8833e#3) |
| Ledger App Rewrite (2025) | [gov.tools](https://gov.tools/governance_actions/8ad3d454f3496a35cb0d07b0fd32f687f66338b7d60e787fc0a22939e5d8833e#9) |
| IO & VacuumLabs Plutus (joint) | [gov.tools](https://gov.tools/governance_actions/73e171a4c0730b4b59ecae271ab89f12a9d56360b02920e1f95107dbdc1d6762#6) |
| Catalyst (Ledger Live, message signing, CTF, tokens) | Multiple Fund 9–12 projects cited in metadata |

## DRep position

No completed DRep vote context is currently recorded.

## Open questions

- Confirm contracted vendor identity and public milestone schedule.
- How does recurring ₳1.3M/year maintenance compare to Catalyst-funded one-offs for the same stack?
- Trezor still lacks Conway governance fields per CIP-21 — does this maintenance scope include closing that gap?
- **Eternl** sits on the 2026 Oversight Committee while also requesting a separate self-administered treasury withdrawal — evaluate independence.

## Related

- [[concepts/hardware-wallet-interoperability]]
- [[sources/cip-21-hardware-wallet-interoperability]]
- [[entities/vacuumlabs]]
- [[entities/sundae-labs]]
- [[entities/intersect]]
- [[entities/eternl]]
- [[concepts/treasury-escrow-oversight]]
- [[proposals/eternl-path-to-sustainability-2026-2027]]
