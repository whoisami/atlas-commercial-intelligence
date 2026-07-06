# Commercial Signal Validation Checklist v2

## Signal capture

- [ ] Discovery began from a dated commercial/industrial signal or a monitored source—not a generic company list.
- [ ] Signal type, date, source class, entity and geography are recorded.
- [ ] Signal is VERIFIED, ESTIMATED or UNKNOWN.
- [ ] Freshness window and review/expiry date are explicit.
- [ ] Commercial meaning and an alternative explanation are documented.

## Entity resolution

- [ ] Legal/trading name, city and domain belong to the same entity.
- [ ] Factory/operating address is verified or `UNKNOWN`.
- [ ] Public business phone/contact is verified or `UNKNOWN`.
- [ ] Brand, subsidiary and namesake conflicts are resolved.
- [ ] Manufacturer, distributor, trader, procurement office or buyer role is correctly classified.

## Multi-source verification

- [ ] At least two independent source classes support every `PROCEED` entity.
- [ ] One decisive source proves manufacturing capability or buyer function.
- [ ] Company-controlled pages are counted as one source class.
- [ ] OSB, chamber, exporter, government, fair, machinery or certification evidence is checked where available.
- [ ] Contradictions are resolved or the record remains `WAIT`.
- [ ] Verification Score is factor-by-factor reproducible.

## Manufacturer readiness

- [ ] Relevant production process and OEM Metal Components fit are verified.
- [ ] Export activity is verified; otherwise export readiness is explicitly estimated/unknown.
- [ ] Certification claims distinguish company claim from registry verification.
- [ ] Capacity/investment signals distinguish announced, installed and commissioned states.
- [ ] Weak website presence is not used as automatic rejection.

## Buyer and partner discovery

- [ ] Buyer type is one of OEM, Tier supplier, procurement company, sourcing company, contract-manufacturing buyer, purchasing office, industrial distributor, trading company or supply-chain partner.
- [ ] Product/need evidence is recorded separately from outsourcing evidence.
- [ ] Supplier registration or portal evidence is not treated as an RFQ.
- [ ] Country and category-owner/access route are verified or `UNKNOWN`.

## Commercial scoring

- [ ] Manufacturing, Export Readiness, Accessibility, Signals, Revenue Potential, Execution Speed and Verification are each scored 0–100.
- [ ] Every component has evidence state and rationale.
- [ ] Atlas Opportunity Score recalculates using v2 weights.
- [ ] Accessibility explicitly considers company size, export maturity, channel network, decision access, public openness and partnership signals.
- [ ] Signal Score reflects recency, strength, corroboration and 90-day actionability.
- [ ] Unknown price/volume/commission data is not invented.

## Decision

- [ ] Every output contains all required v2 opportunity fields.
- [ ] `PROCEED` passes all numeric and hard gates.
- [ ] `WAIT` identifies the missing evidence, owner and review trigger.
- [ ] `DROP` records the disqualifier.
- [ ] First Recommended Action is specific, reversible and does not imply unauthorized contact.
- [ ] No company was contacted and no outreach email was created.
