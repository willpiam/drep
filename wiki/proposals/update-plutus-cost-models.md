# Update Plutus Cost Models

**Type:** Parameter change (`parameter_change_action`)  
**Proposer:** [[entities/intersect|Intersect]] ([[entities/parameter-committee|Parameter Committee]] recommendation; [[entities/technical-steering-committee|TSC]] confirmation)  
**Source:** [[sources/update-plutus-cost-models]]

Intersect proposes updating on-chain **[[concepts/plutus-cost-models|Plutus cost models]]** for V1, V2, and V3 to support the **[[concepts/van-rossem-hard-fork|van Rossem hard fork]]** (Protocol Version 11), align builtin availability across Plutus language versions, and refresh costs for re-benchmarked existing primitives.

## On-chain details

| Item | Value |
|------|-------|
| Parameter update | `cost_models` — `plutus_v1`, `plutus_v2`, `plutus_v3` |
| Deposit | ₳100,000 |
| Transaction ID | `c21b00f90f18fce4003edf42b0b0d455126e01c946e80cc5341a9f9750caf795` |
| Gov action index | 0 |
| [Cardanoscan](https://cardanoscan.io/govAction/gov_action1eqhnsdyf3exhp5mqt7sdjtl7xy69wqg8tvg854psns2jt72cra3qqrcnr8r) | `gov_action1eqhnsdyf3exhp5mqt7sdjtl7xy69wqg8tvg854psns2jt72cra3qqrcnr8r` |

## Motivation

Three objectives:

1. **New primitives** — After Protocol Version 11, new Plutus builtins become available; cost models must be set before they can be used.
2. **Cross-version parity** — Primitives previously limited to Plutus V3 are enabled in V1 and V2 as well.
3. **Re-benchmarking** — CPU/memory costs for some existing primitives are updated from fresh benchmarking data.

## Enactment timing

| Change class | When effective |
|--------------|----------------|
| Existing primitive cost updates | **Immediately** on governance enactment |
| New primitive availability | Only after **Protocol Version 11** (van Rossem hard fork); **not** in Protocol Version 10 |

## New primitives (by CIP)

| CIP | Builtin(s) | Category |
|-----|------------|----------|
| [CIP-109](https://github.com/cardano-foundation/CIPs/tree/master/CIP-0109) | `expModInteger` | Modular exponentiation (cryptography) |
| [CIP-132](https://github.com/cardano-foundation/CIPs/tree/master/CIP-0132) | `dropList` | List manipulation |
| [CIP-133](https://github.com/cardano-foundation/CIPs/tree/master/CIP-0133) | `bls12_381_G1_multiScalarMul`, `bls12_381_G2_multiScalarMul` | BLS12-381 MSM (cryptography) |
| [CIP-138](https://github.com/cardano-foundation/CIPs/tree/master/CIP-0138) | `indexArray`, `lengthOfArray`, `listToArray` | Array operations |
| [CIP-153](https://github.com/cardano-foundation/CIPs/tree/master/CIP-0153) | `insertCoin`, `lookupCoin`, `unionValue`, `valueContains`, `valueData`, `unValueData`, `scaleValue` | Mary-era value manipulation |

Each new primitive has both CPU and memory unit cost models.

## Changes to existing primitives

| Primitive | Versions affected |
|-----------|-------------------|
| `equalsByteString` (CPU) | V1, V2, V3 |
| `divideInteger`, `modInteger`, `quotientInteger`, `remainderInteger` (CPU) | V3 only |

Full diffs vs current mainnet cost models are in the raw governance metadata ([IPFS diffchecker reference](ipfs://bafybeicefsednx6bwwghyhrf5zwy3a4zzgdnwf4pbqpidukveihdpfq56a)).

## Approvals and process

| Body | Action | Date |
|------|--------|------|
| [[entities/parameter-committee|Parameter Committee]] | Recommended | [2026-03-05](https://forum.cardano.org/t/mar-5-2026-parameter-committee-triweekly-meeting-notes/154363), [2026-03-19](https://forum.cardano.org/t/mar-19-2026-parameter-committee-triweekly-meeting-notes/154364) |
| [[entities/technical-steering-committee|TSC]] | Confirmed | [2026-05-13](https://committees.docs.intersectmbo.org/intersect-technical-steering-committee/meeting-minutes/2026-tsc-meeting-minutes/meeting-minutes-may-13-2026) |

### Testnet deployments (equivalent changes)

| Network | Gov action ID | When |
|---------|---------------|------|
| SanchoNet | `gov_action1kundw4x5cn2s85rmkccx7lkfgamgmy2w4p0kx87w4uh2ku52rwesqkj3cwm` | March 2026 |
| Preview | `gov_action1q9xr9etnglg3gazzzrsexj3qsnzaqpf2yvfpwrvnwk9l64n089tqqqg02j9` | April 2026 |
| Preprod | `gov_action18cd564yw8jcsj392ggtge8swd3pkxm5k6rdhlf3sv308z0rjy3gsqdgxfqp` | May 2026 |

## Constitutional guardrails

| Guardrail | Requirement | Status |
|-----------|-------------|--------|
| PCM-01 | Cost model values set by benchmarking on reference architecture | Satisfied — IOE Plutus Core team validated on reference machine |
| PCM-02 | Update cost model when new primitives or Plutus version added | Satisfied — new primitives for Protocol Version 11 |
| PCM-03 | Cost model values must not be negative | Satisfied |

None of these guardrails are checkable by the automated guardrails script.

## Downstream dependencies

**[[proposals/committee-min-size-7-to-5]]** ratification depends **temporally** on enactment of this action. No technical interaction between the parameter updates.

## DRep position

Published vote context: [vote 63](../../vote_context/markdown/63_updatePlutusCostModels.md) — **YES** on *Update Plutus Cost Models* (2026-06-15). Rationale text in vote context is still a placeholder; position recorded on-chain only.

## Open questions

- How should DApp developers plan upgrades given the split timing (existing costs immediate, new primitives post–hard fork)?
- Do cross-version builtin parity changes affect script validation assumptions for legacy V1/V2 contracts?
- What is the expected calendar for van Rossem (Protocol Version 11) relative to this parameter enactment?

## Related

- [[concepts/plutus-cost-models]]
- [[concepts/van-rossem-hard-fork]]
- [[entities/parameter-committee]]
- [[entities/technical-steering-committee]]
- [[entities/intersect]]
- [[proposals/committee-min-size-7-to-5]]
