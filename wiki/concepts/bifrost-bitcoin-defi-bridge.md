# Bifrost Bitcoin DeFi Bridge

**Bifrost** is a proposed Bitcoin-Cardano bridge model designed to bring BTC liquidity onto Cardano as a native asset (**fBTC**) using threshold custody tied to Cardano SPO participation.

## Position

From [[sources/bifrost-unlocking-bitcoin-defi-on-cardano-road-to-mainnet-phase-1-of-2]], Bifrost is framed as Cardano's strategic BTC-liquidity rail: move from testnet to audited private mainnet in Phase 1, then public rollout and operations in Phase 2.

The proposal argues Cardano's eUTxO model, native assets, fee predictability, and SPO decentralization make it suitable for security-oriented Bitcoin DeFi, but only if a trusted BTC access path exists.

## Architecture claims (proposal framing)

| Component | Role |
|----------|------|
| Watchtowers | Permissionless observers posting Bitcoin headers/confirmations to Cardano |
| Threshold custody | SPO-weighted co-signing for BTC release from Taproot custody scripts |
| Federated mode | Operational fallback if SPO coordination fails |
| fBTC | 1:1 represented native Cardano asset for DeFi composability |
| Atomic-swap fast lane | Optional faster entry path with premium fee |
| SDK / white-label | Embeddable bridge access for wallets and dApps |

## Security and economics framing

- Security emphasis: external audits, formal verification, pentest, bug bounty, and staged private-mainnet exposure before public launch.
- Economic framing: no separate bridge token, fees in fBTC, reserve waterfall, intended future Treasury surplus share, SPO incentive share.
- Governance framing: long-term independent stewardship structure targeted before Phase 2.

## Comparative narrative used

The source compares Bifrost with multisig, threshold-ECDSA bridges, and BitVM-style designs. Its core claim is that FROST/Taproot-style threshold signing can keep on-chain Bitcoin transaction cost low while supporting a large SPO-derived signer set.

## Related proposals

- [[proposals/bifrost-road-to-mainnet-phase-1]]
- [[proposals/io-hydra]] (complementary Cardano scalability stack)
- [[proposals/cardano-critical-integrations-v2]] (other ecosystem infrastructure/funding trade-offs)

## Open questions

- What objective security thresholds define "ready for public Phase 2"?
- How are signer-participation assumptions stress-tested under adversarial conditions?
- What is the practical risk profile of federated fallback vs SPO-threshold mode?
- How much BTC custody concentration emerges in practice once delegation weighting is applied?
