# Export Need Scoring

## Scope

This model implements only the five requested commercial dimensions and the final `PROCEED` / `WATCH` / `DROP` decision from [SPEC_001](../specs/01_export_need_analyzer.md). It consumes Manufacturing Strength from the accepted manufacturer assessment and does not redefine that score.

Use the [Export Need Assessment](export_need_assessment.md) as the calculation record. No score authorizes contact, CRM activity, outreach or a commercial commitment.

## Evidence-to-points rule

Award each subfactor from 0 to its maximum using direct, cited evidence and written rationale. Apply these caps:

| Evidence state | Maximum award |
|---|---:|
| VERIFIED | 100% of subfactor maximum |
| ESTIMATED | 50% of subfactor maximum |
| HYPOTHESIS | 25% of subfactor maximum |
| UNKNOWN | 0 |

The cap is not an automatic award. Weak evidence may earn less. Use the weakest state when one claim depends on multiple unresolved facts. Same-owner sources do not increase the evidence state. Preserve unrounded subfactor awards; each dimension is the sum of its listed subfactors and ranges from 0 to 100.

## Export Readiness Score

Measures ability to serve foreign customers now; English website content alone earns no points.

| Subfactor | Maximum | Evidence required |
|---|---:|---|
| Verified export activity | 25 | Current foreign shipments, markets, customers when public, or authoritative export evidence |
| Relevant certification and regulatory readiness | 20 | Valid holder, scope and expiry matched to target demand |
| Export documentation, quality and traceability | 15 | Documented systems for specifications, inspection, records and export paperwork |
| International technical communication | 10 | Verified language/technical response capability or international sales function |
| Logistics and trade-term readiness | 15 | Evidence of packaging, customs, Incoterms, freight or cross-border delivery capability |
| International market experience | 15 | Dated fairs, references, projects or sustained foreign-market activity |
| **Export Readiness Score** | **100** | Sum of awarded points |

## Growth Need Score

Measures evidenced ambition or capacity need that external market development could accelerate; it never measures assumed financial distress.

| Subfactor | Maximum | Evidence required |
|---|---:|---|
| Capacity, facility or machinery investment | 25 | Dated installed/commissioned expansion evidence; announcement state identified |
| New product or foreign-market objective | 20 | Specific launch, target market or export-growth statement |
| Capacity-utilization or order-growth need | 20 | Direct evidence of available capacity, target utilization or need for new orders |
| Growth-linked hiring or organization change | 15 | Dated export/international sales or market-development role evidence |
| Signal recency and active timing | 10 | Evidence remains inside its justified action window |
| Relevance of external support | 10 | Growth objective plausibly benefits from external buyer/market access |
| **Growth Need Score** | **100** | Sum of awarded points |

## Business Development Need Score

Measures a specific capability or access gap Atlas could address; company size, weak website or silence are not evidence.

| Subfactor | Maximum | Evidence required |
|---|---:|---|
| Target-country coverage gap | 25 | Target market is relevant but not adequately covered by current team/channel |
| Buyer and procurement-access gap | 25 | Specific difficulty reaching buyer types, qualification routes or category owners |
| Export-sales capacity gap | 20 | Verified staffing, language, process or account-development limitation |
| Channel or partner gap | 15 | Missing/incomplete distributor, agent, representative or sourcing route |
| Defined business-development objective | 15 | Named market/customer objective, timing and internal owner or accepted direct record |
| **Business Development Need Score** | **100** | Sum of awarded points |

## Partnership Openness Score

Measures evidence that the manufacturer may use an external commercial partner; a contact page alone earns no points.

| Subfactor | Maximum | Evidence required |
|---|---:|---|
| Explicit partner, agent or distributor search | 30 | Current first-party notice or accepted authorized statement |
| Existing external-channel model | 20 | Verified use of agents, distributors, representatives or sourcing partners |
| Authorized international-sales route | 15 | Current public or accepted route to the responsible commercial function |
| Prior external collaboration | 15 | Evidence of relevant market-development or commercial partnerships |
| Territory and scope availability | 10 | No evident exclusive conflict and a plausible product/geography scope |
| Partnership governance readiness | 10 | Ability to define lead ownership, support, reporting and commercial responsibilities |
| **Partnership Openness Score** | **100** | Sum of awarded points |

## Atlas Revenue Potential

Measures Atlas's evidence-backed ability to create and capture value; unknown prices, volumes or terms are never invented.

| Subfactor | Maximum | Evidence required |
|---|---:|---|
| Commercial model and Atlas role clarity | 20 | Representation, commission, sourcing, introduction, back-to-back or other defined role |
| Payer and revenue event clarity | 20 | Identifiable payer, compensation basis and event that earns revenue |
| Demand and commercial access strength | 20 | Defined foreign demand plus plausible route to a commercial decision |
| Repeatability and account value | 15 | Evidence of repeat orders, recurring requirement or sufficient one-off value |
| Time to first revenue | 15 | Bounded, evidence-backed gates and timing; `UNKNOWN` timeline earns zero |
| Capital, liability and downside fit | 10 | Acceptable working-capital, payment, quality, logistics and legal exposure |
| **Atlas Revenue Potential** | **100** | Sum of awarded points |

## Final score

Use the six-dimension weights from SPEC_001:

| Dimension | Weight |
|---|---:|
| Manufacturing Strength — consumed, not recalculated | 15 |
| Export Readiness Score | 15 |
| Growth Need Score | 20 |
| Business Development Need Score | 20 |
| Partnership Openness Score | 15 |
| Atlas Revenue Potential | 15 |
| **Total** | **100** |

`Atlas Export Need Score = Σ(dimension score × weight) / 100`

Do not round dimensions or weighted contributions. Round only the final score to the nearest whole number. Recalculate from the worksheet; never type a preferred final score.

## Final decision

### PROCEED

Every condition is mandatory:

- all Export Need Analyzer hard gates PASS;
- Atlas Export Need Score ≥75;
- Evidence Quality ≥70;
- Manufacturing Strength ≥60;
- Export Readiness Score ≥50;
- Growth Need Score ≥55;
- Business Development Need Score ≥60;
- Partnership Openness Score ≥50;
- Atlas Revenue Potential ≥60;
- no decision-critical `UNKNOWN`;
- one deeper partnership-validation action is named.

`PROCEED` authorizes only that validation action, never contact.

### WATCH

Use when the score is 50–74; Evidence Quality is below 70; a floor misses because evidence is incomplete; or a hard gate/contradiction is realistically resolvable. Record one missing fact, its decision impact, smallest verification action, owner, due date and review trigger. No outreach is authorized.

A score below 50 may remain `WATCH` only when one clearly bounded missing fact could plausibly reverse the decision. State that counterfactual explicitly.

### DROP

Use when a hard gate conclusively fails; the score is below 50 without a credible reversal path; manufacturing or demand fit is disproven; no evidenced business-development gap or partnership route exists; Atlas cannot lawfully capture value; risk is unacceptable; or verification cost exceeds plausible value.

Record the decisive reason and evidence. Re-entry requires a new dated signal that materially changes the failed condition.

## Calculation validation

- Five commercial dimension totals each equal the sum of their awarded subfactors and remain 0–100.
- Every awarded point has evidence state, source reference and rationale.
- Evidence-state caps are respected and `UNKNOWN` receives zero.
- Evidence Quality is separate and not added to the final score.
- Manufacturing Strength is consumed without being recalculated here.
- Six final weights total 100 and the final score recalculates.
- Hard gates and dimension floors override the aggregate score.
- The decision authorizes no contact or commitment.
