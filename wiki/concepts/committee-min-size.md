# committeeMinSize

**`committeeMinSize`** is an on-chain protocol parameter defining the **minimum** number of registered [[concepts/constitutional-committee|Constitutional Committee]] members required for the committee to function. If active membership falls **below** this value, governance actions needing Constitutional Committee approval become **ineligible for ratification** — including parameter changes, constitution updates, treasury withdrawals, and hard forks.

## Current and proposed values

| Setting | Value | Notes |
|---------|------:|-------|
| Current (mainnet) | 7 | Equals current elected CC size → no operational buffer |
| Proposed ([[proposals/committee-min-size-7-to-5]]) | 5 | Intersect resubmission via PCP-005; Civics + TSC approved |

The parameter sets a **floor**, not the target elected size. Intersect's CC election process is intended to maintain **7 seats** even if `committeeMinSize` is lowered.

## Operational impact

When membership equals `committeeMinSize`, a single resignation or term expiration can halt governance until seats are refilled. Lowering the minimum creates headroom (e.g. 7 members with min 5 tolerates two departures).

## Voting threshold interaction

Constitutional Committee approval typically uses a **2/3** threshold among active members. Smaller committees change how many votes are needed to pass or block:

| Active members | Yes votes to pass (2/3) | No votes to block |
|:--------------:|:-----------------------:|:-----------------:|
| 7 | 5 | 3 |
| 6 | 4 | 3 |
| 5 | 4 | 2 |

At five members, one inactive member plus one dissenter can prevent ratification — a trade-off against governance halts from undersized membership.

## Constitutional guardrails

From the Cardano Constitution parameter guardrails (cited in [[proposals/committee-min-size-7-to-5]]):

- **CMS-01:** must not be negative
- **CMS-02:** must not be lower than **3**
- **CMS-03:** must not exceed **10**

Setting to **5** satisfies all three.

## Related

- [[concepts/constitutional-committee]]
- [[proposals/committee-min-size-7-to-5]]
- [[entities/parameter-committee]]
- [[sources/reduce-committeeminsize-7-to-5]]
