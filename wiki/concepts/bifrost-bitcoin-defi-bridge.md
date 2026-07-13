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

## Security model

Bifrost's security model is **threshold custody of real BTC on Bitcoin**, with **Cardano-side mint/burn of fBTC** and **permissionless observation** of Bitcoin state. The proposal frames it as avoiding a company, foundation, or fixed small signer committee in favour of Cardano's existing SPO set.

### Actors and trust assumptions

| Actor | Role | Trust assumption (proposal framing) |
|-------|------|-------------------------------------|
| **Users** | Deposit BTC, claim fBTC, return fBTC, receive BTC | Self-custody of claim/withdrawal actions |
| **Watchtowers** | Observe Bitcoin and post confirmed headers to Cardano | Permissionless; anyone can run one |
| **SPOs** | Co-sign BTC releases via threshold signing | Majority of delegated stake must cooperate to move locked BTC |
| **Federated fallback** | Continuity path if SPO coordination fails | Separate operational fallback mode; trust profile not fully specified in Phase 1 metadata |

### Core flows

**Deposit (peg-in):**

1. User sends BTC to a **Taproot custody script** on Bitcoin.
2. A watchtower posts the confirmed deposit to Cardano.
3. User claims equivalent **fBTC** on Cardano in a self-service transaction (no operator approval).

**Withdrawal (peg-out):**

1. User returns fBTC on Cardano.
2. A **cryptographic threshold of SPOs** co-signs the Bitcoin release transaction.
3. BTC is sent to the user's Bitcoin address. Withdrawals can be partial.

**Fast lane (optional):** non-custodial **atomic swap** between a BTC holder entering Cardano and an fBTC holder providing instant liquidity; both sides cryptographically locked.

### Cryptographic custody design

- **FROST** (Flexible Round-Optimized Schnorr Threshold) produces a single Schnorr signature from many signers off-chain.
- On Bitcoin, the spend appears as a normal **Taproot** transaction — compact and not visibly exposing signer count.
- Custody is intended to scale to **400+ SPOs**, weighted by delegation, rather than a small fixed multisig set.
- Moving funds requires a threshold representing the **majority of delegated stake**.
- **Trade-off acknowledged:** off-chain signing rounds require signer liveness; stalled coordination stalls signing. Mitigations claimed: persistent SPO infrastructure + federated fallback.

### What is *not* the security model

- Not a custodial wrapped-BTC company holding keys.
- Not synthetic BTC price exposure — fBTC is 1:1 with BTC locked in the Bitcoin script.
- Not an ADA bridge — only BTC/fBTC movement between Bitcoin and Cardano.
- Not BitVM/optimistic fraud-proof style — Bifrost uses threshold signing, not 1-of-N challenge games.

### Assurance and rollout controls (Phase 1 emphasis)

The proposal treats security as both **design** and **process**:

- External audits: smart contracts, cryptographic protocol (Tapscript/FROST/Schnorr/DKG), off-chain components.
- Formal verification of critical paths.
- Penetration testing and bug bounty from private mainnet.
- Staged rollout: private mainnet with real BTC under controlled access and TVL cap before public Phase 2.
- Both custody modes (SPO threshold and federated fallback) must be demonstrated on mainnet before public launch.

### Residual risks (as stated in proposal)

| Risk | Residual exposure claimed |
|------|---------------------------|
| Smart-contract / crypto exploit | Low but non-zero; bounded early by TVL cap and bug bounty |
| Custody validation on private mainnet | Bounded exposure under controlled access before public scale |
| SPO coordination failure | Federated fallback; signing stalls if both paths fail |
| Federated fallback mode | Open question — different trust concentration than full SPO threshold |

## Security and economics framing

- Security emphasis: external audits, formal verification, pentest, bug bounty, and staged private-mainnet exposure before public launch.
- Economic framing: no separate bridge token, fees in fBTC, reserve waterfall, intended future Treasury surplus share, SPO incentive share.
- Governance framing: long-term independent stewardship structure targeted before Phase 2.

## Comparative narrative used

The source compares Bifrost with multisig, threshold-ECDSA bridges, and BitVM-style designs. Its core claim is that FROST/Taproot-style threshold signing can keep on-chain Bitcoin transaction cost low while supporting a large SPO-derived signer set.

## Related proposals

- [[proposals/bifrost-road-to-mainnet-phase-1]]
- [[proposals/alchemy-cardano-native-bitcoin-treasury]] — structured BTCfi (FIRE/ICE) vs. bridge liquidity
- [[concepts/cardano-btcfi]]
- [[proposals/io-hydra]] (complementary Cardano scalability stack)
- [[proposals/cardano-critical-integrations-v2]] (other ecosystem infrastructure/funding trade-offs)

## Open questions

- What objective security thresholds define "ready for public Phase 2"?
- How are signer-participation assumptions stress-tested under adversarial conditions?
- What is the practical risk profile of federated fallback vs SPO-threshold mode?
- How much BTC custody concentration emerges in practice once delegation weighting is applied?
