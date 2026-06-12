# Overview

**Agenda:** Keep Cardano viable for generations to come.

This wiki is the compounding knowledge base for [$computerman's DRep platform](../ReadMe.md). It sits between immutable raw sources and published vote context.

## What lives here

- **Entities** — IOG/IOR, Harmonic Labs, Intersect, proposers, committees
- **Concepts** — Cardano Vision, post-quantum readiness, Ouroboros/Leios, Pebble/TypeScript tooling, treasury delivery models
- **Sources** — Summaries of proposals and reference material in `raw/`
- **Proposals** — Cross-linked governance actions and voting patterns
- **Analysis** — Comparisons and syntheses filed from wiki-query sessions

## Current focus (May 2026)

The core ingested governance source is **Cardano Vision 2026** from IO Research: a ₳32.9M treasury ask continuing the five-year research program approved in 2025. The program organizes work into seven packages under three themes—**post-quantum security**, **scalable architecture**, and **human-centred design**—with an explicit IOR → ARC → CBU pipeline to improve research-to-deployment conversion.

Published DRep vote context records **YES** on this action ([vote 53](../vote_context/markdown/53_IOR.md)), aligned with earlier emphasis on post-quantum R&D in [2025 roadmap feedback](../vote_context/markdown/7a_roadmap.md). Vote rationale text in that file is still sparse; the wiki proposal page tracks open gaps (e.g. Chronos not named in the 2026 draft).

The wiki now also tracks external post-quantum warning sources. [[sources/brace-for-impact-ecdlp-challenges]] proposes a reproducible [[concepts/ecdlp-challenge-ladder]] for [[concepts/quantum-cryptanalysis]]. [[sources/securing-elliptic-curve-cryptocurrencies]] reports lower secp256k1 attack resource estimates, introduces [[concepts/blockchain-quantum-attack-modes]], and explicitly flags Cardano staking and voting keys as at-rest exposure surfaces. Together they strengthen the governance case for completing primitive assessment, Ouroboros security analysis, and migration planning before public quantum demonstrations reach high-risk rungs.

A second current treasury source is [[sources/pebble-ecosystem-maintenance-typescript-core-cardano]], the [[entities/harmonic-labs]] proposal for [[concepts/pebble]] and [[concepts/cardano-typescript-tooling]]. It asks for 4.6M ADA over 12 months, combining a production-ready TypeScript-shaped smart-contract language with hard-fork maintenance for libraries used by Mesh, Lucid Evolution, Midgard, and related downstream tooling. The local vote context for this action is still a placeholder, so the wiki records no DRep position yet.

A third major 2026 treasury source is [[sources/tweag-core-cardano-infrastructure-2026-2028]]: [[entities/tweag]] requests **₳39.8M** over 2026–2028 for 17 work packages focused on **[[concepts/peras|Peras]] mainnet deployment**, [[concepts/history-expiry|History Expiry]], [[concepts/hoarding-node|Hoarding Node]] observability, and testing scaffolding. The largest single line items are **Peras v2** (₳8.2M), **Plutus Script Re-Executor** (₳6.7M), and **Peras v1** (₳5.0M). Peras v1 success metrics include ≤5 min median settlement and no KillSwitch use in the first six epochs post-activation. See [[analysis/tweag-2026-2028-work-package-deliverables]] for the full budget and milestone map. This is the engineering complement to IOR's research program — where Cardano Vision funds analysis and validation, Tweag funds production delivery and operational tooling. Intersect administers both proposals via the same TRSC/PSSC model.

Published DRep vote context records **YES** on this action ([vote 56](../vote_context/markdown/56_tweag.md), [[sources/vote-56-tweag-core-cardano-infrastructure-2026-2028]]). The rationale engages common **NO** arguments — **two-year timeline** and **bundled 17-package structure** — and argues both can be appropriate for an integrated Peras activation pipeline; see [[concepts/treasury-proposal-bundling]] for the evolving delegate view on governance granularity vs line-item votes.

A fourth 2026 treasury source is [[sources/eternl-path-to-sustainability-2026-2027]]: [[entities/eternl]] / [[entities/tastenkunst]] requests **₳1,680,000** ($420k at $0.25/ADA) for 12 months of wallet operations while rolling out **Pro subscriptions** as a sustainability path. This uses a **[[concepts/treasury-payback-model|revenue payback]]** model (biannual surplus returns) rather than milestone escrow or Intersect TRSC administration — contrasting with Pebble's SundaeSwap escrow and Tweag's Intersect/CDH contract pattern. Eternl claims 10–18% of mainnet transactions and positions itself as the only wallet with comprehensive in-app governance tooling. No DRep vote context is recorded yet.

A governance-parameter source is [[sources/reduce-committeeminsize-7-to-5]]: [[entities/intersect]] (Civics + TSC, Parameter Committee PCP-005) proposes lowering **`committeeMinSize`** from **7** to **5** so the [[concepts/constitutional-committee|Constitutional Committee]] can keep operating if one or two members depart. The seven-member body currently equals the minimum, so a single resignation halts CC-dependent actions. The change is a resubmission after a prior collision with another parameter action; enactment depends temporally on a Plutus cost-model change for the van Rossem hard fork. Trade-off: easier blocking at effective size 5 (2/3 threshold) vs catastrophic governance halt. Intersect elections still target 7 seats. DRep vote context is a placeholder ([vote 60](../vote_context/markdown/60_committeeMinSize.md)).

## Voting workflow (human)

1. Create vote context in `vote_context/markdown/` (summary + conclusion + links)
2. Cast vote on-chain; publish JSON-LD metadata to IPFS
3. Ingest the vote context and related raw material into this wiki to compound knowledge

## DRep identity

- **DRep ID:** `drep1yfpgzfymq6tt9c684e7vzata8r5pl4w84fmrjqeztdqw0sgpzw3nt`
- **Handle:** $computerman / William Doyle
