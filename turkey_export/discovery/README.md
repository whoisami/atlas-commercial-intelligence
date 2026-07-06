# Turkey Export Commercial Signal Discovery Engine v2

Discovery Engine v2 does not begin with company names. It detects commercial signals, resolves the organizations behind those signals, verifies them across independent source classes and ranks collaboration opportunities by commercial probability.

## Mission

Identify Turkish manufacturers and potential foreign buyer types with the highest probability of a commercially useful relationship within 90 days—even when the manufacturer has weak digital presence.

## Sprint scope

- CNC Machining
- Sheet Metal
- Precision Machining
- Metal Fabrication
- Welded Assemblies

## Components

- [discovery_engine.md](discovery_engine.md) — layered signal-to-opportunity workflow
- [manufacturer_sources.md](manufacturer_sources.md) — public, industrial and signal source map
- [scoring_model.md](scoring_model.md) — verification, accessibility, signal and Atlas Opportunity scores
- [validation_checklist.md](validation_checklist.md) — multi-source and decision gates
- [output_schema.md](output_schema.md) — manufacturer, buyer and opportunity records
- [export_need_analyzer.md](export_need_analyzer.md) — post-discovery manufacturer need evaluation
- [export_need_assessment.md](export_need_assessment.md) — controlled assessment and validation record

## Core principle

Atlas searches for evidence of change, readiness, need and access. A company record is created only after a signal can be associated with a real organization. Company websites are useful but never mandatory and never sufficient by themselves.

## Evidence states

- **VERIFIED:** directly supported by a current primary or authoritative institutional source.
- **ESTIMATED:** derived from identified public evidence; method and limitation are explicit.
- **UNKNOWN:** not supported; no positive score is awarded.

## Required opportunity output

Every opportunity contains Turkish Manufacturer, Potential Foreign Buyer Type, Potential Country, Commercial Model, Accessibility Score, Signal Score, Verification Score, Atlas Opportunity Score, Evidence Summary, Why Now, First Recommended Action and `PROCEED` / `WAIT` / `DROP`.

## Boundaries

This is commercial intelligence—not CRM, scraping or outreach automation. It never invents export readiness, never contacts a company and never writes outreach emails during discovery.

The Export Need Analyzer runs only after discovery has produced a stable Turkish manufacturer record and a defined foreign-demand context. Its `PROCEED` / `WATCH` / `DROP` decision is separate from the Discovery Engine's portfolio decision and authorizes no contact.
