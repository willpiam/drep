# Ikigai stuck deposit — ledger accounting

**From query:** 2026-06-22  
**Question:** Where is the Ikigai 100k ADA deposit currently accounted for on the ledger?

## Answer

The **₳100,000** governance-action deposit is **no longer in the proposal deposit pot**. After the original Ikigai info action expired (~Oct 2024), the ledger attempted to refund the deposit to the specified return stake credential. Because that credential was **unregistered at expiry**, the refund could not be credited to the submitter's reward account. Under Conway ledger rules, such **unclaimed proposal deposits are transferred to the Cardano treasury** — commingled with all other treasury ADA, not held as a separate locked UTxO or deposit entry.

The submitter's return address (`stake1uys93fhep4lc2u6lu0q09kcxayxzthasded35c0x0w60ugc9s0cm5`) was only registered later (epoch 626, 2026); it currently holds ~₳7.6 in UTxO plus the ₳2 stake-key deposit — **not** the original ₳100k.

**Remediation in flight:** treasury withdrawal [gov_action1654yj97lf7guxsh27phtknq2tsc4dajp95fh7vrucaltjy0502csq7qtkhq](https://cardanoscan.io/govAction/gov_action1654yj97lf7guxsh27phtknq2tsc4dajp95fh7vrucaltjy0502csq7qtkhq) requests **₳103,000** (₳100k + ₳3k staking-reward compensation) to that same stake address. DRep vote context: [vote 59](../../vote_context/markdown/59_ikigai.md), [vote 25](../../vote_context/markdown/25_reimburse_ikigai.md).

## Ledger journey (timeline)

| Phase | Ledger bucket | Amount |
|-------|---------------|--------|
| Submission (epoch 510, Sep 18 2024) | Moved from submitter UTxO → **proposal deposit pot** (`deposits_proposal`) | +₳100k |
| While action live (epochs 510–516) | Held in **proposal deposit pot** | ₳100k locked |
| Expiry (~epoch 517/518, Oct 21 2024) | Removed from proposal deposit pot | −₳100k from `deposits_proposal` |
| Refund attempt | Return credential unregistered → **not** credited to reward account | — |
| Post-expiry accounting | **Treasury** (unclaimed deposit sweep) | +₳100k to treasury pot |

On-chain evidence: `deposits_proposal` was **₳200,000** (two active actions) in epochs 515–517 and dropped to **₳100,000** at epoch 518 when Ikigai expired — exactly one ₳100k deposit leaving the pot.

## Root cause

A **pre-fix node bug** allowed submitting a governance action with an **unregistered** stake key as the deposit-return address ([cardano-ledger#4605](https://github.com/IntersectMBO/cardano-ledger/issues/4605), fixed in [PR #4639](https://github.com/IntersectMBO/cardano-ledger/pull/4639), Oct 2024). Ledger designers noted that if the return address is registered **before the action expires**, the deposit is returned normally; Ikigai's return address remained unregistered until 2026.

## Key on-chain references

| Item | ID / address |
|------|----------------|
| Original Ikigai info action | `gov_action1t87n2vjnavthuggyarerafxx8c7n9mu4c7r96qlfp5uggsjdc8dsqymg588` (expired) |
| Submission tx | `59fd353253eb177e2104e8f23ea4c63e3d32ef95c7865d03e90d3884424dc1db` |
| Deposit-return stake | `stake1uys93fhep4lc2u6lu0q09kcxayxzthasded35c0x0w60ugc9s0cm5` |
| Reimbursement treasury withdrawal | `gov_action1654yj97lf7guxsh27phtknq2tsc4dajp95fh7vrucaltjy0502csq7qtkhq` (live, expires Jul 13 2026) |

## Sources

- [gov.tools — Reimburse Ikigai](https://gov.tools/governance_actions/d52a4917df4f91c342eaf06ebb4c0a5c3156f6412d137f307cc77eb911f47ab1)
- [cardanoscan — original Ikigai action](https://cardanoscan.io/govAction/gov_action1t87n2vjnavthuggyarerafxx8c7n9mu4c7r96qlfp5uggsjdc8dsqymg588)
- [vote_context/markdown/25_reimburse_ikigai.md](../../vote_context/markdown/25_reimburse_ikigai.md)
- [vote_context/markdown/59_ikigai.md](../../vote_context/markdown/59_ikigai.md)
- [cardano-ledger#4605](https://github.com/IntersectMBO/cardano-ledger/issues/4605) — deposit-loss scenarios and unregistered return accounts
- Koios `totals` / `account_info` / `tx_info` (queried 2026-06-22)

## Open questions

- Exact epoch boundary of the treasury sweep (inferred from `deposits_proposal` drop at epoch 518; not independently verified block-by-block).
- Whether any portion was briefly credited as orphaned rewards before treasury sweep (no reward history on the return stake address).
