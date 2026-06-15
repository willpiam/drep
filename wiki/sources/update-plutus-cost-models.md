# Update Plutus Cost Models

**Raw:** [../raw/Update-Plutus-Cost-Models.json](../raw/Update-Plutus-Cost-Models.json)  
**Ingested:** 2026-06-15

## Summary

[[entities/intersect|Intersect]]'s [[entities/parameter-committee|Parameter Committee]] proposes a **parameter change** updating on-chain **[[concepts/plutus-cost-models|Plutus cost models]]** for V1, V2, and V3. The action prepares Cardano for the **[[concepts/van-rossem-hard-fork|van Rossem hard fork]]** (Protocol Version 11) by setting costs for new Plutus primitives, backporting V3-only builtins to V1/V2, and re-benchmarking selected existing primitives.

**Timing split:** changes to **existing** primitive costs take effect immediately on enactment; **new** primitives remain unusable until Protocol Version 11 activates (not in Protocol Version 10).

Parameter Committee recommended the change **2026-03-05** and **2026-03-19**; [[entities/technical-steering-committee|TSC]] confirmed **2026-05-13**. Equivalent updates were enacted on SanchoNet (March 2026), Preview (April 2026), and Preprod (May 2026).

Deposit **₳100,000**. On-chain gov action: `gov_action1eqhnsdyf3exhp5mqt7sdjtl7xy69wqg8tvg854psns2jt72cra3qqrcnr8r`.

## Key points

- **Three objectives:** (1) cost models for new primitives post–van Rossem; (2) cross-version consistency — V3 builtins available in V1/V2; (3) updated costs for existing primitives from benchmarking.
- **New primitives** (five CIPs): modular exponentiation (`expModInteger`, CIP-109); `dropList` (CIP-132); BLS12-381 multi-scalar mul (CIP-133); array builtins `indexArray`, `lengthOfArray`, `listToArray` (CIP-138); Mary-era value ops `insertCoin`, `lookupCoin`, `unionValue`, `valueContains`, `valueData`, `unValueData`, `scaleValue` (CIP-153).
- **Existing primitive updates:** `equalsByteString` CPU cost in V1/V2/V3; `divideInteger`, `modInteger`, `quotientInteger`, `remainderInteger` CPU cost in **V3 only**.
- **Guardrails:** PCM-01 (benchmarked on reference architecture), PCM-02 (update when primitives added), PCM-03 (no negative values) — all satisfied; not checkable by automated guardrails script.
- **Security / performance:** no specific security concerns raised; benchmarking data from IOE Plutus Core team on reference machine.
- **Downstream dependency:** [[proposals/committee-min-size-7-to-5]] ratification depends **temporally** on enactment of this action (no technical interaction).

## Wiki updates

- Created [[proposals/update-plutus-cost-models]]
- Created [[concepts/plutus-cost-models]]
- Created [[concepts/van-rossem-hard-fork]]
- Updated [[entities/parameter-committee]]
- Updated [[entities/technical-steering-committee]]
- Updated [[entities/intersect]]
- Updated [[proposals/committee-min-size-7-to-5]]
- Updated [[overview]]
