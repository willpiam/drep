# DeFi Kernel

The **DeFi Kernel** is a proposed open, fee-free compatibility standard for Cardano DeFi: permissionless, composable, discoverable smart contracts that expose on-chain financial intents through consistent metadata and discovery mechanisms.

## Position

[[sources/global-order-book-connect-cardano-defi]] argues Cardano DeFi remains fragmented — DEXs, lending, options, and marketplaces operate as separate liquidity silos with inconsistent datum/redeemer exposure, discovery paths, and integration documentation.

The DeFi Kernel defines a common pattern where compatible contracts publish script hashes, datum/redeemer schemas, integration instructions, audit status, and discovery tags (e.g. **CIP-89 beacon tokens**, deterministic addresses, or other on-chain tagging). Users can write or fill orders without a privileged batcher.

Public registry: [defikernel.org](https://defikernel.org/) — maintained under [[proposals/global-order-book-defi-kernel]] WP1.

## Compatibility requirements (proposal framing)

- Registration does **not** require payment, licensing, certification fees, listing fees, revenue share, or mandatory smart-contract open-sourcing.
- Compatible protocols must publish enough metadata for wallets, bots, indexers, and dApps to interact safely.

## What it takes for an existing dApp to integrate

Per [defikernel.org](https://defikernel.org/) and the [registry README](https://github.com/DeFiKernel-Cardano/DeFi-Kernel-Registry-for-Cardano):

### 1. Conform to three on-chain properties (the real bar)

| Rule | Meaning for an existing dApp |
|------|------------------------------|
| **Permissionless** | Users must sign/submit fills themselves to a Cardano node — **no required batcher / privileged operator** standing between intent and settlement |
| **Composable** | Publish a full public **datum (and reusable integration) schema** so others can read intents and chain txs atomically |
| **Discoverable** | Orders/intents findable from the UTxO set alone (e.g. **CIP-89 beacons**, deterministic addresses, or equivalent on-chain tags) — not only via a private indexer |

If a dApp is batcher-gated or only discoverable through a closed API, listing alone is not enough — it needs a contract/UX redesign (or a parallel kernel-compatible surface).

### 2. Document and register (cheap relative to #1)

1. Fork [DeFi-Kernel-Registry-for-Cardano](https://github.com/DeFiKernel-Cardano/DeFi-Kernel-Registry-for-Cardano), copy `_template.md`.
2. Fill YAML (name, developer, category, **script hashes**, links) + markdown (`Description`, `Datum Schema`, `Integration Guide`, `Off-Chain Libraries`).
3. Open a PR. Stated checks: parseable file, hashes resolve on mainnet, three rules implemented — **no review committee / fee**.

### 3. Optional tooling (what this treasury ask adds)

WP4’s **Composable DeFi Transaction Builder SDK** is meant to lower integrator cost after registration (registry reader, schema parsing, tx helpers, adapters). Until that ships, integrators rely on each contract’s published guide + own off-chain libs.

**DRep framing:** registry onboarding is intentionally light; the hard cost for incumbent AMM/batcher dApps is meeting **permissionless + on-chain discoverability**, not filling out a form.

## Reference implementations (treasury-funded)

| Primitive | Description |
|-----------|-------------|
| Spot Leverage Order Book | Leveraged spot via orders coordinating collateral, borrowing, swaps, liquidation — not a vanilla spot book |
| American Options Market-Making Pools | Extended concentrated-pool model for pool-priced American options |
| Composable DeFi Transaction Builder SDK | Registry reader, schema parser, discovery helpers, tx construction |

## Relation to “intents”

**Overlaps in language and spirit, not the same product category as a full intent architecture.**

The proposal describes DeFi Kernel as exposing **on-chain financial intents** — users publish or fill orders without a privileged batcher, and protocols share discoverable schemas so others can compose with them. That is close to the general idea of intents: declare a financial wish on-chain and let others fulfill it.

It is **not** (as framed) a general-purpose intent/solver market like Anoma- or CowSwap-style systems where a user states an end state and competing solvers invent the execution path. The funded work is more concrete: a **compatibility registry + order-book/options reference apps + SDK**, so Cardano DeFi protocols can interoperate. IOR’s Cardano Vision research (Cavefish / intent solver market) is a separate, more research-oriented intents track.

| | DeFi Kernel (this proposal) | Broad “intents” architectures |
|--|-----------------------------|-------------------------------|
| Core ask | Shared standard + discoverability + two apps + SDK | Outcome declaration + solver competition |
| User act | Write/fill structured on-chain orders | Often “swap X→Y under constraints” |
| Coordination | Order books, beacons, schemas | Relayers/solvers/matchers |

## Related

- [[entities/dano-finance]]
- [[proposals/global-order-book-defi-kernel]]
- [[entities/minswap-labs]]
- [[concepts/cardano-vision]] (separate intents/solver research thread)
