# R001 — Turkey Export Discovery Engine v1 Design

## Executive Summary

Discovery Engine v1 defines a source-led, evidence-gated method for discovering Turkish OEM metal-component manufacturers without requiring user-supplied company names. It separates manufacturing verification, export potential and evidence confidence, then permits `PROCEED` only when the company passes hard readiness gates.

Sprint 001 is limited to CNC machining, sheet metal, precision machining, metal fabrication and welded assemblies. This report designs the engine; it does not claim that manufacturer discovery has been executed. The canonical database therefore contains its validated header only and no invented company rows.

## Discovery Sources

The engine discovers candidates through:

- OSB directories;
- sector association directories;
- trade fair exhibitor lists;
- chamber of industry records;
- exporters' union directories;
- company websites;
- official LinkedIn company pages;
- B2B directories used only for discovery;
- ISO and quality-certification references.

Company websites and technical documents are primary evidence for capabilities. Institutional sources support discovery and corroboration. Search results, marketplaces and directory claims cannot serve as final proof.

## Scoring Model

The 0–100 Export Potential Score weights manufacturing evidence and export readiness most heavily, then evaluates quality certifications, product complexity, repeat-order potential, foreign buyer fit, website credibility, communication readiness, sector attractiveness and commission potential.

Discovery Confidence is scored separately from identity, manufacturing evidence, source corroboration, recency and contact verification. Atlas Score combines 70% Export Potential and 30% Discovery Confidence. Every record requires a written rationale explaining evidence, deductions, unknowns and status.

## Validation Rules

`PROCEED` requires:

- real manufacturing evidence;
- export activity or a credible readiness signal;
- verified fit with an allowed subsector;
- sufficient public information for later outreach preparation;
- a usable public business contact channel;
- required source URLs;
- Export Potential, Discovery Confidence and Atlas scores of at least 70.

`WAIT` applies when the candidate is plausible but decisive evidence is missing or a principal score is 50–69. `DROP` applies below 50 or when a hard disqualifier is verified. Numeric scores never override failed hard gates.

## Output Schema

The canonical CSV is `turkey_export/database/turkish_manufacturers.csv`. It contains all required manufacturer fields plus `score_rationale`, which makes each score and status auditable.

Portfolio outputs are:

1. up to 100 qualified discovered manufacturers;
2. up to 20 export-ready `PROCEED` manufacturers;
3. up to five immediate candidates;
4. a specific evidence-backed reason for every `PROCEED` candidate.

These are qualification ceilings, not quotas.

## First Sprint Recommendation

Run a controlled discovery pass by source class and region, deduplicate candidates, and validate the first 25 records before expanding toward 100. Review scoring consistency after the first ten fully evidenced records. Continue only if source quality produces reproducible manufacturing and export-readiness evidence.

Do not begin buyer discovery or outreach preparation until at least one manufacturer passes all `PROCEED` gates.

## Risks

- Directory records may be stale or classify distributors as manufacturers.
- Company websites may overstate machinery, certifications or export experience.
- English-language content can be mistaken for export evidence.
- Certification logos may be expired, irrelevant or unverifiable.
- Company-size signals from public platforms may be inaccurate.
- Score inflation may occur if multiple pages repeat the same underlying claim.
- Filling Top 100 or Top 20 targets may pressure analysts to admit weak records.

Controls are direct-source verification, source triangulation, explicit unknowns, independent confidence scoring, hard gates and refusal to pad ranked outputs.

## Next Action

Execute the first 25-company discovery batch for OEM Metal Components, validate each row against the checklist, and produce the initial ranked evidence review. Owner and execution date: `UNKNOWN`.
