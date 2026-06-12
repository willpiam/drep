# Reduce the committeeMinSize parameter from 7 to 5

**Raw:** [../raw/Reduce-the-committeeMinSize-parameter-from-7-to-5.json](../raw/Reduce-the-committeeMinSize-parameter-from-7-to-5.json)  
**Ingested:** 2026-06-12

## Summary

[[entities/intersect|Intersect]] (on behalf of the [[entities/civics-committee|Civics Committee]] and [[entities/technical-steering-committee|Technical Steering Committee]], with [[entities/parameter-committee|Parameter Committee]] recommendation) proposes a **parameter change** lowering **`committeeMinSize`** from **7** to **5**. The change introduces an operational buffer between the on-chain minimum and the current seven-seat [[concepts/constitutional-committee|Constitutional Committee]] body, so one or two resignations or term expirations do not halt governance.

Ratification **depends temporally** on enactment of a separate Plutus cost-model parameter change ahead of the **van Rossem** hard fork (`gov_action1eqhnsdyf3exhp5mqt7sdjtl7xy69wqg8tvg854psns2jt72cra3qqrcnr8r`). There is no technical interaction between the two actions.

On-chain update sets `committee_min_size` to **5** (deposit **₳100,000**). Civics Committee approved submission **2026-03-13**; TSC approved **2026-06-03**. Off-chain discussion: [PCP-005 on Cardano Forum](https://forum.cardano.org/t/pcp-005-committeeminsize-yuta/151156) (Yuta, published **2025-11-11**).

This is a **resubmission** after a prior action (`gov_action1mldvtys6ketjg87wtpvr6cd77kdrd8sp62a8sxgadhmxx2s8lh7sqp2qedq`) was invalidated by a technical collision with another parameter change.

## Key points

- **Problem:** With 7 members and `committeeMinSize` = 7, dropping below 7 makes CC approval ineligible — parameter changes, constitution updates, treasury withdrawals, and hard forks stall.
- **Intent:** Buffer only; does **not** reduce elected seats. Intersect's CC election process still targets **7 seats**.
- **Trade-off:** At 5 members with 2/3 threshold, **4 yes** votes pass but only **2 no** votes can block (vs 3 at size 7). One inactive member plus one dissenter can veto.
- **Guardrails satisfied:** CMS-01 (non-negative), CMS-02 (≥ 3), CMS-03 (≤ 10). PARAM-06a (90-day off-chain lead time for critical governance parameters) cited via Nov 2025 forum post.
- **Reversible:** Reverting to 7 only bites if fewer than 7 CC members are registered at reversion time.

## Wiki updates

- Created [[proposals/committee-min-size-7-to-5]]
- Created [[concepts/committee-min-size]]
- Created [[concepts/constitutional-committee]]
- Created [[entities/civics-committee]]
- Created [[entities/technical-steering-committee]]
- Created [[entities/parameter-committee]]
- Updated [[entities/intersect]]
- Updated [[overview]]
