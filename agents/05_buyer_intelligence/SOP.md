# SOP — Buyer Intelligence

## 1. Verify the handoff

1. Read the accepted Market Opportunity GO report.
2. Read the accepted Product Intelligence GO report.
3. Extract product applications, variants, industries, buying roles, replacement logic, OEM/aftermarket routes and technical constraints.
4. Confirm Türkiye is the buyer geography.
5. If product-use or buying-role logic is incomplete, stop and return the handoff.

## 2. Define the ideal customer profiles

Create separate profiles for applicable buyer types:

- Industrial Manufacturer
- OEM
- Machine Builder
- System Integrator
- Maintenance Company
- MRO Company
- EPC Contractor
- Industrial Service Company
- Large End User
- Authorized Dealer
- Government / Municipality

For each profile define:

- Qualifying operation or facility
- Product application
- Purchase trigger
- User and specifier
- Procurement route
- Repeat-purchase mechanism
- Exclusions
- Strong and weak evidence signals

## 3. Build the account universe

Search public sources such as:

- Official company and facility pages
- Industrial-zone and chamber records
- Sector associations
- Public tender and project sources
- OEM product catalogues
- EPC project references
- Maintenance and service portfolios
- Government and municipality sources
- Trade fairs and exhibitor records
- Professional company pages
- Credible industry publications
- Existing lawful internal data

Build by application, facility and buyer role—not by generic keyword alone.

## 4. Resolve each entity

1. Verify legal/trading company identity.
2. Verify Turkish operation and city.
3. Identify facility or operational unit.
4. Distinguish parent, subsidiary, dealer, branch and brand.
5. Resolve duplicates.
6. Record website and LinkedIn company page.
7. Reject non-operating, irrelevant or unverifiable entities.

## 5. Prove or hypothesize product need

For each account:

1. State the potential product need.
2. Explain the technical or commercial reason.
3. Link the need to verified operations.
4. Search for installed equipment, project, tender, maintenance or procurement signals.
5. Classify as Verified Demand, Strong Demand Hypothesis, Weak Relevance or No Fit.
6. Record contradictory evidence.
7. Reject weak relevance and no-fit accounts from priority tiers.

## 6. Model purchase behavior

1. Identify demand route: OEM, project, aftermarket, MRO, service, dealer or public procurement.
2. Identify purchase trigger.
3. Estimate frequency only from supported lifecycle/project evidence.
4. Use ranges where defensible.
5. Write `UNKNOWN` when frequency cannot be verified.
6. Identify whether demand is planned, shutdown-driven, tendered, emergency or failure-driven.
7. Identify likely order-unit and qualification behavior without inventing quantities.

## 7. Map the buying center

Identify or mark `UNKNOWN`:

- User department
- Maintenance/reliability
- Specifier
- Engineering/technical approval
- Quality/compliance
- Budget owner
- Procurement/purchasing
- Payer/legal entity
- Installer/service provider

Map departments before people. Record a named person only when a relevant public professional role is available.

## 8. Verify public contact routes

Collect only public business information:

- Purchasing contact, if public
- Professional title
- Public business email
- Company email
- Company phone
- LinkedIn company page
- Public professional profile, when relevant

Do not infer contact details or collect private information. Record source and verification date.

## 9. Score each account

1. Score Need.
2. Score Buying Probability.
3. Score Repeat Purchase Potential.
4. Score Strategic Importance.
5. Score Ease of Contact.
6. Score Market Influence.
7. Calculate Priority Score.
8. Score Evidence Quality separately.
9. Explain evidence, confidence and unknowns.
10. Assign GO, WATCH or NO-GO.

Use identical rules across buyer types; explain type-specific interpretation.

## 10. Challenge the pipeline

1. Remove accounts included only because of industry adjacency.
2. Check whether the company actually buys or merely influences.
3. Check whether purchasing sits at a parent or group entity.
4. Check whether the product is embedded by an OEM and not bought by the end user.
5. Check incumbent dealer or framework constraints.
6. Check public procurement constraints.
7. Check duplicates, closed facilities and stale projects.
8. Rescore when evidence changes.

## 11. Build commercial tiers

### Top 100 Buyers

All highest-quality qualified accounts, ranked by Priority Score and evidence. Include fewer than 100 when the evidence standard is not met.

### Top 25 Priority Buyers

Accounts with strongest need, recurrence, probability and strategic value.

### Top 10 Immediate Targets

Only GO accounts with:

- Verified Turkish operation
- Specific product need
- Identified decision-maker department
- Public company response channel
- Clear first-contact hypothesis
- Explicit risk or unknown note

“Immediate” means ready for contact planning, not authorized to contact.

## 12. Design the first-contact strategy

Define:

- Buyer segment order
- Department to approach first
- Problem/value hypothesis
- Evidence or question to lead with
- Technical material required
- What not to claim
- Follow-up logic
- Manufacturer information still needed

The strategy must be useful before Atlas contacts a manufacturer: it should show manufacturers that Atlas understands real Turkish demand.

## 13. Write and synchronize outputs

1. Write the next `intelligence/buyers/RXXX.md`.
2. End with the six required sections in order.
3. Update `database/buyers.csv` for every evaluated account.
4. Update `workspace/active_project.md` with pipeline status and next gate.
5. Update only Buyer Intelligence-owned values in `dashboard/CEO_DASHBOARD.md`.
6. Preserve stable IDs, source history and unrelated content.
7. Cite the report ID and verification date.
8. Route Top 10 to Atlas CEO and Outreach Intelligence for later contact preparation.

## Escalation

Escalate privacy concerns, restricted data, public-procurement legal ambiguity, sanctions concerns, sensitive infrastructure, contradictory entity identity or any request to contact externally.

## Completion definition

Work is complete when Atlas can show a manufacturer a credible, evidence-backed Turkish buyer pipeline with clear applications and buying routes—not a directory of companies.

