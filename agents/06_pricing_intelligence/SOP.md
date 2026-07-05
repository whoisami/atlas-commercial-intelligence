# SOP — Pricing Intelligence

## 1. Define the opportunity unit

1. Read accepted Product, Manufacturer, Buyer and relevant Due Diligence reports.
2. Define product specification, variant, certification, unit and order scenario.
3. Define manufacturer, origin, buyer segment, destination and commercial route.
4. Define evidence cutoff, currencies and analysis date.
5. If specifications or quantities are not comparable, stop and assign WATCH.

## 2. Create the evidence register

For every input record:

- Value or range
- VERIFIED / ESTIMATED / UNKNOWN
- Specification
- Unit
- Quantity
- Currency
- Date
- Incoterm
- Source
- Validity
- Confidence
- Notes

Do not calculate before evidence states are assigned.

## 3. Collect manufacturer pricing and MOQ

1. Capture dated manufacturer quotes or official price evidence.
2. Prefer EXW for transparent comparison when available.
3. Record MOQ, price breaks, tooling, packaging and documentation costs.
4. Record payment terms and validity.
5. Separate list, indicative, negotiated and transaction prices.
6. If price is unavailable, write UNKNOWN; do not fabricate a benchmark.

## 4. Normalize price observations

1. Verify technical equivalence.
2. Align unit and quantity.
3. Adjust for included accessories, documentation, warranty and service.
4. Align currency using a cited dated FX rate.
5. Align Incoterm and destination.
6. Reject non-comparable observations.
7. Preserve original and normalized values.

## 5. Build freight and import assumptions

1. Define mode, route, dimensions, weight, volume and shipment frequency.
2. Use a verified freight quote or estimate from cited reference data.
3. Record insurance, origin, terminal, brokerage and inland charges.
4. Identify GTIP/HS candidate and confidence.
5. Verify customs duty and import measures from authoritative current sources.
6. Separate recoverable VAT from economic cost and model its cash-flow effect.
7. Flag assumptions requiring customs/tax professional verification.

## 6. Build the landed-cost bridge

Calculate each cost component explicitly. Show:

- Formula
- Currency
- FX rate/date
- Per-unit and per-order cost
- VERIFIED / ESTIMATED / UNKNOWN
- Base/downside/upside range

Reconcile the sum to Landed Economic Cost.

## 7. Collect Turkey price evidence

1. Capture Turkish market, distributor and competitor prices.
2. Identify whether price is list, asking, tender, quote or transaction evidence.
3. Match specification, quantity, service, tax and date.
4. Record seller/channel and source.
5. Do not infer achieved price from a public listing.
6. Triangulate where possible.

## 8. Model project and repeat-order economics

1. Define typical project and repeat-order scenarios.
2. Use verified values or transparent ranges.
3. Calculate revenue, gross contribution, operating cost and net contribution.
4. Model annual order frequency only when supported.
5. Separate first-order economics from repeat-order economics.
6. Include acquisition, travel, technical, translation, samples, warranty, banking and administration costs when relevant.

## 9. Analyze five commercial models

For each model:

1. Define revenue mechanism.
2. Identify contractual assumptions.
3. Calculate gross and net contribution.
4. Calculate capital and working-capital needs.
5. Model payment timing and cash conversion.
6. Model FX, inventory, warranty and credit exposure.
7. Estimate speed to first revenue.
8. Record verification gaps.
9. Assign viability status.

Do not assume exclusive distribution is superior.

## 10. Run scenarios and sensitivities

At minimum test:

- Supplier price
- Selling price
- Commission rate
- FX
- Freight
- Duty/customs treatment
- Quantity/MOQ
- Payment timing
- Delay
- Returns/warranty
- Operating cost

Identify break-even values and the assumptions most capable of reversing the decision.

## 11. Score financial viability

1. Score Profitability.
2. Score Scalability.
3. Score raw Capital Requirement.
4. Calculate Capital Efficiency.
5. Score Cash Flow Strength.
6. Score Speed to Revenue.
7. Score raw Risk.
8. Calculate Inverse Risk.
9. Calculate Atlas Score.
10. Score Evidence Quality separately.
11. Explain evidence, confidence and sensitivity.

## 12. Select the commercial model

Choose the model with the strongest combination of:

- Credible net contribution
- Low capital exposure
- Cash-flow control
- Speed
- Scalability
- Manufacturer/buyer fit
- Risk controls
- Evidence quality

A hybrid must describe sequence and boundaries precisely.

## 13. Apply decision rules

- GO only when every threshold passes and one model is robust.
- WATCH when a quote, tariff, freight, market price or payment term can close the gap.
- NO-GO when no realistic model produces acceptable risk-adjusted economics.

Do not average away a fatal cash or capital risk.

## 14. Write and synchronize outputs

1. Write the next `intelligence/pricing/RXXX.md`.
2. End with the five mandatory sections in order.
3. Update `database/pricing.csv` with evidence state, scenarios, economics and model recommendation.
4. Update `workspace/active_project.md` with financial status and next gate.
5. Update only Pricing Intelligence-owned values in `dashboard/CEO_DASHBOARD.md`.
6. Preserve stable IDs, original values, source history and unrelated content.
7. Cite report ID and verification date.
8. Route GO to Atlas CEO for controlled commercial validation.

## Escalation

Escalate customs classification, tax treatment, sanctions, controlled goods, legal terms, credit exposure, banking restrictions or financial assumptions requiring licensed advice. Do not make external contact without authorization.

## Completion definition

Work is complete when Atlas can reproduce the economics, see which values are verified versus estimated, understand downside cash exposure and choose a commercial model without relying on hidden assumptions.

