# Real-World Payments

**Real-world payments** on Cardano means infrastructure for everyday spending, merchant acceptance, and fiat-connected financial activity — bridging onchain balances to banking rails, stablecoins, and spend interfaces (cards, POS, remittance) rather than DeFi-only flows.

## Position

Cardano's strategy framework identifies **Payments** as a high-value vertical under **Pillar 2** (adoption and utility). The ecosystem has strong DeFi and dApp foundations but historically lacked integrated payment rails at scale.

[[proposals/wirex-real-world-payments]] is the primary ingested treasury ask targeting this gap: **₳3,961,538** for [[entities/wirex|Wirex]] to deliver open-source onchain payments infrastructure plus **Visa card issuance** linked to onchain balances.

## Layered ecosystem context

| Layer | Example | Role |
|-------|---------|------|
| Stablecoin rails | [[concepts/cardano-critical-integrations|CCI]] / USDCx | Attestor infrastructure, licensed stablecoin on Cardano |
| L2 throughput | [[concepts/hydra|Hydra]] | Sub-second finality, micropayments, agent commerce |
| Signing/access | [[concepts/hardware-wallet-interoperability|CIP-21]] / HW maintenance | Secure transaction signing for wallets and devices |
| Merchant spend | [[proposals/wirex-real-world-payments|Wirex]] | Visa cards, banking connectivity, settlement smart contracts |

These layers are complementary: stablecoins provide denomination, L2 can reduce settlement cost for high-frequency flows, HW tooling secures signing, and Wirex-style infrastructure connects balances to merchant acceptance.

## Wirex proposal deliverables (ingested)

- Smart contract settlement, account abstraction, batched transactions, settlement logic
- Wallet and API ecosystem layer (open source, public good)
- Visa card issuance backed by onchain balances
- Banking-rail and stablecoin-system connectivity
- Self-custody wallet native integration

## Open questions

- Which stablecoin denominations will Wirex cards support on Cardano — ADA, USDCx, or Wirex-issued balances?
- How do open-source contract deliverables interact with Wirex's proprietary regulated card-issuing stack?
- What transaction-volume and user-adoption KPIs will milestones use?
- How does treasury-funded payments infrastructure relate to commercial Wirex products already serving 7M+ users off Cardano?

## Related

- [[proposals/wirex-real-world-payments]]
- [[entities/wirex]]
- [[sources/withdraw-wirex-real-world-payments]]
- [[concepts/cardano-critical-integrations]]
- [[concepts/hydra]]
- [[concepts/hardware-wallet-interoperability]]
- [[concepts/cardano-vision]]
