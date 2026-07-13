# Global Order Book connect Cardano DeFi to increase transaction

**Raw:** [../raw/Global-Order-Book-connect-Cardano-DeFi-to-increase-transaction.json](../raw/Global-Order-Book-connect-Cardano-DeFi-to-increase-transaction.json)  
**Ingested:** 2026-07-13

## Summary

Treasury-withdrawal proposal by **[[entities/dano-finance|Dano Finance]]** requesting **₳3,333,000** (₳3,300,000 delivery + ₳33,000 / 1% administration fee) to accelerate the **[[concepts/defi-kernel|DeFi Kernel]]** — an open standard for permissionless, composable, discoverable on-chain financial intents and global order-book coordination on Cardano — plus two reference protocols and an integration SDK.

**[[entities/minswap-labs|Minswap Labs]]** serves as budget administrator. Four work packages: DeFi Kernel registry (defikernel.org), Spot Leverage Order Book, American Options Market-Making Pools, and Composable DeFi Transaction Builder SDK. Dano Finance claims ~$18M TVL and 10,000+ on-chain transactions as operating credibility.

## Key points

- **Problem:** Cardano DeFi lacks a shared coordination layer for contract discovery, datum/redeemer schemas, and composable execution across siloed protocols.
- **DeFi Kernel standard:** Fee-free compatibility standard; registration requires integration metadata (script hashes, schemas, CIP-89 beacons or deterministic addresses) — not payment or open-sourcing mandates.
- **WP2 Spot Leverage Order Book:** Leveraged spot trading via orders coordinating collateral, borrowing, swaps, and liquidation — distinct from vanilla spot order books.
- **WP3 American Options:** Pool-based American options market-making with extended concentrated-pool logic.
- **WP4 SDK:** Registry reader, metadata parser, discovery helpers, and transaction construction for wallets, bots, and indexers.
- **KPIs:** $1M rolling 30-day volume (order book and options) within 90 days of mainnet; SDK v1 with at least one external integration.
- **Fee return:** 5% of protocol fees from Treasury-funded contracts returned to Treasury for 12 months post-mainnet.
- **Accountability:** Milestone-based delivery; security review before mainnet; Minswap Labs admin; unused funds returned per administrator process.

## Wiki updates

- Created [[sources/global-order-book-connect-cardano-defi]]
- Created [[proposals/global-order-book-defi-kernel]]
- Created [[entities/dano-finance]], [[entities/minswap-labs]]
- Created [[concepts/defi-kernel]]
- Updated [[overview]], [[index]]
