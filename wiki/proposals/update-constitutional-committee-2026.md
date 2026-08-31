# Update Constitutional Committee 2026

**Type:** Update Committee (`update_committee`)  
**Proposer:** [[entities/intersect|Intersect]]  
**Source:** [[sources/update-constitutional-committee-2026]]

Intersect endorses the **2026 Constitutional Committee election** and updates the four seats expiring at **Epoch 653**. Elected members serve **146 epochs** (~two years), expiring at **Epoch 799**, matching current [[concepts/committee-max-term-length|`committeeMaxTermLength`]]. Quorum remains **2/3**. The remaining three members (terms expire Epoch 726) are unchanged.

## On-chain details

| Item | Value |
|------|-------|
| Action type | `update_committee` |
| Deposit | ₳100,000 |
| Transaction ID | `4dab331457b61b824bbc6ba4b9d9be4750e25c0b5dd42207aeb63c7431a6b704` |
| Gov action index | 0 |
| Signature threshold | 2/3 (unchanged) |
| [Explorer](https://explorer.cardano.org/governance-action/4dab331457b61b824bbc6ba4b9d9be4750e25c0b5dd42207aeb63c7431a6b70400) | Cardano Foundation governance explorer |

## Motivation

The [[concepts/constitutional-committee|Constitutional Committee]] must be renewed as terms expire so membership stays at or above [[concepts/committee-min-size|`committeeMinSize`]]. This action seats the four candidates elected through Intersect's public process (Constitution Article III, Section 3 (2)): registration, DRep voting, independent audit, published results.

## Incoming members (expire Epoch 799)

| Member | Credential | CIP-129 Bech32 | Term |
|--------|------------|----------------|-----:|
| [[entities/marek-mahut\|Marek Mahut]] | pubkey `0af99047bc90e0d9073467548a19a85089b766e73eb807748a2ad361` | `cc_cold1zg90nyz8hjgwpkg8x3n4fzse4pggndmxuultspm53g4dxcgjkqykp` | 146 |
| [[entities/philip-disarro\|Phil_uplc]] | pubkey `13493790d9b03483a1e1e684ea4faf1ee48a58f402574e7f2246f4d4` | `cc_cold1zgf5jdusmxcrfqapu8ngf6j04u0wfzjc7sp9wnnlyfr0f4q68as9w` | 146 |
| [[entities/leandros-bsp\|Leandros BSP]] | script `7c34e0240b84029e0932f5e8d81af42a63f55de6da31f16e19b1f5b4` | `cc_cold1zd7rfcpypwzq98sfxt673kq67s4x8a2aumdrrutwrxcltdq9jkwn2` | 146 |
| [[entities/cardano-curia\|Cardano Curia]] | script `16feefc225e06f75a3c917f4aa50acffde7631ea0355721f2ac12542` | `cc_cold1zvt0am7zyhsx7adreytlf2js4nlaua33agp42usl9tqj2ssazjmn9` | 146 |

## Members removed on-chain

`members_to_remove` lists **three** credentials. Re-elected Phil_uplc and Cardano Curia keep the same cold credentials and are **re-appointed** (not removed) with the new expiration.

| Member | Credential | CIP-129 Bech32 | Prior expiration |
|--------|------------|----------------|-----------------:|
| Cardano Japan Council | script `9cc3f387623f45dae6a68b7096b0c2e403d8601a82dc40221ead41e2` | `cc_cold1zwwv8uu8vgl5tkhx569hp94sctjq8krqr2pdcspzr6k5rcsxw2az4` | 653 |
| KtorZ | pubkey `dc0d6ef49590eb6880a50a00adde17596e6d76f7159572fa1ff85f2a` | `cc_cold1ztwq6mh5jkgwk6yq559qptw7zavkumtk7u2e2uh6rlu972slkt0rz` | 653 |
| Cardano Atlantic Council | script `349e55f83e9af24813e6cb368df6a80d38951b2a334dfcdf26815558` | `cc_cold1zv6fu40c86d0yjqnum9ndr0k4qxn39gm9ge5mlxly6q42kqmjmzyj` | 653 |

Atlantic Council is described as a **retired** member whose term would otherwise expire at 653; the action still removes that credential.

## Unchanged members (expire Epoch 726)

Eastern Cardano Council, Tingvard, and Ace Alliance are not in this action.

**Committee after enactment:** Marek Mahut, Cardano Curia, Philip DiSarro, Leandros BSP, Eastern Cardano Council, Tingvard, Ace Alliance.

## Election results (stake-weighted)

DReps could approve up to four candidates. Seats go to the top four by **voting power (ada)**, not DRep ballot count.

| # | Candidate | Voting power (ada) | DRep votes | Outcome |
|---|-----------|-------------------:|-----------:|---------|
| 1 | [[entities/philip-disarro\|Philip DiSarro]] | 1,979,047,586.427 | 24 | Elected (re-election) |
| 2 | [[entities/leandros-bsp\|Leandros BSP]] | 1,964,850,507.458 | 23 | Elected |
| 3 | [[entities/marek-mahut\|Marek Mahut]] | 1,370,113,895.267 | 28 | Elected |
| 4 | [[entities/cardano-curia\|Cardano Curia]] | 1,288,633,576.302 | 27 | Elected (re-election) |
| 5 | Asia Africa Cardano Coalition | 1,142,561,765.138 | 16 | Not seated |
| 6 | Bosco Ribeiro | 197,409,335.579 | 10 | Not seated |
| 7 | Gbiri Oluwaseun | 121,192,048.252 | 3 | Not seated |
| 8 | NexTrium Global Innovations Ltd | 34,298,868.077 | 4 | Not seated |
| 9 | Ian Njuguna | 1,324,683.789 | 2 | Not seated |
| 10 | Meek Owen | 0 | 0 | Not seated |

Marek Mahut received the **most DRep ballots** (28) but ranked third by stake; Cardano Curia similarly outpolled Leandros BSP in DRep count while ranking fourth by power.

### Election process

Designed by the Constitutional Committee election working group under the [[entities/civics-committee|Civics Committee]]: constitutional compliance, open candidate registration for any ada owner, on-chain-verifiable results.

| Phase | Dates |
|-------|-------|
| Candidate registration | 8 May 2026 – 21 June 2026 |
| DRep voting | 28 June 2026 21:45 UTC – 23 July 2026 21:45 UTC |
| Voting-power snapshot | 23 July 2026 21:45 UTC |
| Independent audit (DQuadrant) | 23–26 July 2026 |
| Audited results published | 26 July 2026 12:00 UTC |

Ballot: [Intersect Ekklesia](https://intersect.ekklesia.vote/ballots/6a3ff13334b52f591a6b4f3d/proposals/6a3ff13334b52f591a6b4f3e).

## Enactment timing (ledger constraint)

An Update Committee action stores each member's **expiration epoch as a fixed value**. Actual term length = expiration − enactment epoch, and that length must be **≤ `committeeMaxTermLength` (146)**.

Setting expiration to 799 (maximum term) means the action **cannot enact before Epoch 653**. Enacting earlier would start the term sooner while still ending at 799 — a longer term, which the ledger rejects. With a 6-epoch action lifetime, ratification occurs in the **final epoch** regardless of how fast voting thresholds are met. DReps, SPOs, and the CC should still vote on a normal schedule.

Re-election does **not** stack prior service: `committeeMaxTermLength` caps each term from enactment, not cumulative tenure. Phil_uplc and Cardano Curia receive a fresh 146-epoch term starting where the current one ends.

## DRep position

No published vote context for this action yet.

## Open questions

- Does forced last-epoch enactment create operational risk if thresholds are missed until late in the lifetime?
- How should DReps weigh stake-weighted ranking vs DRep-count ranking when they diverge (Mahut/Curia vs DiSarro/Leandros)?
- Interaction with [[proposals/committee-min-size-7-to-5]]: if `committeeMinSize` is still 7 at Epoch 653 and this action fails, four expirations plus the Atlantic Council removal path would drop membership below the floor.

## Related

- [[concepts/constitutional-committee]]
- [[concepts/committee-max-term-length]]
- [[concepts/committee-min-size]]
- [[proposals/committee-min-size-7-to-5]]
- [[entities/intersect]]
- [[entities/civics-committee]]
