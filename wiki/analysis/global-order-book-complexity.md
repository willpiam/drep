# Global Order Book / DeFi Kernel — points of complexity

**From query:** 2026-07-14  
**Question:** What are the points of complexity with this proposal?

## Answer

Complexity is not mainly budget size (₳3.33M is mid-small). It is **bundled scope**, **hard product classes**, **adoption friction for incumbents**, and **soft accountability** on security and people.

### 1. Conceptual bundling — four jobs in one vote

| Piece | What it is | Complexity |
|-------|------------|------------|
| WP1 Registry / standard | Public good (defikernel.org) | Low–medium delivery; success depends on *others* adopting |
| WP2 Spot Leverage Order Book | New DeFi product | High — collateral, borrow, liquidation, eUTxO composition |
| WP3 American Options MM | New DeFi product | High — pricing, exercise, LP risk, pool extensions |
| WP4 Tx-builder SDK | Developer tooling | Medium — only valuable if WPs 1–3 (and externals) stick |

A YES funds **ecosystem standard + two high-risk apps + SDK** together. Hard to weight “yes to registry, no to leverage/options” inside one action ([[proposals/global-order-book-defi-kernel]]).

### 2. Product complexity (WP2 / WP3)

- **Leveraged spot** is not a vanilla order book: must coordinate collateral, debt, swaps, risk params, settlement/liquidation ([[sources/global-order-book-connect-cardano-defi]]).
- **American options** extend concentrated-pool logic with strike/expiry/premium/exercise and LP risk accounting — among the harder on-chain surfaces on Cardano.
- Security bar is only “review **or** audit” before mainnet; prior Anastasia audits of *Danogo* do not cover these new contracts ([[proposals/global-order-book-defi-kernel#security-trust-surface]]).

### 3. Adoption complexity — the standard’s real cost

Kernel-compatible means **permissionless (no required batcher) + public schemas + on-chain discoverability**. Registry PR is easy; making Minswap-style batcher/AMM dApps compatible is often a **redesign**, not a plugin ([[concepts/defi-kernel#what-it-takes-for-an-existing-dapp-to-integrate]]).

Open DRep questions (also in vote notes): how much work for incumbents? Will gained volume justify that cost?

### 4. Ecosystem / narrative complexity

- “Intents” language overlaps broader intent architectures and IOR Vision research, but this proposal is **registry + apps + SDK**, not a solver market ([[concepts/defi-kernel#relation-to-intents]]).
- Brands split: **Dano Finance / Danogo** + **fallen-icarus**; CIP authors empty; team unnamed ([[entities/dano-finance]]).
- Registry already lists some contracts; treasury ask accelerates tooling/protocols, not inventing the idea from zero — evaluation is “fund acceleration vs already-community work.”

### 5. Accountability / KPI complexity

- Admin is Minswap (1%), not Intersect TRSC/PSSC escrow pattern.
- Volume KPIs ($1M / 30d within 90 days of mainnet) can be gamed by incentives unless retention clauses bite (options has a post-incentive retention note; order book less so).
- Fee return is only **5% of protocol fees for 12 months** — modest treasury recapture relative to ask and risk.

### Complexity map (quick)

```text
Low     Medium              High
─────────────────────────────────
WP1     WP4 SDK             WP2 leverage book
listing                     WP3 American options
docs                        Incumbent redesign for 3 rules
                            Security of new contracts
                            Adoption economics for other dApps
```

## Sources

- [[proposals/global-order-book-defi-kernel]]
- [[concepts/defi-kernel]]
- [[sources/global-order-book-connect-cardano-defi]]
- [[entities/dano-finance]]
