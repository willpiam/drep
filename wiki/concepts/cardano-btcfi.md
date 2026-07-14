# Cardano BTCfi

**Cardano BTCfi** (Bitcoin decentralized finance on Cardano) is the ecosystem category of Bitcoin-backed financial primitives — reserves, structured exposure, yield, and composable BTC-linked assets — deployed natively on Cardano rather than only via wrapped tokens on other chains.

## Position

As of mid-2026 treasury proposals, Cardano has **bridge-oriented** BTC access ([[concepts/bifrost-bitcoin-defi-bridge|Bifrost]] → fBTC) but limited **production BTCfi infrastructure** — transparent reserve systems, structured products, dashboards, and integration standards at ecosystem scale.

[[sources/alchemy-sundial-charms-cardano-native-bitcoin-treasury-protocol]] frames this as a strategic gap: Bitcoin liquidity and structured exposure are consolidating on Ethereum, BNB, Solana, and off-chain capital markets (e.g. Strategy/MSTR, Strive SATA, on-chain Apyx/Saturn/Pendle-style products).

## Alchemy model (FIRE / ICE)

[[proposals/alchemy-cardano-native-bitcoin-treasury]] proposes a **shared BTC reserve** with two composable Cardano-native assets:

| Asset | Role |
|-------|------|
| **FIRE** (BTC+) | Volatility-absorbing residual claim; amplified BTC upside; first-loss on downside |
| **ICE** (BTC−) | USD-denominated lower-volatility BTC-backed exposure with growth potential |

Reserve ratio: (V × P) / L where V = BTC in vault, P = BTC/USD price, L = ICE liability USD. Target **5.0×** with safety zones constraining mint/redemption below 4× and pausing risky activity below 2×.

Analogous in spirit to DJED's senior/junior two-token model, adapted for Bitcoin-backed goals.

**Naming — “Bitcoin treasury protocol”:** Product language for a BTC-reserve structured system (FIRE/ICE), analogous to public-market BTC treasury preferreds / on-chain structured BTC exposure — **not** an extension of Cardano’s L1 governance treasury to multi-asset holdings. See [[analysis/alchemy-bitcoin-treasury-meaning]].

**Alchemy product vs transfer rail:** Alchemy's funded scope is reserve architecture + FIRE/ICE + reporting/liquidity — **not** a dedicated "bridge BTC to Cardano as fBTC" program like Bifrost. Bitcoin↔Cardano asset circulation for Alchemy is delegated to [[entities/charms|Charms]] (meta-protocol / beaming). That still has cross-chain failure modes the proposal labels bridge/oracle/accounting risk.

## Parallel BTC-on-Cardano paths

| Path | Proposal | Mechanism |
|------|----------|-----------|
| Bridge liquidity | [[proposals/bifrost-road-to-mainnet-phase-1]] | SPO threshold custody; fBTC native asset |
| Structured BTCfi layer | [[proposals/alchemy-cardano-native-bitcoin-treasury]] | Reserve architecture; FIRE/ICE; Charms issuance layer |

## Reserve asset path (Alchemy vs fBTC)

[[proposals/alchemy-cardano-native-bitcoin-treasury]] does **not** state that Alchemy will use Bifrost **fBTC**. The proposal describes vault reserve as **BTC** (`V` = BTC in the vault) and routes Cardano circulation through **[[entities/charms|Charms]]** meta-protocol issuance — Bitcoin-native logic circulating as Cardano-native FIRE/ICE. Risks listed are Charms-layer bridge/oracle/accounting, not a dependency on Bifrost Phase 1.

Wiki framing of Alchemy as *complementary* to Bifrost remains proposer/wiki synthesis (bridge liquidity vs structured products), not an integration claim. Whether Alchemy later accepts fBTC (or other bridged BTC) as reserve collateral is **unspecified**.

**If Bifrost succeeds:** Alchemy’s claimed add is structured FIRE/ICE exposure + reporting/bootstrap — not BTC access. Skeptical case: build that on fBTC with existing DeFi instead. See [[analysis/alchemy-vs-bifrost-value-add]].

**DRep judgment (2026-07-14):** Yes — a successful Bifrost **weakens** Alchemy’s treasury case. The “Cardano lacks Bitcoin infrastructure” urgency is largely absorbed by the bridge rail. What remains is a narrower ask (structured FIRE/ICE + bootstrap liquidity on a Charms path that may *not* use fBTC). That can still be valuable to some voters, but it is harder to justify as scarce public-good infrastructure versus a product that could be built competitively on fBTC.

## Open questions

- Whether Alchemy ever integrates fBTC or other bridged BTC as reserve or composable collateral (not specified in the ₳10M proposal).
- Regulatory treatment of structured BTC-backed exposure vs. bridge representations.
- Whether multiple BTCfi stacks fragment or complement liquidity depth.

## Related

- [[entities/sundial-protocol]]
- [[entities/charms]]
- [[concepts/bifrost-bitcoin-defi-bridge]]
- [[proposals/alchemy-cardano-native-bitcoin-treasury]]
- [[proposals/bifrost-road-to-mainnet-phase-1]]
