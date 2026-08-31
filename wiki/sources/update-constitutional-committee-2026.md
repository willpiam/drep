# Update Constitutional Committee 2026

**Raw:** [../raw/Update-Constitutional-Committee-2026.json](../raw/Update-Constitutional-Committee-2026.json)  
**Ingested:** 2026-08-31

## Summary

[[entities/intersect|Intersect]] submits an **Update Committee** governance action that replaces the four [[concepts/constitutional-committee|Constitutional Committee]] seats expiring at **Epoch 653** with the candidates elected in the **2026 Constitutional Committee election**. Incoming terms expire at **Epoch 799** (146 epochs, the current [[concepts/committee-max-term-length|`committeeMaxTermLength`]] cap). Quorum stays **2/3**. Author witness: Intersect (ed25519). Deposit **₳100,000**.

The action endorses a public election under Constitution Article III, Section 3 (2): candidate registration, DRep stake-weighted voting (up to four approvals), independent audit by **DQuadrant**, and published audited results before on-chain submission. The four highest vote-power candidates are seated; two incumbents ([[entities/philip-disarro|Philip DiSarro]] / Phil_uplc and [[entities/cardano-curia|Cardano Curia]]) are re-elected onto fresh maximum-length terms.

Because expiration epochs are **fixed on-chain**, a max-length term can only be enacted in the action's **final lifetime epoch** (Epoch 653). Earlier enactment would make the term exceed 146 epochs and be rejected by the ledger. Vote timing is unaffected.

## Key points

- **Type:** `update_committee` (not a parameter change or treasury withdrawal).
- **Incoming (term 146, expire 799):** [[entities/marek-mahut|Marek Mahut]], [[entities/philip-disarro|Phil_uplc]], [[entities/leandros-bsp|Leandros BSP]], [[entities/cardano-curia|Cardano Curia]].
- **On-chain removes (3 credentials):** Cardano Japan Council, KtorZ, Cardano Atlantic Council (retired; term would otherwise expire 653). Re-elected credentials are **not** in `members_to_remove`; they are re-appointed with expiration 799.
- **Unchanged (expire 726):** Eastern Cardano Council, Tingvard, Ace Alliance.
- **Post-enactment roster (7):** Marek Mahut, Cardano Curia, Philip DiSarro, Leandros BSP, Eastern Cardano Council, Tingvard, Ace Alliance.
- **Election ranking (ada voting power):** Philip DiSarro 1.979B (24 DReps); Leandros BSP 1.965B (23); Marek Mahut 1.370B (28); Cardano Curia 1.289B (27). Next was Asia Africa Cardano Coalition at 1.143B (16 DReps) — not seated. Ranking is by **stake-weighted voting power**, not DRep count (Mahut had the most DRep ballots).
- **Timeline:** registration 8 May–21 June 2026; DRep voting 28 June–23 July 2026 (snapshot 23 July 21:45 UTC); DQuadrant audit 23–26 July; results published 26 July 2026 12:00 UTC.
- **Ledger quirk:** `committeeMaxTermLength` caps each **individual** term from enactment, not cumulative service. Re-election is a seamless renewal, not stacked time.

## On-chain

| Item | Value |
|------|-------|
| Tag | `update_committee` |
| Transaction ID | `4dab331457b61b824bbc6ba4b9d9be4750e25c0b5dd42207aeb63c7431a6b704` |
| Gov action index | 0 |
| Deposit | ₳100,000 |
| Reward account | `stake1uyvjdz9rxsfsmv44rtk75k2rqyqskrga96dgdfrqjvjjpwsefcjnp` |
| Signature threshold | 2/3 |
| [Explorer](https://explorer.cardano.org/governance-action/4dab331457b61b824bbc6ba4b9d9be4750e25c0b5dd42207aeb63c7431a6b70400) | Cardano Foundation governance explorer |

## References (from metadata)

- [Audited Election Results (XLSX)](ipfs://bafybeigc77zeko6rhfgc5nzp4q474m5d4i7vt522ykhdjypv5odqplvl7m)
- [Audited Files](ipfs://QmPMB1fTNMqaKcJkmMUr98EtUxtJ95p8uRxdDsiyFqTrTy)
- [Constitutional Committee Election 2026 (Ekklesia ballot)](https://intersect.ekklesia.vote/ballots/6a3ff13334b52f591a6b4f3d/proposals/6a3ff13334b52f591a6b4f3e)

## Wiki updates

- Created [[proposals/update-constitutional-committee-2026]]
- Created [[concepts/committee-max-term-length]]
- Created [[entities/philip-disarro]]
- Created [[entities/marek-mahut]]
- Created [[entities/leandros-bsp]]
- Created [[entities/cardano-curia]]
- Updated [[concepts/constitutional-committee]]
- Updated [[concepts/committee-min-size]]
- Updated [[entities/intersect]]
- Updated [[entities/civics-committee]]
- Updated [[proposals/committee-min-size-7-to-5]]
- Updated [[overview]]
