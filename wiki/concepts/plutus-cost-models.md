# Plutus cost models

**Plutus cost models** are on-chain protocol parameters that assign **CPU and memory execution costs** to each Plutus Core builtin primitive. They determine how much a script pays in transaction fees relative to its computational work, and must be updated when new builtins are introduced or existing implementations are re-benchmarked.

Cardano maintains separate cost model arrays for **Plutus V1**, **V2**, and **V3** under the `cost_models` protocol parameter.

## Constitutional guardrails (PCM)

| ID | Rule |
|----|------|
| PCM-01 | Cost model values must be set by benchmarking on a reference architecture |
| PCM-02 | The cost model must be updated if new primitives are introduced or a new Plutus language version is added |
| PCM-03 | Cost model values should not be negative |

These guardrails are **not** checkable by the automated guardrails script; compliance relies on Parameter Committee and TSC review.

## Benchmarking process

Intersect's Parameter Committee coordinates cost model updates with the IOE Plutus Core developer team. Benchmarking uses a reference machine and implementation consistent with existing mainnet settings. Data and methodology:

- [Plutus cost-model data](https://github.com/IntersectMBO/plutus/tree/master/plutus-core/cost-model/data)
- [Cost model overview documentation](https://github.com/IntersectMBO/plutus/tree/master/doc/cost-model-overview)
- [CI benchmarking workflow](https://github.com/IntersectMBO/plutus/actions/workflows/cost-model-benchmark.yml)

## History

### 2026 — van Rossem preparation

[[proposals/update-plutus-cost-models]] (Intersect, 2026) updates V1/V2/V3 cost models ahead of the **[[concepts/van-rossem-hard-fork|van Rossem hard fork]]** (Protocol Version 11):

- Adds costs for new builtins from CIP-109, CIP-132, CIP-133, CIP-138, and CIP-153
- Backports V3-only builtins to V1 and V2 for cross-version consistency
- Re-benchmarks `equalsByteString` (all versions) and integer division primitives (V3)

Existing-primitive cost changes take effect on parameter enactment; new primitives become usable only after Protocol Version 11.

## Related

- [[concepts/van-rossem-hard-fork]]
- [[entities/parameter-committee]]
- [[proposals/update-plutus-cost-models]]
- [[concepts/pebble]] — compiles to UPLC; cost model changes affect script fee economics
- [[concepts/cardano-typescript-tooling]] — libraries must track cost model and Plutus version changes around hard forks
