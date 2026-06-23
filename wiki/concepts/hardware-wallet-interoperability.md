# Hardware wallet interoperability

**Hardware wallet interoperability** on Cardano is the requirement that software wallets, DApps, and CLI tools construct transactions that Ledger and Trezor devices can sign. **CIP-21** ([[sources/cip-21-hardware-wallet-interoperability]]) defines the canonical CBOR serialization and transaction-body restrictions that prevent ambiguity when HW wallets stream partial transaction data and return witness signatures only.

## Position

Cardano nodes accept a broader transaction set than HW wallets can process. Without a shared serialization format and explicit limits, users see signing failures or — worse — mismatches between what the device displays and what nodes execute (e.g. duplicate map keys in multiassets or withdrawals). Maintaining this layer is **security-critical**: HW wallets are the primary secure-signing path for many holders and integrators.

The **[[proposals/hardware-wallet-maintenance-2026|2026 treasury maintenance proposal]]** funds continuity of Ledger/Trezor app compatibility, **cardano-hw-cli**, and the **cardano-hw-interop-library** — the reference tooling named in CIP-21's implementation plan.

## CIP-21 core rules

| Area | Rule |
|------|------|
| Serialization | Canonical CBOR (RFC 7049 §3.9): minimal encodings, sorted map keys, definite lengths |
| Conway tags | Tag 258 in sets must be consistent (all or none) |
| Integers | int64 / uint64 bounds |
| Counts | ≤65535 per element class (inputs, outputs, certs, witnesses, etc.) |
| Pool registration | Isolated transaction — no withdrawals, mint, Plutus extras, governance fields |
| Outputs | Legacy tuple format when no multi-assets; post-Alonzo map format encouraged |
| Auxiliary data | HW signs hash only; Catalyst voting registration uses tuple format with empty scripts array |

## Signing modes

Ledger and Trezor validate transactions against a **signing mode** chosen by the software wallet:

1. **Stake pool registration** — minimal tx, registration cert only
2. **Ordinary** — credentials as key derivation paths
3. **Multisig** — script hashes; CIP-1854 keys only
4. **Plutus** — allows script data hash and Plutus-related fields; fewer restrictions, more user-visible detail

## Device capability gaps (as of CIP-21)

| Device | Notable missing features |
|--------|--------------------------|
| Trezor | DRep/CC keys and certs, voting procedures, treasury/donation fields, pool cold keys, operational certs, operator pool registration |
| Ledger Nano S | Operational certs, native script hash derivation, pool registration/retirement |
| Ledger Nano S Plus / X / Stax | CIP-21 "allowed" features expected to work |

Conway-era governance features (DRep certs, votes, treasury/donation tx elements) remain a **Trezor gap** — relevant as on-chain governance adoption grows.

## Maintenance tooling

| Tool | Maintainer | Role |
|------|------------|------|
| cardano-hw-interop-library | [[entities/vacuumlabs|VacuumLabs]] | Validate/transform txs to HW-compatible format |
| cardano-hw-cli | VacuumLabs | CLI wrapper using interop library |

Wallets such as **[[entities/eternl|Eternl]]** depend on maintained HW stacks for Ledger, Trezor, OneKey, Keystone, and Bluetooth mobile flows.

## Related

- [[sources/cip-21-hardware-wallet-interoperability]]
- [[sources/withdraw-hardware-wallet-maintenance-2026]]
- [[proposals/hardware-wallet-maintenance-2026]]
- [[entities/vacuumlabs]]
- [[entities/eternl]]
- [[concepts/treasury-escrow-oversight]]

## Open questions

- Which vendor holds the 2026 maintenance contract (not named in on-chain metadata; tooling history points to VacuumLabs)?
- How quickly do HW apps absorb new Conway governance fields (DRep, treasury/donation) given Trezor's documented gaps?
- Should DReps treat HW maintenance as infrastructure baseline (like node compatibility) or scrutinize as recurring vendor spend?
