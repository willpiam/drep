# CIP-21: Transaction requirements for interoperability with hardware wallets

**Raw:** [../raw/Transaction requirements for interoperability with hardware wallets.md](../raw/Transaction%20requirements%20for%20interoperability%20with%20hardware%20wallets.md)  
**Source URL:** [cips.cardano.org/cip/CIP-21](https://cips.cardano.org/cip/CIP-21)  
**Ingested:** 2026-06-23  
**Published:** 2021-06-15

## Summary

**CIP-21** defines the transaction restrictions software wallets and tools must follow when building transactions signed by **hardware wallets (HW)**. HW devices (Ledger, Trezor) have limited memory and cannot process all node-valid transactions. They stream transaction data in chunks, compute a rolling hash, and return witness signatures — so clients must reconstruct the signed body using a **canonical, unambiguous CBOR serialization**.

The CIP covers canonical CBOR rules, transaction body limits (unsupported entries, integer sizes, element counts), output formats (legacy vs post-Alonzo), multiasset and certificate restrictions, withdrawal rules, auxiliary data encoding, and **device-specific capability gaps**. Implementation tools include **[[entities/vacuumlabs|VacuumLabs]]**'s `cardano-hw-interop-library` and `cardano-hw-cli`.

## Key points

- **Canonical CBOR:** Minimal integers/lengths; sorted map keys; definite-length items; consistent optional tag-258 usage in Conway-era sets.
- **Unsupported body entries:** `update` (6), `proposal procedures` (20).
- **Limits:** int64/uint64 integers; max 65535 inputs, outputs, asset groups, tokens, certificates, etc.; single voter with single voting procedure.
- **Pool registration isolation:** Pool registration certs cannot combine with withdrawals, mint, datum outputs, script data hash, collateral, required signers, reference inputs, voting procedures, treasury, or donation fields.
- **Unsupported cert types:** genesis key delegation, MIR, stake/vote delegation combos (Conway-era combined certs).
- **Signing modes (Ledger/Trezor):** stake pool registration, ordinary (key paths), multisig (script hashes), Plutus (maximum flexibility, higher user exposure).
- **Trezor gaps:** no DRep/CC keys or certs, voting procedures, treasury/donation elements, pool cold keys, operational certs, operator-side pool registration.
- **Ledger Nano S gaps:** no operational certs, native script hash derivation, pool registration/retirement, full Byron address detail display.
- **Active status:** Interoperability generally achieved since Alonzo; recent ledger changes may impose temporary extra restrictions until HW apps catch up.

## Wiki updates

- Created [[sources/cip-21-hardware-wallet-interoperability]]
- Created [[concepts/hardware-wallet-interoperability]]
- Created [[entities/vacuumlabs]]
- Updated [[proposals/hardware-wallet-maintenance-2026]], [[entities/eternl]]
- Updated [[overview]], [[index]]
