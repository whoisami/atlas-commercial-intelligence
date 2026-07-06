# Commercial Signal Output Schema v2

## Evidence state

Every scored claim uses `VERIFIED`, `ESTIMATED` or `UNKNOWN`. Source URLs remain mandatory for named entities.

## Manufacturer record

File: `turkey_export/database/turkish_manufacturers.csv`

Retain the v1 identity/capability fields and add:

| Field | Rule |
|---|---|
| discovery_signal_type | Signal taxonomy value or `UNKNOWN` |
| discovery_signal_date | ISO date or `UNKNOWN` |
| signal_evidence_state | VERIFIED / ESTIMATED / UNKNOWN |
| source_classes | Independent classes separated by `|` |
| verification_score | 0–100 or `UNKNOWN` pending recalculation |
| commercial_accessibility_score | 0–100 or `UNKNOWN` |
| commercial_signal_score | 0–100 or `UNKNOWN` |
| signal_summary | Evidence-backed signal and limitation |

Legacy `discovery_confidence` remains for audit history but does not substitute for v2 Verification Score.

## Buyer record

File: `turkey_export/database/foreign_buyers.csv`

Add source classes, verification score, accessibility score, signal score, signal date/state and signal summary. Buyer type must support OEMs, Tier suppliers, procurement/sourcing companies, contract-manufacturing buyers, purchasing offices, distributors, traders and supply-chain partners.

## Opportunity record

File: `turkey_export/database/opportunities.csv`

The fields below preserve the v2 upstream discovery-screening record. Its `atlas_opportunity_score` must not be overwritten with the final five-dimension score from [Opportunity Scoring](opportunity_scoring.md). Record the final post-match score in an [Opportunity Scorecard](opportunity_scorecard.md) until a separately authorized schema migration defines a distinct field.

Every row must contain:

| Required field | Rule |
|---|---|
| turkish_manufacturer | Named verified entity or `UNKNOWN` while entity resolution is open |
| potential_foreign_buyer_type | Verified/estimated buyer role |
| potential_country | Country supported by evidence |
| commercial_model | Plausible Atlas model; not authorization |
| manufacturing_score | 0–100 with evidence state/rationale |
| export_readiness_score | 0–100 with evidence state/rationale |
| accessibility_score | 0–100 |
| signal_score | 0–100 |
| revenue_potential_score | 0–100 |
| execution_speed_score | 0–100 |
| verification_score | 0–100 |
| atlas_opportunity_score | Weighted v2 score |
| score_evidence_state | VERIFIED / ESTIMATED / UNKNOWN |
| evidence_summary | Independent sources, decisive facts, deductions and unknowns |
| why_now | Dated signal and commercial timing implication |
| first_recommended_action | One specific reversible action |
| decision | PROCEED / WAIT / DROP |

The named foreign buyer may remain as supporting context, but the v2 decision is framed around a buyer type and country until buyer-specific need is verified.

## Data rules

- UTF-8 CSV; one header; one distinct entity/opportunity per row.
- `UNKNOWN` replaces unsupported data.
- Multiple URLs/classes use `|`.
- Every score is reproducible and its evidence state is explicit.
- Existing v1 records keep their historical fields; v2 fields remain `UNKNOWN` until recalculated.
- No record is upgraded solely because more URLs repeat the same claim.

## Portfolio outputs

Rank commercial signals/opportunities by Atlas Opportunity Score only after v2 validation. Report fewer results rather than padding. Every `PROCEED` row explains why now and the first action.
