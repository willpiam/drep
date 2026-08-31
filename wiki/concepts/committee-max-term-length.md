# committeeMaxTermLength

**`committeeMaxTermLength`** is an on-chain protocol parameter capping how long a [[concepts/constitutional-committee|Constitutional Committee]] member may serve **in a single term**, measured from the epoch the appointing Update Committee action is **enacted** to that member's **expiration epoch**. As of the [[proposals/update-constitutional-committee-2026|2026 CC update]], the value is **146 epochs** (about two years).

It does **not** cap cumulative or continuous service across terms. Re-election grants a fresh term measured from the new enactment.

## Interaction with Update Committee actions

An Update Committee governance action writes each new member's expiration as a **fixed epoch**, not a duration. Term length is then `expiration − enactment_epoch`. If that difference exceeds `committeeMaxTermLength`, the ledger **rejects** enactment.

Consequence for a max-length appointment: the action can only enact in the epoch where `expiration − enactment = 146` (or less). For expiration **799**, that epoch is **653**. Enacting earlier would *lengthen* the term (same end date, earlier start), which exceeds the cap.

[[proposals/update-constitutional-committee-2026]] states this is counterintuitive but does not change how or when DReps, SPOs, or the CC should vote. With a 6-epoch action lifetime, a 146-epoch term expiring at 799 ratifies in the **last** lifetime epoch even if thresholds are met sooner.

## Related

- [[concepts/constitutional-committee]]
- [[concepts/committee-min-size]]
- [[proposals/update-constitutional-committee-2026]]
- [[sources/update-constitutional-committee-2026]]
