# Turkey Export Discovery Engine

Discovery Engine v1 identifies Turkish OEM metal-component manufacturers with credible export potential. It supplies qualified manufacturer intelligence to the wider Turkey Export module without contacting companies or producing outreach.

## Sprint 001 scope

- CNC Machining
- Sheet Metal
- Precision Machining
- Metal Fabrication
- Welded Assemblies

## Components

- [discovery_engine.md](discovery_engine.md) — operating workflow and decision gates
- [manufacturer_sources.md](manufacturer_sources.md) — source hierarchy and search routes
- [scoring_model.md](scoring_model.md) — evidence-based scores and status rules
- [validation_checklist.md](validation_checklist.md) — record-level quality gate
- [output_schema.md](output_schema.md) — canonical CSV and portfolio outputs

## Required portfolio outputs

1. Top 100 discovered manufacturers
2. Top 20 export-ready manufacturers
3. Top 5 immediate candidates
4. Reason for every `PROCEED` candidate, backed by evidence

Targets are maximum qualified outputs, not quotas. The engine reports fewer records when evidence is insufficient.

## Boundaries

This is commercial intelligence, not a CRM, scraper or email system. It uses public business evidence, writes `UNKNOWN` for unverified data, requires source URLs for every company and never contacts anyone.

Do not create outreach emails yet. Discovery ends with manufacturer qualification and a next-action recommendation.
