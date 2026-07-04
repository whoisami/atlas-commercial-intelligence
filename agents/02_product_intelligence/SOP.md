# SOP — Product Intelligence

## 1. Verify the handoff

1. Read the accepted `intelligence/market/RXXX.md`.
2. Confirm the selected product family is GO.
3. Capture the market thesis, intended trade model, known buyer use case, score assumptions and unresolved questions.
4. Confirm the product-family boundary.
5. If the market report is missing, not accepted or not GO, stop. Product Intelligence does not select a replacement family.

## 2. Establish product vocabulary and boundaries

1. Define the product's primary function in plain language.
2. Identify what is inside and outside the family.
3. List synonyms, trade names and ambiguous terms.
4. Map components, materials, interfaces and failure points.
5. Separate complete products, components, consumables, accessories and services.

## 3. Build the variant taxonomy

1. Identify the construction or technology families.
2. Map variants by size, capacity, material, operating range, interface, control method and performance class.
3. Identify which variants serve which applications.
4. Separate standardized products from engineered-to-order products.
5. Create a minimum variant matrix another analyst can use consistently.

Do not advance until variant ambiguity is controlled.

## 4. Build the specification model

1. List every parameter needed to select or quote the product correctly.
2. Define units, acceptable ranges and dependencies.
3. Identify application data that the buyer must provide.
4. Identify mandatory datasheet, drawing, sample or testing inputs.
5. Map standards, tolerances, performance tests and documentation.
6. Flag parameters whose error could cause failure, downtime, safety risk or warranty disputes.

## 5. Map applications and industries

For each major application:

1. Describe the process and product function.
2. Identify operating conditions.
3. Map relevant variant and specification requirements.
4. Identify the cost and consequence of failure.
5. Identify likely industries and facility types.
6. Separate proven applications from plausible but unverified ones.

## 6. Map certifications, regulation and classification

1. Identify mandatory legal requirements.
2. Separate tender, buyer and industry-practice requirements.
3. Identify testing, declaration, traceability and documentation obligations.
4. Capture GTIP/HS-code candidates and explanatory scope.
5. Record classification ambiguity and the authoritative verification route.
6. Never state a provisional code as final.

## 7. Map the buying center

Answer for OEM, project and aftermarket routes:

1. Who uses the product?
2. Who identifies the need?
3. Who specifies it?
4. Who approves technical suitability?
5. Who approves the budget?
6. Who executes procurement?
7. Who pays?
8. Who installs and accepts delivery?
9. Who influences replacement brand choice?

Write `UNKNOWN` where evidence is absent.

## 8. Model demand and repeat purchase

1. Separate OEM, new-project, aftermarket, replacement and MRO demand.
2. Identify wear, failure, inspection, regulation, shutdown and capacity triggers.
3. Map maintenance and replacement cycles.
4. Determine whether replacement is planned, condition-based or failure-driven.
5. Identify installed-base lock-in and switching costs.
6. Assess repeat-purchase predictability without inventing intervals.

## 9. Test order, MOQ and stock economics

1. Describe order-unit logic and typical basket composition.
2. Identify whether demand is single-item, kit, batch, project lot or blanket order.
3. Record verified order-size or MOQ evidence; otherwise write `UNKNOWN`.
4. Test made-to-order, direct shipment, project registration, consignment and back-to-back routes.
5. Identify lead-time tolerance and emergency-stock pressure.
6. Decide whether local inventory is optional, helpful or essential.

## 10. Test installation and support

1. Define installation and commissioning complexity.
2. Identify training required for Atlas, buyers and installers.
3. Determine what support can be remote.
4. Identify what requires manufacturer engineers or local service.
5. Map troubleshooting, returns, warranty and failure-analysis needs.
6. State the minimum technical enablement required before sales.

## 11. Map alternatives and lifecycle

1. Identify complementary products and natural cross-sell.
2. Identify direct substitutes and competing technologies.
3. Compare selection logic, lifecycle cost and switching barriers.
4. Map design-in, qualification, operating, maintenance, replacement and obsolescence stages.
5. Define the value proposition for user, specifier, procurement and payer.

## 12. Score and challenge

1. Score all nine required dimensions from 0 to 100.
2. Explain evidence, confidence and commercial effect.
3. Calculate Commercial Product Fit using the controlled formula.
4. Identify the strongest reason to reject the product.
5. Stress-test liability, certification, inventory, support, MOQ and sales-cycle assumptions.
6. Rescore if the contradiction check changes the evidence.

## 13. Decide readiness

- GO when manufacturer research can begin against a precise, supportable specification and commercial model.
- WATCH when targeted product verification is still required.
- NO-GO when the product is structurally incompatible with Atlas's model.

The decision is product readiness, not market attractiveness and not manufacturer approval.

## 14. Write and synchronize outputs

1. Write the next `intelligence/products/RXXX.md`.
2. End the report with GO, WATCH or NO-GO and a commercial recommendation.
3. Update the selected family in `database/products.csv`.
4. Update `workspace/active_project.md` with product-readiness status and next gate.
5. Update only Product Intelligence-owned values in `dashboard/CEO_DASHBOARD.md`.
6. Preserve unrelated records and cite the report ID.
7. If GO, provide Manufacturer Hunter with explicit inclusion, exclusion, specification and certification criteria.

## Escalation

Escalate when product evidence indicates controlled goods, material safety or product-liability exposure; when regulatory interpretation requires licensed advice; when customs classification remains decisive and ambiguous; or when completion would require external contact not authorized by Atlas CEO.

## Completion definition

Work is complete only when a technically literate Manufacturer Hunter can identify suitable producers without guessing what the product is, and Atlas can explain how the product is bought, supported, replaced and represented.

