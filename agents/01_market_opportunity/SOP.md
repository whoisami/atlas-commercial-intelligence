# SOP — Market Opportunity

## 1. Establish the decision frame

1. Read `workspace/active_project.md`, `workspace/current_sprint.md` and `dashboard/CEO_DASHBOARD.md`.
2. Confirm Atlas's operating constraints: Turkey focus, technical B2B, repeat purchase, stock-free preference, limited capital and need for near-term meetings and revenue.
3. Define the evidence cutoff and decision time horizon.
4. Record any explicit exclusions. Do not infer preferred sectors.

## 2. Build a sector-neutral candidate universe

1. Generate product-family candidates from Turkish import patterns, industrial maintenance demand, production inputs, regulations, capex projects and replacement cycles.
2. Include multiple sectors and purchase mechanisms.
3. Keep product families commercially coherent: broad enough to support several manufacturers and buyers, narrow enough to share technical and buying logic.
4. Record why each family entered the longlist.
5. Do not give incumbent Atlas research an automatic advantage.

## 3. Apply fast elimination gates

Reject or park candidates before deep research when any of the following is evident:

- Mostly consumer or commodity trade.
- One-off purchase with weak replacement demand.
- Requires substantial local inventory or working capital.
- Dominated by entrenched exclusive channels.
- Minimal technical differentiation.
- No identifiable Turkish industrial buyer base.
- No credible pool of export manufacturers.
- High fraud, sanctions, safety or compliance risk.
- Sales cycle clearly incompatible with first-revenue objectives.

Document every fast rejection briefly. Do not spend equal research time on weak candidates.

## 4. Deep-score survivors

For each surviving family:

1. Verify Turkish import dependency or label the exact value `UNKNOWN` and use a documented proxy.
2. Map repeat-purchase mechanisms.
3. Assess technical barriers and qualification requirements.
4. Test margin potential without inventing price data.
5. Design the order flow and test stock-free feasibility.
6. Verify at least several plausible manufacturers.
7. Verify Turkish buyer segments and example accounts.
8. Map incumbents, local producers and channel intensity.
9. Assess trust and fraud exposure.
10. Estimate meeting speed and revenue speed using observable sales-cycle evidence.
11. Assign 0–100 criterion scores using the controlled rubric.
12. Calculate the weighted Atlas Score and separate Evidence Quality score.

## 5. Challenge the preferred answer

1. Search for evidence that Turkey is less import-dependent than it appears.
2. Identify local substitutes and powerful incumbent distributors.
3. Check whether repeat purchasing belongs to the OEM rather than the end user.
4. Test whether manufacturers can actually ship direct or work back-to-back.
5. Identify certification, tender, vendor-list, warranty or payment barriers.
6. State the strongest reason the opportunity may fail.

If a contradiction changes a criterion, rescore it.

## 6. Apply the decision rules

- GO only when Atlas Score ≥ 80, Repeat Purchase ≥ 70, Stock-Free Feasibility ≥ 60 and Evidence Quality ≥ 70.
- WATCH when the opportunity is plausible but any GO gate is missed or a solvable critical unknown remains.
- NO-GO when structural economics, access or risk make the opportunity unattractive.

The first family to clear all GO gates with sufficient evidence becomes the recommended execution priority.

## 7. Use the stopping rule

Stop research when:

- One family clears every GO gate.
- The decisive evidence has been contradiction-checked.
- Remaining unknowns are execution questions rather than selection blockers.
- More candidate research is unlikely to change the first-priority decision.

Do not extend the longlist for appearance or completeness.

## 8. Write the report

1. Use the next sequential file: `intelligence/market/RXXX.md`.
2. Include the candidate funnel, full scorecard, evidence, unknowns and decision.
3. State exactly what GO authorizes.
4. Assign downstream actions to Manufacturer Hunter, Buyer Intelligence and Pricing Intelligence.
5. Link every material claim to a source.

## 9. Update controlled operating surfaces

After the report passes the checklist:

1. Update `database/products.csv` with one record per scored family. Preserve stable IDs and unrelated rows.
2. Update `workspace/active_project.md` with the selected product family, report ID, status and next decision gate.
3. Update only the Market Opportunity-assigned values in `dashboard/CEO_DASHBOARD.md`:
   - GO product opportunities
   - Selected product family
   - Atlas Score
   - Evidence Quality
   - Primary import-dependency evidence
   - Critical unknown
   - Source report
4. Do not alter another agent's dashboard values.
5. If no family is GO, record the leading WATCH candidate and its promotion trigger.

## Escalation

Stop and escalate when evidence indicates sanctions, controlled goods, material safety or legal risk; when canonical IDs conflict; or when the requested action would authorize external contact, spend, stock or a commercial commitment.

## Completion definition

The task is complete when one defensible decision exists, the report and three controlled surfaces agree, every score is traceable, unknowns are explicit, and the next execution actions have owners.

