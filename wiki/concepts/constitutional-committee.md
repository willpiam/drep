# Constitutional Committee

The **Constitutional Committee (CC)** is one of three Cardano governance bodies (alongside DReps and SPOs). It ratifies certain governance actions — parameter changes, constitution updates, treasury withdrawals, and hard forks — subject to on-chain voting thresholds. Members are registered on-chain; their votes carry constitutional weight distinct from DRep and SPO ballots.

## Size and operability

Effective operation requires at least **`committeeMinSize`** registered members ([[concepts/committee-min-size]]). Below that floor, actions requiring CC approval cannot progress, which can stall much of on-chain governance.

As of the [[proposals/committee-min-size-7-to-5]] proposal context (2026), the CC comprises **7 members**, matching the then-current `committeeMinSize` of **7** — leaving no buffer for departures.

## Elections and administration

[[entities/intersect|Intersect]] facilitates periodic Constitutional Committee elections intended to maintain a **7-seat** committee. Lowering `committeeMinSize` does not, by itself, reduce the target elected size; it only changes the on-chain minimum for operability.

## Approval mechanics

For typical actions, CC ratification uses a **two-thirds** threshold among active members. The number of yes and no votes required scales with committee size; see [[concepts/committee-min-size#Voting threshold interaction]].

## Related governance actions

- [[proposals/committee-min-size-7-to-5]] — parameter change 7 → 5 (operational resilience)
- [[entities/civics-committee]] — Intersect body involved in CC governance process
- [[entities/intersect]]

## Open questions

- How should DReps weigh operational resilience (avoiding governance halts) vs easier blocking at smaller effective committee sizes?
- What is the right long-term relationship between elected CC size and `committeeMinSize`?
