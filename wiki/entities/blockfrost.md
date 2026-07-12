# Blockfrost

**Blockfrost** is Cardano's dominant hosted REST API for reading blockchain data and submitting transactions without operating a full node. Founded in 2020 by Five Binaries and acquired by [[entities/input-output-group|IOG]] in 2024 with a mandate to decentralize the service.

## Position

Blockfrost is described in [[sources/blockfrost-transformation-to-not-for-profit]] as the **lingua franca** of Cardano development. Per the Cardano Foundation State of the Developer Ecosystem survey, it is the **#1 hosted platform** developers use — growing from 39.3% (2022) to **71.5%** (2025). The service covers mainnet, preview, and preprod.

## Usage (proposer metrics, 2026)

| Metric | Value |
|--------|-------|
| Monthly unique visitors | ~781k |
| Monthly API requests | ~1.84B (~700 rps) |
| Monthly data served | ~7 TB |
| Free-tier traffic share | ~90% |
| Mainnet tx submission share | >50% of transactions in most epochs |

## Decentralization

Since 2024, Blockfrost has pursued decentralization through the **Icebreakers** program — decentralized operators running Blockfrost instances. **100+ Icebreakers** had joined as of proposal submission. See [[concepts/blockfrost-decentralization]].

## Treasury and governance transition (2026)

[[proposals/blockfrost-transformation-to-not-for-profit]] requests **₳9,832,979** over 18 months to transition Blockfrost into a **community-governed not-for-profit**: transfer IP (source, trademarks, domains), elect a five-seat board, maintain the free public API, and publish usage and budget transparency. IOG co-proposes with [[entities/intersect|Intersect]] witness; Intersect administers via TRSC/PSSC.

Prior treasury receipt for the Blockfrost workstream: **₳1,137,500** (88% of allocation per IOG appendix).

## Preliminary board (proposal)

- Beatrice Anihiri — Blockfrost
- Christina Gianelloni — BlinkLabs
- Federico Weill — TxPipe
- Jeni Davidson — SundaeLabs
- Francis Luz — Masumi / Begin Wallet

IOG holds a non-voting advisory seat during the first year.

## Ecosystem relationships

- Production user of [[concepts/hydra|Hydra]] (SPO payments) per [[proposals/io-hydra]]
- Critical dependency for wallets, dApps, and indexers building on Cardano — see [[concepts/cardano-typescript-tooling]]

## History

| Year | Event |
|------|-------|
| 2020 | Founded by Five Binaries |
| 2024 | Joined IOG; decentralization mandate |
| 2025–2026 | Prior treasury Blockfrost workstream (₳1.14M received); earlier NFP proposal not funded |
| 2026 | Resubmitted as fully not-for-profit transition ask (₳9.83M) |

## Open questions

- Can elected governance sustain free-tier quality once IOG advisory role ends?
- How do Icebreakers relate to the NFP's long-term vendor-federation model?
- What happens to commercial API customers during IP and entity transfer?

## Related

- [[proposals/blockfrost-transformation-to-not-for-profit]]
- [[concepts/blockfrost-decentralization]]
- [[entities/input-output-group]]
- [[concepts/cardano-typescript-tooling]]
