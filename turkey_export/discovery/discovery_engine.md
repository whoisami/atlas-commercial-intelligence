# Commercial Signal Discovery Engine v2

## Mission

Convert public and industrial signals into verified Turkey-to-world commercial opportunities. The engine asks “what changed, where is demand forming, and can Atlas access it?” before asking for a company name.

## Signal-first workflow

```text
Source monitoring
      ↓
Signal capture
      ↓
Entity resolution
      ↓
Multi-source verification
      ↓
Manufacturer / buyer classification
      ↓
Commercial accessibility and timing assessment
      ↓
Opportunity match and Atlas Opportunity Score
      ↓
PROCEED / WAIT / DROP + first action
```

## Layer 1 — Public Digital Discovery

Monitor:

- company websites;
- LinkedIn company and public job pages;
- Google Business records;
- trade directories;
- industry associations;
- certification databases.

Use Layer 1 to detect public change and corroborate identity. A polished website does not prove manufacturing or export activity. A weak website does not disqualify a company.

## Layer 2 — Industrial Discovery

Monitor:

- Organized Industrial Zone (`OSB`) directories;
- chambers of industry and commerce;
- exporters' associations;
- industrial clusters;
- trade-fair exhibitor lists;
- government industrial directories;
- machine-supplier installation and customer references;
- certification registries.

Layer 2 is the primary recovery path for manufacturers with weak digital presence. An institutional record establishes a lead or corroborating fact; it does not alone prove current production capability.

## Layer 3 — Commercial Signal Discovery

Detect dated, decision-relevant signals:

- new export activity or a new export market;
- new or upgraded certifications;
- production investment or machinery installation;
- capacity expansion or a new facility;
- international trade-fair participation;
- distributor, agent or partnership search;
- Export Sales or International Sales hiring;
- a new product launch;
- a new production line;
- foreign buyer supplier-registration activity, RFQ access or procurement expansion.

Every signal records type, date, source, entity, geography, evidence state, commercial interpretation, expiry/review date and contradiction check.

## Entity resolution

Resolve the company only after a signal is captured:

1. Match legal or trading name, city, factory address, phone, domain and institutional identifier.
2. Separate brands, subsidiaries and unrelated namesakes.
3. Confirm manufacturer versus distributor/trader status.
4. Link the signal to the correct operating entity.
5. Preserve unresolved matches as `WAIT`; never force a company assignment.

## Multi-source verification

No entity receives `PROCEED` from one source. Use at least two independent source classes, with one source proving the decisive operating claim.

Possible verification evidence:

- website or technical catalogue;
- factory address;
- public business phone;
- trade-fair participation;
- chamber or OSB registration;
- exporters' association record;
- ISO or sector certification;
- LinkedIn company presence;
- government industrial record.

Repeated pages controlled by the same company count as one source class. Contradictory evidence reduces Verification Score and must be resolved or escalated.

## Manufacturer classification

Confirm capability fit with CNC Machining, Sheet Metal, Precision Machining, Metal Fabrication or Welded Assemblies. Record processes, machinery, materials, quality systems, industries, export signal and capacity evidence. Do not assume export readiness from English content.

## Buyer discovery

Discover need and access signals across:

- foreign OEMs;
- Tier 1 and Tier 2 suppliers;
- procurement companies;
- sourcing companies;
- contract-manufacturing buyers;
- purchasing offices;
- industrial distributors;
- trading companies;
- supply-chain partners.

A supplier portal is an accessibility signal, not proof of an open order. A product portfolio is a fit signal, not proof of outsourcing.

## Opportunity creation

Create an opportunity only when:

- a Turkish manufacturer or unresolved manufacturer signal has relevant capability evidence;
- a foreign buyer type/country has plausible need evidence;
- at least one time-sensitive or accessibility signal exists;
- an Atlas commercial model is plausible;
- the first verification or commercial action is explicit.

Apply [scoring_model.md](scoring_model.md). Numeric scores never override hard verification, sanctions, channel-conflict or manufacturing gates.

## Decision gates

### PROCEED

The entity and decisive claims are multi-source verified; relevant manufacturing fit exists; a current commercial signal or access route exists; and Atlas can execute a specific next step within 90 days.

### WAIT

The hypothesis is plausible but entity resolution, export readiness, source independence, commercial access, timing, buyer need or channel conflict remains unresolved. Name the exact verification action and review date.

### DROP

Manufacturing or buyer identity is disproven, signal is stale/false, fit is absent, accessibility is commercially impractical, material conflict exists or expected value no longer justifies work.

## Stop rules

Stop when one defensible next action is ready. Do not continue collecting companies after the commercial decision is clear. Do not contact anyone, create outreach or convert discovery into CRM activity.
