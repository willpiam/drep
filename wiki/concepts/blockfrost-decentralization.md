# Blockfrost Decentralization

**Blockfrost decentralization** is the effort to move Cardano's dominant hosted API from centralized IOG operation toward a network of community operators (**Icebreakers**) and ultimately community-governed not-for-profit stewardship.

## Position

[[entities/blockfrost|Blockfrost]] joined [[entities/input-output-group|IOG]] in 2024 explicitly to decentralize. The **Icebreakers** program recruits independent operators to run Blockfrost infrastructure; **100+ Icebreakers** had joined by the time of [[sources/blockfrost-transformation-to-not-for-profit]] (2026).

The proposal argues decentralization removes single points of failure in the access layer most applications depend on, while a treasury-funded transition period pays for DevOps and migration until an elected board assumes control.

## Icebreakers model

Icebreakers are decentralized Blockfrost operators — often including SPOs and infrastructure teams with experience running Blockfrost products. They extend the operator set beyond IOG-hosted endpoints and are cited as natural participants in a future **vendor-backed federation** where multiple parties jointly operate the public API.

## Not-for-profit transition (2026 proposal)

[[proposals/blockfrost-transformation-to-not-for-profit]] funds an 18-month path:

1. Establish or integrate with a not-for-profit legal entity (PRAGMA candidate)
2. Elect a five-seat community board (four infrastructure-entity seats + one community seat)
3. Cut over all public API traffic and transfer IP to the NFP
4. Consult on long-term sustainability — either NFP-operated paid tiers (profits to treasury) or federated vendor partners

The free tier remains the stated core public good (~90% of traffic). Commercial paths are deferred to post-transition board decisions.

## Tension with prior funding debate

An earlier Blockfrost treasury proposal was **not funded**. Community feedback highlighted hesitation about treasury support for what appeared to be a **commercial venture**. The 2026 redesign commits to full not-for-profit status and IP transfer, but still outlines future commercial revenue models under NFP or vendor governance — a point DReps may weigh when assessing recurring treasury dependence vs self-sustainability.

## Related infrastructure role

Blockfrost is not L1 consensus infrastructure, but the proposal claims **>50% of mainnet transactions** are submitted through it in most epochs — making the access layer operationally critical for transaction volume, developer onboarding, and protocol fee revenue KPIs.

## Open questions

- What technical split remains between IOG-hosted endpoints and Icebreaker nodes at Q1 2027 cutover?
- Do Icebreakers receive treasury subsidy, or only the central NFP operator budget?
- Can federated operators maintain 99% uptime SLA without centralized coordination?

## Related

- [[entities/blockfrost]]
- [[proposals/blockfrost-transformation-to-not-for-profit]]
- [[concepts/treasury-payback-model]]
- [[concepts/treasury-escrow-oversight]]
