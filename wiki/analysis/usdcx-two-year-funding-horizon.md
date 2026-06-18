# USDCx — Two-Year Funding Horizon (CCI)

**From query:** 2026-06-18  
**Question:** What else is required to secure USDCx for the next two years? Is CCI V2 everything in terms of money?

## Answer

**CCI V2 is not a two-year USDCx budget.** It funds **one** 12-month maintenance window (contracted **Year 2** for Circle and the other V1 integrations), bundled with LayerZero, Pyth, Dune, and Fireblocks Year 1. To keep USDCx operable for **two years from enactment**, the public record implies **V2 plus at least one further treasury action** (e.g. CCI V3 / Year 3 maintenance), unless commercial terms or funding models change.

### Funding timeline (USDCx ops only)

| Period | Source | What it covers |
|--------|--------|----------------|
| **Year 1** (post-launch) | **CCI V1** (₳70M, enacted Dec 2025) | Delivery, attestor bring-up, Circle license/platform fees and ops for Year 1 — Intersect report: V1 **"locked … launch and Year 1 obligations"** |
| **Year 2** (next 12 months) | **CCI V2** (₳23M, if enacted) | Circle Year 2 fees + attestor/monitoring/contract-admin ops — inside shared **₳20.7M** maintenance bucket (Circle amount confidential) |
| **Year 3** | **Not in V2** | No on-chain commitment; proposal frames fees as **recurring annual baseline**; V1 text anticipated **"additional funding in future governance cycles"** |

Circle's slice of V2 is **not separable** in the governance action — USDCx maintenance is voted as part of the full CCI V2 bundle.

### What V2 includes for USDCx (money)

Inside the bundled budget:

1. **Contracted Circle fees** — Year 2 license, platform, service, attestation (per existing V1 agreements).
2. **Cardano-side ops** — Attestor infrastructure and operations, monitoring, contract-administrator oversight.
3. **Shared enhancement reserve (₳1.15M max)** — Optional tooling (e.g. USDCx SDK) if Steering Committee approves drawdown; **returned to treasury if unused**.

V2 admin/audit (₳1.15M) is program-wide, not USDCx-specific.

### What V2 does **not** include (separate money if desired)

These are **explicitly excluded** from CCI V2 and would need other funding if the goal is broader "USDCx success" than keeping the integration live:

| Item | Why it matters |
|------|----------------|
| **Treasury liquidity programs** | USDCx can exist on-chain without deep DeFi liquidity |
| **Marketing / events** | Awareness and adoption |
| **Dapp grants** | Apps that consume USDCx |
| **USDT0 or other stablecoins** | Separate tier-1 integration actions |
| **LayerZero OFT token deployments** | Cross-chain USDC flows beyond base LayerZero infra |
| **Year 3+ Circle maintenance** | Next governance cycle |

Complementary CCI integrations (Pyth, LayerZero, Dune) help the **ecosystem around** USDCx but are maintenance-bundled in the same V2 ask, not optional add-ons for Circle alone.

### V1 leftovers?

Intersect's May 2026 report: unused V1 balances (e.g. Fireblocks line not completed, contingency) **return to the Cardano Treasury** — they do **not** extend USDCx into Year 3. Year 2 is what V2 is for.

### Steady-state run-rate (uncertain)

If annual maintenance is roughly stable, **two years of USDCx ops** might ballpark to **~2× the Circle share of one maintenance year** — but:

- Circle's share of ₳20.7M is **confidential**
- V2 also funds Fireblocks Year 1 and three other vendors in the same bucket
- V2 total (₳23M) is **not** a Circle-only figure; it cannot be read as "USDCx costs ₳23M/year"

### Bottom line

| Question | Answer |
|----------|--------|
| Does V2 secure USDCx for two years? | **No** — one year (Year 2). |
| Is V2 all the money USDCx will ever need? | **No** — recurring fees expected; Year 3+ needs future votes. |
| Is V2 all the money to keep USDCx *running* for one year? | **Largely yes** for integration ops, per proposal scope — plus any enhancement-reserve drawdowns for tooling. |
| Anything else for a thriving USDCx market? | **Yes, potentially** — liquidity, apps, marketing are out of scope and unfunded by V2. |

## Sources

- [[proposals/cardano-critical-integrations-v2]]
- [[proposals/cardano-critical-integrations-v1]]
- [[analysis/circle-usdcx-cci-costs]]
- [[analysis/cci-v2-budget-breakdown]]
- [[concepts/cardano-critical-integrations]]
- [Intersect CCI status update report](https://intersectmbo.org/news/cardano-critical-integrations-program-status-update-report)
