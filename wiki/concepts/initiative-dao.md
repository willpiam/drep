# Initiative DAO

An **Initiative DAO** is a purpose-built, smart contract-governed funding body on Cardano where ecosystem participants — typically established builders and projects — coordinate treasury allocation through structured proposal review, debate, and on-chain voting. **[[entities/clarity|Clarity]]** provides the enabling platform ([clarity.vote](https://www.clarity.vote)).

## Position

Initiative DAOs sit between episodic Catalyst-style grants and large single-vendor treasury withdrawals. They offer:

- **Member-governed allocation** — voting members evaluate and fund requesting members
- **On-chain treasury execution** — multi-output treasury withdrawals once quorum is reached
- **Iterative governance** — governing documents, board election, temperature checks, merit review
- **Accountability overlays** — third-party assurance, public KPI reporting, repayment of unused funds

The canonical live example is the **[[entities/cardano-builder-dao|Cardano Builder DAO]]**, which distributed ₳11.1M across 34 proposals in two rounds (2025–2026).

## Contrast with Intersect TRSC

Many treasury withdrawals use **[[entities/intersect|Intersect]]** administration via Sundae Labs TRSC/PSSC contracts ([[concepts/treasury-escrow-oversight]]). Initiative DAOs can instead use **internal smart-contract governance** for sub-allocation while the parent treasury withdrawal may be administered by Intersect (2025 CB DAO) or an independent **dRep DAO council multisig** ([[proposals/cardano-builder-dao|2026 CB DAO continuation]]).

## Related

- [[entities/cardano-builder-dao]]
- [[entities/clarity]]
- [[concepts/ecosystem-kpi-funding]]
- [[concepts/treasury-escrow-oversight]]
- [[proposals/cardano-builder-dao]]

## Open questions

- How many Initiative DAOs beyond CB DAO are operational at scale?
- What standards should Initiative DAO KPI reporting meet for dRep oversight?
