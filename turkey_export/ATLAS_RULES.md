# Atlas Rules — Turkey → World

## Authority and scope

These rules govern all work inside `turkey_export/`.

This module is exclusively for **Turkey → World** commercial intelligence: matching verified Turkish industrial supply capabilities with evidence-backed foreign demand and commercially accessible routes to first revenue.

**Foreign → Turkey is stable and must not be modified.** Turkey Export work must not edit, replace, refactor, import into or redefine the existing Foreign → Turkey architecture, agents, databases, playbooks, workflows or decisions.

## Operating boundaries

### Commercial Intelligence only

Turkey Export may produce research specifications, opportunity assessments, manufacturer and buyer intelligence, scoring logic, decision support, commercial recommendations and evidence-backed next actions.

It does not become an ERP, transactional platform, marketplace, sourcing portal or general-purpose software product.

### No CRM

Turkey Export must not implement CRM functionality. It may define the minimum commercial records required to evaluate an opportunity, but it must not create pipeline-management engines, contact-management systems, activity automation or CRM synchronization.

### No email automation

Turkey Export must not automatically send, schedule, sequence or personalize outbound email. It may prepare a draft only after the applicable commercial and authorization gates are satisfied. Sending always requires explicit authorization outside the intelligence specification.

### No invented data

Never invent companies, contacts, demand, orders, RFQs, prices, capacity, certifications, export activity, buyer intent, commercial access or market claims.

Every material claim must be traceable to a named source or repository record. When evidence is missing, write `UNKNOWN` and state the narrowest next verification step. Estimates must be labeled, explained and kept separate from verified facts.

## Commercial doctrine

### Demand first

Begin with evidence of foreign demand, procurement need, supply-chain change, buyer accessibility or a time-sensitive commercial signal. Do not start by accumulating Turkish manufacturer lists and then searching for a reason to use them.

### Supply follows demand

Search for and qualify Turkish supply only after the required product, capability, certification, geography, volume pattern and buyer context are sufficiently defined. Supply must answer a demand hypothesis; it must not create one retroactively.

### Commercial accessibility matters

Technical fit alone is insufficient. An opportunity must have a plausible route to the relevant buyer, procurement process, supplier-registration channel, intermediary or decision-maker. Score access quality, timing, trust requirements and effort alongside product fit.

Public contact details or a supplier portal prove a route exists; they do not prove buyer intent or authorization to contact.

### First revenue probability is the priority

Prioritize the opportunity with the highest evidence-backed probability of producing first revenue within a commercially useful period—not the largest theoretical market, longest company list or most polished report.

Assess at minimum:

- verified demand strength and timing;
- Turkish supply fit and readiness;
- buyer accessibility;
- competitive and trust barriers;
- commercial model feasibility;
- expected time and steps to first revenue;
- downside risk and verification cost.

When evidence is otherwise comparable, prefer the narrower, more accessible and more reversible opportunity.

## Decision discipline

Every specification must define:

- the commercial decision it supports;
- required evidence and accepted source types;
- hard gates and rejection conditions;
- scoring and treatment of unknowns;
- the exact action authorized by each decision;
- acceptance criteria that can be tested without inventing data.

Numeric scores never override failed identity, manufacturing, sanctions, legal, authorization or evidence gates.

Use the decision vocabulary defined by the applicable Turkey Export workflow. A positive decision authorizes only the named next step; it never implies automatic outreach, an order, exclusivity or a commercial commitment.

## Specification-before-implementation rule

All future Turkey Export capabilities must first be defined in `turkey_export/specs/` using `SPEC_TEMPLATE.md`.

A specification describes required commercial behavior and acceptance criteria. It must not contain executable engine code, deployment instructions or architecture changes. Implementation requires separate authorization.

## Non-negotiable safeguards

- Preserve the Turkey → World direction.
- Keep Foreign → Turkey untouched.
- Use public, authorized and commercially relevant evidence.
- Minimize personal data and never scrape private information.
- Record contradictions, limitations and evidence dates.
- Stop research when one defensible commercial decision or next verification action is ready.
- Prefer commercial decisions over document volume.
