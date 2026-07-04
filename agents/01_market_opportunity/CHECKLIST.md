# Checklist — Market Opportunity

## Pre-execution

- [ ] The question is “Which product family should Atlas pursue first?”
- [ ] Turkey, technical B2B, repeat purchase and stock-free constraints are explicit.
- [ ] No sector or familiar product family has been preselected.
- [ ] Candidate generation covers multiple sectors and buying mechanisms.
- [ ] Existing product research is treated as evidence, not as the answer.
- [ ] The canonical product schema and current IDs were reviewed.
- [ ] Evidence cutoff and time horizon are defined.
- [ ] Research has a stopping rule.

## Candidate-quality checks

- [ ] Every candidate is a coherent product family, not a vague industry.
- [ ] Consumer, commodity and inventory-heavy candidates were screened out early.
- [ ] Product-family boundaries and relevant HS-code limitations are clear.
- [ ] Fast rejections have a concise reason.
- [ ] Survivors were evaluated under identical criteria.

## Evidence checks

- [ ] Import dependency is supported by E1/E2 evidence or explicitly marked `UNKNOWN`.
- [ ] Import value, market size, production and dependency are not conflated.
- [ ] Repeat-purchase mechanism is evidenced.
- [ ] Stock-free order flow is operationally described.
- [ ] Plausible manufacturers are verified as real manufacturers.
- [ ] Turkish buyer segments or accounts are verified.
- [ ] Local production, substitutes, distributors and competition were checked.
- [ ] Trust, fraud, sanctions and compliance risks were considered.
- [ ] Speed-to-meeting and speed-to-revenue scores have observable reasoning.
- [ ] Search snippets and unsourced market claims are not final evidence.
- [ ] No import values, companies, prices or claims were invented.

## Scoring checks

- [ ] All 11 criteria are scored 0–100.
- [ ] Missing criterion evidence is labeled `UNKNOWN` and scored 0.
- [ ] Weights total 100%.
- [ ] Atlas Score arithmetic was verified.
- [ ] Evidence Quality is scored separately.
- [ ] Scores above 80 have strong, decision-ready evidence.
- [ ] The preferred family was contradiction-tested and rescored if necessary.

## GO gate

- [ ] Atlas Score ≥ 80.
- [ ] Repeat Purchase Potential ≥ 70.
- [ ] Stock-Free Feasibility ≥ 60.
- [ ] Evidence Quality ≥ 70.
- [ ] Manufacturer availability is sufficient for execution.
- [ ] Buyer availability in Turkey is sufficient for execution.
- [ ] No fatal risk or unresolved contradiction remains.
- [ ] GO clearly authorizes manufacturer, buyer and pricing execution—not outreach or spend.

If any box fails, the family cannot be GO.

## Output checks

- [ ] The report is saved as the next `intelligence/market/RXXX.md`.
- [ ] The full scorecard and source logic are visible.
- [ ] `database/products.csv` matches the report.
- [ ] `workspace/active_project.md` matches the decision.
- [ ] Only assigned values in `dashboard/CEO_DASHBOARD.md` were updated.
- [ ] Stable IDs and unrelated content were preserved.
- [ ] Unknowns include the exact next verification action.
- [ ] Downstream actions have owners and decision gates.

## Stop check

- [ ] One family has crossed every GO threshold with sufficient evidence, or no family can do so with the available evidence.
- [ ] Additional research is unlikely to change the first-priority decision.
- [ ] Research stopped when decision usefulness was reached.

