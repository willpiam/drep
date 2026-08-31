# Constitutional Committee

The **Constitutional Committee (CC)** is one of three Cardano governance bodies (alongside DReps and SPOs). It ratifies certain governance actions — parameter changes, constitution updates, treasury withdrawals, and hard forks — subject to on-chain voting thresholds. Members are registered on-chain; their votes carry constitutional weight distinct from DRep and SPO ballots.

## Size and operability

Effective operation requires at least **`committeeMinSize`** registered members ([[concepts/committee-min-size]]). Below that floor, actions requiring CC approval cannot progress, which can stall much of on-chain governance.

As of the [[proposals/committee-min-size-7-to-5]] proposal context (2026), the CC comprises **7 members**, matching the then-current `committeeMinSize` of **7** — leaving no buffer for departures. [[proposals/update-constitutional-committee-2026]] renews four seats at Epoch 653 so the elected size stays 7.

## Elections and administration

[[entities/intersect|Intersect]] facilitates periodic Constitutional Committee elections intended to maintain a **7-seat** committee, under Constitution Article III, Section 3 (2). Lowering `committeeMinSize` does not, by itself, reduce the target elected size; it only changes the on-chain minimum for operability.

The **2026 election** (Civics Committee election working group; DRep stake-weighted votes, up to four approvals; DQuadrant audit) seated [[entities/marek-mahut|Marek Mahut]], [[entities/leandros-bsp|Leandros BSP]], and re-elected [[entities/philip-disarro|Philip DiSarro]] and [[entities/cardano-curia|Cardano Curia]] for terms ending Epoch 799. See [[proposals/update-constitutional-committee-2026]]. Individual terms are capped by [[concepts/committee-max-term-length|`committeeMaxTermLength`]] (146 epochs).

## Membership (2026 renewal)

Outgoing at Epoch 653: Cardano Japan Council, KtorZ, Cardano Atlantic Council (retired; still removed on-chain), plus the two re-elected incumbents' prior terms. Unchanged through Epoch 726: Eastern Cardano Council, Tingvard, Ace Alliance.

**After enactment of the 2026 update:** Marek Mahut, Cardano Curia, Philip DiSarro, Leandros BSP, Eastern Cardano Council, Tingvard, Ace Alliance.

Founding entities ([[entities/emurgo|EMURGO]], [[entities/input-output-group|IOG]], [[entities/cardano-foundation|Cardano Foundation]]) and Intersect held **appointed** seats on the Interim CC and **did not stand** for the 2025 elected committee. None of them is among 2026 candidates or the post-enactment roster. See [[analysis/founding-entities-constitutional-committee]].

## Approval mechanics

For typical actions, CC ratification uses a **two-thirds** threshold among active members. [[proposals/update-constitutional-committee-2026]] leaves quorum at **2/3**. The number of yes and no votes required scales with committee size; see [[concepts/committee-min-size#Voting threshold interaction]].

## Related governance actions

- [[proposals/update-constitutional-committee-2026]] — 2026 election seating; Epoch 653 → 799 terms
- [[proposals/committee-min-size-7-to-5]] — parameter change 7 → 5 (operational resilience)
- [[concepts/committee-max-term-length]]
- [[entities/civics-committee]] — Intersect body involved in CC governance process
- [[entities/intersect]]
- [[entities/emurgo]]
- [[entities/cardano-foundation]]
- [[analysis/founding-entities-constitutional-committee]]

## Open questions

- How should DReps weigh operational resilience (avoiding governance halts) vs easier blocking at smaller effective committee sizes?
- What is the right long-term relationship between elected CC size and `committeeMinSize`?
- How should stake-weighted election ranking vs DRep-count ranking be interpreted when they diverge?
