# Discovery Engine v1

## Mission

Discover and rank Turkish OEM metal-component manufacturers that Atlas could support in foreign-market business development without requiring the user to supply company names.

## Scope gate

Include only manufacturers with evidence of one or more Sprint 001 capabilities:

- CNC Machining
- Sheet Metal
- Precision Machining
- Metal Fabrication
- Welded Assemblies

Reject distributors, traders, marketplaces, service-only intermediaries and companies whose manufacturing claim cannot be verified.

## Workflow

### 1. Build the discovery universe

Search the approved source classes in [manufacturer_sources.md](manufacturer_sources.md). Record the discovery source and company website as soon as a candidate is identified. Deduplicate legal names, brands and group companies before scoring.

### 2. Verify manufacturer identity

Confirm the candidate is a Turkish operating manufacturer. Look for process pages, factory information, machinery, production photographs, technical documents, quality references and consistent company identity. A directory label alone is not manufacturing evidence.

### 3. Classify capability fit

Assign one or more allowed subsectors only when public evidence supports them. Record processes, materials, tolerances, machinery and industries served. Unsupported details remain `UNKNOWN`.

### 4. Assess export readiness

Look for foreign-language pages, export markets, international customers, trade-fair participation, export logistics, international standards, public export contacts and credible technical documentation. Do not infer exports from an English website alone.

### 5. Triangulate evidence

Use the company website as the primary source for capabilities. Corroborate identity, certifications or international activity with independent credible sources where available. Resolve contradictions or downgrade discovery confidence.

### 6. Score candidates

Apply [scoring_model.md](scoring_model.md). Every awarded score must be supported by fields and source URLs. Write a concise `score_rationale` explaining the decisive positive evidence, deductions and unknowns.

### 7. Validate and decide

Run [validation_checklist.md](validation_checklist.md). Assign exactly one status:

- `PROCEED`
- `WAIT`
- `DROP`

`PROCEED` requires real manufacturing evidence, an export or export-readiness signal, clear capability fit and enough public data to prepare later outreach. A high numeric score cannot override a failed hard gate.

### 8. Produce ranked outputs

Rank by `atlas_score`, then `export_potential_score`, then `discovery_confidence`. Produce:

- up to 100 qualified discovered manufacturers;
- the top 20 export-ready `PROCEED` manufacturers;
- the top five immediate candidates;
- a specific evidence-backed reason for each `PROCEED` candidate.

Do not fill an output tier with weak records to meet a target.

## Stop rules

Stop investigating a record when:

- its identity or manufacturing status cannot be verified after the planned source checks;
- it is outside the allowed subsectors;
- decisive evidence supports `DROP`;
- enough evidence exists to assign a defensible score and status.

Discovery must not drift into buyer research, outreach writing, contact execution or CRM activity.
