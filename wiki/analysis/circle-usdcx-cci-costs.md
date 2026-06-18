# Circle USDCx — CCI Cost Disclosure and Year 2 Fees

**From query:** 2026-06-18  
**Question:** How much of CCI V2 goes to Circle? What are we buying? What if we don't pay? Was this disclosed in V1? Are we being squeezed?

## Answer

**No public Circle-specific figure exists** for CCI V2 (or V2 Year 2 maintenance overall). Circle's share sits inside the bundled **₳20.7M integration & maintenance** line together with LayerZero, Pyth, Dune, and **Fireblocks Year 1**. Partner NDAs block per-vendor splits.

### What we are buying from Circle (per proposal text)

Two cost layers, both in the V2 maintenance bucket:

1. **Contracted fees to Circle** — annual license, platform, service, and attestation fees under existing V1 commercial agreements ("Year 2" of a multi-year structure).
2. **Cardano-side ops** (not necessarily all paid to Circle) — attestor infrastructure and operations, monitoring, contract-administrator oversight.

USDCx is not a one-time software drop: native USDC on a non-EVM chain requires ongoing **attestor operations** so mint/burn/attestation stays aligned with Circle's issuance framework.

### V1 context (Circle was already the biggest line)

Intersect's May 2026 status report states:

- Circle was the **largest single allocation under CCI V1** (ordering: Circle > LayerZero > Pyth > Dune).
- V1 covered a **multi-year licensing and platform fee structure** plus attestor/ops work to go live.
- V1 contracting **"locked … launch and Year 1 obligations"** — Year 2 was part of the commercial structure, not an ad-hoc add-on after launch.

So USDCx going live did **not** mean Year 1+ fees were fully prepaid forever inside ₳70M; Year 1 was funded from V1, Year 2 is what V2 requests.

### What happens if fees are not paid?

The proposal does not spell out a Circle-specific shutdown clause. General claims:

- V1 operating agreements **expire or need renewal** within the V2 window.
- Without funded maintenance, **"usability … deteriorates"** — attestor ops, monitoring, and contract-admin oversight lapse.
- Practical risk: degraded or halted **mint/burn/attestation pipeline** and loss of institutional confidence — not necessarily instant on-chain erasure of existing USDCx, but the integration stops being reliably operable.

Exact legal/technical consequences depend on confidential contract terms.

### Was this disclosed in prior withdrawals?

**Yes, but not with Circle amounts or a Year 2 price tag.**

| Document | What it said |
|----------|----------------|
| CCI V1 treasury withdrawal (Dec 2025) | Integration costs include **"licensing fees, maintenance costs"**; funding supports **"multi-year commercial terms where required"**; integrations may receive **"additional approved maintenance payments during the program period"** |
| CCI V1 treasury withdrawal | **"We anticipate … additional funding in future governance cycles"** after demonstrating value |
| Budget info action (Nov 2025) | Breakdown would be **limited in granularity** due to partner confidentiality |
| Intersect status report (May 2026) | **"Multi-year obligations"**; maintenance is a **current obligation**, not discretionary |

V1 did **not** publish "Circle Year 2 = ₳X." V2 is the first on-chain ask that names **"CCI V1 Contracted Year 2 Licensing/Platform fees"** explicitly.

### Are we being squeezed by Circle?

**Not provable from public materials.** What we can say:

- Year 2 fees are framed as **pre-contracted** in V1 negotiations, not a post-launch surprise tariff from Circle alone.
- Circle's market position as regulated USDC issuer gives them leverage in any chain deal; that is structural, not unique to this vote.
- The sharper voter surprise is likely **Pentad bundling and cadence** (₳70M enacted Dec 2025 → ₳23M ask ~6 months later, with Fireblocks added) plus **zero vendor line-item transparency**, not a disclosed Circle price hike.
- Whether ₳23M total (all vendors + Fireblocks) is fair cannot be audited without the confidential splits.

## Sources

- [[sources/cardano-critical-integrations-v2]]
- [[proposals/cardano-critical-integrations-v2]]
- [[proposals/cardano-critical-integrations-v1]]
- [[analysis/cci-v2-budget-breakdown]]
- [Intersect CCI status update report](https://intersectmbo.org/news/cardano-critical-integrations-program-status-update-report) (May 2026)
- CCI V1 treasury withdrawal: `ipfs://bafkreicbxui5lbdrgcpjwhlti3rqkxfnd3vveiinkcu2zak5bny435w4yq`
