# Discovery Output Schema

## Canonical database

File: `turkey_export/database/turkish_manufacturers.csv`

| Field | Type / allowed values | Rule |
|---|---|---|
| company_name | Text | Verified public company name |
| city | Text / `UNKNOWN` | Turkish operating city |
| website | URL | Official website |
| subsector | Pipe-separated values | Allowed Sprint 001 subsectors only |
| capabilities | Pipe-separated text / `UNKNOWN` | Evidence-backed production capabilities |
| export_evidence | Text / `UNKNOWN` | Verified export fact or specific readiness signal |
| certifications | Pipe-separated text / `UNKNOWN` | State verification limits in rationale |
| machinery_evidence | Text / `UNKNOWN` | Direct machinery or production-equipment evidence |
| industries_served | Pipe-separated text / `UNKNOWN` | Evidence-backed end industries |
| apparent_company_size | Text / `UNKNOWN` | Public estimate with basis in rationale |
| foreign_language_readiness | Text / `UNKNOWN` | Languages and supporting evidence |
| contact_channel | Text / `UNKNOWN` | Public business route only |
| source_urls | Pipe-separated URLs | Required; direct evidence pages |
| discovery_confidence | Integer 0–100 | Calculated under the confidence model |
| export_potential_score | Integer 0–100 | Weighted commercial score |
| atlas_score | Integer 0–100 | 70% potential + 30% confidence |
| status | `PROCEED` / `WAIT` / `DROP` | Must satisfy status gates |
| score_rationale | Text | Positive evidence, deductions, unknowns and status reason |

## Data rules

- UTF-8 CSV with one header row.
- One row per distinct manufacturer entity.
- Use `UNKNOWN`, never a blank, for unavailable business data.
- Separate multiple values and URLs with `|`.
- Do not place commas in unquoted fields.
- Scores must be reproducible from the cited evidence and report scorecard.

## Ranked report outputs

### Top 100 discovered manufacturers

Include rank, company, city, subsector, Export Potential Score, Discovery Confidence, Atlas Score, status and concise reason.

### Top 20 export-ready manufacturers

Include only `PROCEED` records. Add export signal, strongest capability, quality evidence, public contact route, key risk and next validation action.

### Top 5 immediate candidates

Include only manufacturers with enough public data for later outreach preparation. Add the explicit selection reason, decisive evidence, main risk and next best action.

If the qualified population is smaller than a target, report the actual count and reason; never pad the output.
