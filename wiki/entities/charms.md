# Charms

**Charms** is a Bitcoin meta-protocol layer providing live Bitcoin/Cardano compatibility infrastructure and the technical foundation for issuing Bitcoin-native assets that circulate as Cardano-native assets. Public Charms materials describe cross-chain movement as ZK **"beaming"** (no custodial wrapped-bridge model); Alchemy still lists Charms **bridge / oracle / asset-accounting** risk in its treasury rationale.

## Position

In [[sources/alchemy-sundial-charms-cardano-native-bitcoin-treasury-protocol]], Charms is the technical partner for **[[proposals/alchemy-cardano-native-bitcoin-treasury|Alchemy]]** — enabling FIRE and ICE to be issued with Bitcoin-native logic and integrated into Cardano wallets, DEXs, and DeFi tooling. Alchemy is **not** asking treasury funds to build a Bifrost-style BTC→fBTC bridge; Charms is the assumed Bitcoin↔Cardano asset path under that product.

**Funding scope:** The ₳10M ask is for **Alchemy** (Pool 1 liquidity + Pool 2 delivery/audit/GTM). It is not framed as a standalone Charms R&D grant. Charms appears as delivery partner; line items are Alchemy protocol infrastructure, engineering, audits, dashboards, legal, GTM — not “fund Charms core protocol.” Proposal bans personal compensation to Charms principals; a rollover clause redirects the Alchemy *development* portion to extra treasury liquidity if external investment already pays that work.

The Alchemy proposal acknowledges **protocol-layer risk** from Charms: bridge, oracle, or asset-accounting vulnerabilities could impair reserve health. Mitigations include independent security review, economic modeling, staged deployment, dashboard reporting, and pause rules.

## Related

- [[entities/sundial-protocol]]
- [[proposals/alchemy-cardano-native-bitcoin-treasury]]
- [[concepts/cardano-btcfi]]
- [[concepts/bifrost-bitcoin-defi-bridge]] — parallel BTC-on-Cardano approach (bridge vs. meta-protocol issuance)
