# Checklist — Pricing Intelligence

## Start gate

- [ ] Product specification and variant are explicit.
- [ ] Manufacturer/origin or scenario is explicit.
- [ ] Buyer/destination or segment is explicit.
- [ ] Quantity and order unit are explicit.
- [ ] Product, manufacturer and buyer reports are accepted.
- [ ] GTIP/HS candidate exists or is explicitly UNKNOWN.
- [ ] Intended commercial routes are defined.
- [ ] Non-equivalent specifications are not being compared.

## Evidence states

- [ ] Every price and rate is VERIFIED, ESTIMATED or UNKNOWN.
- [ ] VERIFIED values have dated attributable sources.
- [ ] ESTIMATED values show formula, source, date, range and confidence.
- [ ] UNKNOWN values have commercial impact and next verification.
- [ ] No value was invented.
- [ ] Original values are preserved.

## Price normalization

- [ ] Product specification is aligned.
- [ ] Unit and quantity are aligned.
- [ ] MOQ and price breaks are considered.
- [ ] Certifications, accessories, warranty and service are aligned.
- [ ] Currency and FX date are explicit.
- [ ] Quote date and validity are explicit.
- [ ] Incoterm, origin and destination are explicit.
- [ ] Payment and lead-time differences are explicit.
- [ ] Non-comparable observations are rejected.

## Landed cost and customs

- [ ] Supplier cost is sourced.
- [ ] Packaging and origin charges are included or UNKNOWN.
- [ ] Freight basis and route are explicit.
- [ ] Insurance is included or UNKNOWN.
- [ ] GTIP/HS confidence is stated.
- [ ] Duty and import measures use authoritative current sources.
- [ ] Brokerage, terminal and inland costs are included.
- [ ] Banking, financing and FX costs are considered.
- [ ] Warranty/certification allowance is considered.
- [ ] Recoverable VAT is separated from economic cost.
- [ ] VAT cash-flow impact is modeled.
- [ ] Professional-verification needs are flagged.

## Market and order economics

- [ ] Turkey market price basis is clear.
- [ ] Distributor price basis is clear.
- [ ] Competitor price basis is clear.
- [ ] Asking and achieved prices are distinguished.
- [ ] Typical project value is verified/estimated/unknown.
- [ ] Typical repeat-order value is verified/estimated/unknown.
- [ ] Commission opportunity is explicit.
- [ ] Gross and net margins are not confused.
- [ ] Operating costs are itemized.
- [ ] First and repeat-order economics are separated.

## Commercial models

- [ ] Representation Model is analyzed.
- [ ] Commission Model is analyzed.
- [ ] Back-to-back Trading is analyzed.
- [ ] Exclusive Distribution is analyzed.
- [ ] Hybrid Model is analyzed.
- [ ] Revenue mechanism is defined for each.
- [ ] Capital and cash timing are defined for each.
- [ ] Risk and speed are defined for each.
- [ ] Revenue is not double-counted.
- [ ] Recommended model is evidence-based.

## Cash, capital and risk

- [ ] Payment terms are modeled.
- [ ] Supplier prepayment is modeled.
- [ ] Buyer receivable timing is modeled.
- [ ] Inventory requirement is scored.
- [ ] Working-capital requirement is calculated or UNKNOWN.
- [ ] Cash Flow Risk is explicit.
- [ ] Currency exposure and FX source/date are explicit.
- [ ] Price volatility is assessed.
- [ ] Warranty, return and delay exposure are assessed.

## Scenarios and scoring

- [ ] Base, downside and upside cases exist.
- [ ] Supplier price sensitivity is tested.
- [ ] Selling price/commission sensitivity is tested.
- [ ] FX and freight sensitivity are tested.
- [ ] Duty, quantity and payment timing are tested.
- [ ] Break-even values are shown.
- [ ] Profitability is scored 0–100.
- [ ] Scalability is scored 0–100.
- [ ] Capital Requirement is scored 0–100, high = heavy.
- [ ] Capital Efficiency is calculated correctly.
- [ ] Cash Flow Strength is scored 0–100.
- [ ] Speed to Revenue is scored 0–100.
- [ ] Risk is scored 0–100, high = severe.
- [ ] Inverse Risk is calculated correctly.
- [ ] Weights total 100%.
- [ ] Atlas Score arithmetic is verified.
- [ ] Evidence Quality is separate.

## GO gate

- [ ] Atlas Score ≥ 75.
- [ ] Profitability ≥ 65.
- [ ] Cash Flow Strength ≥ 60.
- [ ] Risk ≤ 40.
- [ ] Evidence Quality ≥ 70.
- [ ] At least one model is viable.
- [ ] Base-case net contribution is positive.
- [ ] Downside exposure is controlled.
- [ ] No decision-critical assumption is hidden.
- [ ] Required controls are practical.

If any box fails, GO is prohibited.

## Outputs

- [ ] Report uses the next `intelligence/pricing/RXXX.md`.
- [ ] Report ends with the five mandatory sections in order.
- [ ] `database/pricing.csv` matches the report.
- [ ] `workspace/active_project.md` matches status and model.
- [ ] Only Pricing Intelligence dashboard values were updated.
- [ ] Stable IDs, original observations and source history are preserved.
- [ ] Report ID and verification date appear in updated surfaces.
- [ ] No quote, purchase, inventory or commitment was authorized.

## Integrity

- [ ] No prices, costs, rates, duties, quantities or margins were invented.
- [ ] Every estimate is explained and reproducible.
- [ ] Every UNKNOWN identifies the next verification.
- [ ] Tax, customs and legal limitations are explicit.

