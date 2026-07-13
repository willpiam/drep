# Sundae Labs

**Sundae Labs** develops Cardano **treasury management smart contracts** used by [[entities/intersect|Intersect]] to administer major budget withdrawals. The framework provides **Treasury Reserve Smart Contracts (TRSC)** and **Project-Specific Smart Contracts (PSSC)** with multisig governance, milestone fund actions, pause/resume, and community-auditable dashboards.

## Position

Sundae Labs is both the **contract author** and a member of Intersect's **Oversight Committee** — co-signing TRSC/PSSC administrative actions alongside other trusted entities without discretion over governance decisions.

The contracts are audited (TxPipe, MLabs per proposal metadata) and deployed fresh each budget cycle. **2026 TRSC** addresses appear in [[sources/withdraw-hardware-wallet-maintenance-2026]] and other 2026 Intersect-submitted withdrawals.

## Framework features (typical)

| Action | Typical sign-off pattern |
|--------|------------------------|
| TRSC Fund / PSSC Modify | 2/5 Intersect admins + 2/6 trusted entities + 1/3 leadership |
| TRSC Disburse | 2/5 admins + 3/6 trusted + 2/3 leadership |
| TRSC Pause/Resume | 2/5 admins + 1/3 leadership |
| TRSC Sweep | 1/5 admins + 1/3 leadership |
| TRSC Reorganize | 2/5 admins + 3/6 trusted |

Funds in TRSC/PSSC delegate to the **auto-abstain predefined DRep** and cannot stake with an SPO.

## Resources

- [treasury-contracts GitHub](https://github.com/SundaeSwap-finance/treasury-contracts)
- [treasury.sundae.fi dashboards](https://treasury.sundae.fi/)
- [Intersect Smart Contract Guide](https://admin-services.docs.intersectmbo.org/governance/smart-contracts)

## Related

- [[entities/intersect]]
- [[concepts/treasury-escrow-oversight]]
- [[proposals/hardware-wallet-maintenance-2026]]
- [[proposals/wirex-real-world-payments]]
- [[proposals/cardano-vision-2026]]
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]]
- [[proposals/scalus-2026]] — Lantr vendor escrow via same treasury-contracts framework
- [[proposals/bifrost-road-to-mainnet-phase-1]] — referenced escrow pattern in Phase 1 metadata
