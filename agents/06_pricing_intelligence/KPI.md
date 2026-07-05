# KPIs — Pricing Intelligence

## North-star outcome

**Accuracy of the recommended commercial model's realized net contribution, cash requirement and risk compared with the pre-decision forecast.**

The agent is not rewarded for finding a high theoretical margin.

## Evidence-quality KPIs

| KPI | Definition | Target |
|---|---|---:|
| Evidence-state coverage | Monetary/rate inputs labeled VERIFIED, ESTIMATED or UNKNOWN | 100% |
| Estimate reproducibility | Estimates with formula, source, date, range and confidence | 100% |
| Comparable-price coverage | Prices used in conclusions normalized for specification and basis | 100% |
| Customs traceability | Duty/import assumptions linked to authoritative sources | 100% |
| Quote freshness | Decision-critical quotes within stated validity or flagged stale | 100% |
| Hidden UNKNOWN rate | Decision-critical unknowns not disclosed | 0 |

## Forecast-accuracy KPIs

- Forecast gross margin versus realized gross margin.
- Forecast net margin versus realized net margin.
- Forecast commission versus realized commission.
- Forecast first-revenue date versus actual.
- Forecast working-capital peak versus actual.
- Forecast FX/freight impact versus actual.
- Model recommendation reversal rate after verified pricing.

Targets are calibrated by product and transaction type; material variances require a documented cause.

## Commercial-viability KPIs

| KPI | Definition | Target |
|---|---|---:|
| GO model viability | GO opportunities retaining at least one viable model after verification | ≥ 85% |
| Positive net contribution | GO base cases with positive net contribution | 100% |
| Controlled downside | GO cases without uncontrolled downside loss/cash exposure | 100% |
| Capital-fit compliance | GO models compatible with Atlas capital constraints | 100% |
| Model clarity | Reports with one primary model and explicit fallback/conditions | 100% |

## Scoring integrity

- GO cases with Atlas Score ≥ 75: **100%**
- GO cases with Profitability ≥ 65: **100%**
- GO cases with Cash Flow Strength ≥ 60: **100%**
- GO cases with Risk ≤ 40: **100%**
- GO cases with Evidence Quality ≥ 70: **100%**
- Atlas Score arithmetic errors: **0**
- Gross/net/commission margin mislabeling: **0**

## Risk-protection KPIs

- Customs or tax surprises caused by ignored public evidence: **0**
- Recoverable VAT incorrectly treated as permanent cost: **0**
- Unmodeled inventory exposure after GO: **0**
- Unmodeled payment-timing exposure after GO: **0**
- Unauthorized quotes, purchases or commercial commitments: **0**

## Efficiency KPIs

| KPI | Definition | Target |
|---|---|---:|
| Time to pricing decision | Complete inputs to GO/WATCH/NO-GO | ≤ 5 business days unless quotes/professional verification block |
| Decision-changing sensitivity coverage | Assumptions capable of reversing decision identified | 100% |
| Stale-observation overwrite | Historical prices overwritten instead of versioned | 0 |
| Open-ended WATCH | WATCH without input, owner and threshold | 0 |
| Duplicate calculation effort | Rework caused by undocumented formulas | 0 |

## Feedback loop

Atlas CEO records:

- Negotiated supplier price and terms.
- Actual freight, duty, fees and FX.
- Buyer selling price or commission base.
- Payment timing.
- Operating costs.
- Realized contribution.
- First-revenue date.
- Reason for model change.

Learning Intelligence uses actual-versus-forecast results to recalibrate assumptions and thresholds.

## Review cadence

- Recheck arithmetic and evidence states before every report closes.
- Refresh volatile FX, freight and tariff assumptions before commercial use.
- Compare forecast to actual after each order.
- Recalibrate by commercial model quarterly.
- Never improve apparent accuracy by hiding uncertainty.

