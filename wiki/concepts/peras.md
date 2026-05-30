# Peras

**Peras** is an Ouroboros overlay protocol that reduces settlement latency — targeting roughly **~2 minute finality** vs **~12 minutes** under standard Praos today. It is described alongside [[concepts/leios|Leios]] as one of two critical protocol upgrades for Cardano's next growth phase.

## Research vs engineering

| Track | Actor | Role |
|-------|-------|------|
| Research & validation | [[entities/io-research|IO Research]] ([[proposals/cardano-vision-2026]]) | MEV/mempool analysis, adversarial modelling, Peras–Leios interaction, deployment readiness studies |
| Engineering delivery | [[entities/tweag|Tweag]] ([[proposals/tweag-core-cardano-infrastructure-2026-2028]]) | Peras v1/v2 mainnet deployment, KillSwitch, production cryptography, conformance testing |

IOR targets **2026 deployment readiness**; production hard-fork work is explicitly out of IOR scope. Tweag's 2026–2028 proposal is the primary treasury-funded **mainnet delivery** path ingested in this wiki.

## Tweag delivery scope (2026–2028)

Per [[sources/tweag-core-cardano-infrastructure-2026-2028]]:

- **Peras v1:** Production cryptography, KillSwitch, mainnet readiness
- **Peras v2:** Pre-agreement algorithm, cooldown recovery, performance optimizations
- Staggered delivery aligned with Hard Fork Combinator windows; v2 begins in parallel with v1 finalization
- Supported by CTC conformance testing, mutation testing, adversarial fork simulation, and [[concepts/hoarding-node|Hoarding Node]] observability

Tweag commits to **ready-for-activation** deliverables (merged code, releases, runbooks, benchmarks, governance-action packages) while reporting ecosystem activation (HFC timing, CIP progression) separately.

## Related votes

No DRep vote context recorded yet for [[proposals/tweag-core-cardano-infrastructure-2026-2028]].

## Open questions

- Peras v1 vs v2 HFC sequencing and dependency on IO Consensus Initiative
- Interaction effects with Linear Leios throughput and [[concepts/history-expiry|History Expiry]] under high TPS
- Whether IOR research outputs and Tweag engineering milestones are synchronized

## Related

- [[concepts/ouroboros]]
- [[concepts/leios]]
- [[entities/tweag]], [[entities/io-research]]
- [[proposals/tweag-core-cardano-infrastructure-2026-2028]]
- [[proposals/cardano-vision-2026]]
