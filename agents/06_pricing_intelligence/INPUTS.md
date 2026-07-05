# Inputs — Pricing Intelligence

## Mandatory opportunity inputs

- Accepted `intelligence/products/RXXX.md`
- Accepted `intelligence/manufacturers/RXXX.md`
- Accepted `intelligence/buyers/RXXX.md`
- Manufacturer Due Diligence status when a named manufacturer is modeled
- Product specification and order unit
- Manufacturer and origin
- Buyer or buyer segment and destination
- Quantity/MOQ scenario
- GTIP/HS candidate
- Intended commercial models
- Evidence cutoff

If technical equivalence or order basis is missing, stop.

## Operating inputs

- `database/products.csv`
- `database/manufacturers.csv`
- `database/buyers.csv`
- `database/pricing.csv`
- `database/decisions.csv`
- `workspace/active_project.md`
- `workspace/current_sprint.md`
- `dashboard/CEO_DASHBOARD.md`
- Relevant `intelligence/competition/RXXX.md`
- Relevant `intelligence/learning/RXXX.md`

## Price and cost evidence

Use, when lawfully available:

- Manufacturer quotations
- Official price lists
- Buyer quotations or tenders
- Historical invoices and purchase orders
- Public distributor and competitor prices
- Freight quotations
- Carrier or logistics reference rates
- Insurance quotations
- Official GTIP/HS and tariff sources
- Customs, trade-remedy and import-control sources
- Central-bank or authoritative FX rates
- Bank and financing fee schedules
- Public market/tender results
- Internal operating-cost evidence
- Approved commission or representation proposals

## Mandatory fields

Obtain or mark UNKNOWN:

- Manufacturer price and basis
- MOQ and price breaks
- Incoterm
- Currency, date and validity
- Freight assumptions
- GTIP/HS confidence
- Duty and import charges
- VAT treatment
- Market/distributor/competitor prices
- Project and repeat-order value
- Commission opportunity
- Operating costs
- Payment terms
- Price volatility
- Currency exposure
- Inventory and working capital
- Commercial-model assumptions

## Evidence-state rules

Every monetary and rate input must be one of:

- VERIFIED
- ESTIMATED
- UNKNOWN

For ESTIMATED inputs record formula, source, date, range, confidence and sensitivity.

## Comparison rules

- Match specification, unit, quantity, Incoterm and date.
- Preserve original currencies and source values.
- Do not compare list and transaction prices without labeling.
- Do not treat public asking prices as achieved prices.
- Do not treat recoverable VAT as final cost without explanation.
- Mark customs, tax and legal interpretations that need professional verification.

