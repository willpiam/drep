# Peras

**Peras** is an Ouroboros overlay protocol that reduces settlement latency — targeting roughly **~2 minute finality** (overwhelming probability under standard assumptions) vs **~12 minutes** under standard Praos today, with a formal success metric of **≤5 minutes median settlement** under non-degraded conditions and ≤25% adversarial stake. It is described alongside [[concepts/leios|Leios]] as one of two critical protocol upgrades for Cardano's next growth phase.

## Research vs engineering

| Track | Actor | Role |
|-------|-------|------|
| Research & validation | [[entities/io-research|IO Research]] ([[proposals/cardano-vision-2026]]) | MEV/mempool analysis, adversarial modelling, Peras–Leios interaction, deployment readiness studies |
| Engineering delivery | [[entities/tweag|Tweag]] ([[proposals/tweag-core-cardano-infrastructure-2026-2028]]) | Peras v1/v2 mainnet deployment, KillSwitch, production cryptography, conformance testing |

IOR targets **2026 deployment readiness**; production hard-fork work is explicitly out of IOR scope. Tweag's 2026–2028 proposal is the primary treasury-funded **mainnet delivery** path ingested in this wiki.

## Tweag delivery scope (2026–2028)

Per [[sources/tweag-core-cardano-infrastructure-2026-2028]]:

- **Peras v1 (₳4.95M):** Historical certificates for secure bootstrapping; production cryptography (BLS placeholder until CBU/ARK research finalizes); **KillSwitch** for coordinated disable/re-enable; on-chain tunable parameters; `cardano-cli` certificate tooling; milestones T1.1–T1.5 through preprod and HFC readiness
- **Peras v2 (₳8.24M):** Pre-agreement (pre-vote / Byzantine agreement / vote) to avoid cooldown when adversary &lt;25% stake; faster cooldown recovery; N2N, memory/CPU, and committee-selection optimizations informed by mainnet metrics
- Staggered delivery aligned with Hard Fork Combinator windows; v2 begins in parallel with v1 finalization
- Supported by CTC conformance testing, mutation testing, adversarial fork simulation, and [[concepts/hoarding-node|Hoarding Node]] observability

**Success metrics (PDF):** ≤30% storage increase vs Praos under same conditions; no KillSwitch activation in first **6 epochs** (~30 days) post-activation. Mainnet HFC activation is explicitly outside vendor control.

Tweag commits to **ready-for-activation** deliverables (merged code, releases, runbooks, benchmarks, governance-action packages) while reporting ecosystem activation (HFC timing, CIP progression) separately.

See [[analysis/tweag-2026-2028-work-package-deliverables]] for per-milestone acceptance criteria.

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
