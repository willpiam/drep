# van Rossem hard fork

The **van Rossem hard fork** is a planned Cardano hard fork that upgrades the ledger to **Protocol Version 11**. It enables new Plutus Core builtins and related ledger features that cannot activate under Protocol Version 10.

## Relationship to Plutus cost models

[[proposals/update-plutus-cost-models]] sets on-chain cost models for new Plutus primitives **before** the hard fork, but the primitives themselves become **usable only after Protocol Version 11** activates. Changes to costs for **existing** primitives take effect immediately when the parameter change is enacted.

This split timing means developers may see updated fees for existing builtins while new builtins remain unavailable until the hard fork completes.

## Governance dependencies

**[[proposals/committee-min-size-7-to-5]]** — ratification of the `committeeMinSize` reduction depends **temporally** on enactment of the Plutus cost-model parameter change (`gov_action1eqhnsdyf3exhp5mqt7sdjtl7xy69wqg8tvg854psns2jt72cra3qqrcnr8r`). There is no technical interaction between the two parameter updates.

## New capabilities (cost-model proposal)

Primitives introduced via CIP-109 (modular exponentiation), CIP-132 (`dropList`), CIP-133 (BLS12-381 MSM), CIP-138 (array builtins), and CIP-153 (Mary-era value builtins). See [[proposals/update-plutus-cost-models]] for the full builtin list.

## Related

- [[concepts/plutus-cost-models]]
- [[proposals/update-plutus-cost-models]]
- [[proposals/committee-min-size-7-to-5]]
- [[concepts/cardano-typescript-tooling]] — ecosystem libraries must track protocol version upgrades
