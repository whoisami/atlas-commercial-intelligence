# SPEC_005 — Commercial Models

## Purpose

Define how Atlas selects a lawful, transparent Turkey → World commercial model for a verified opportunity. Selection follows demand, match and opportunity validation; it prioritizes first-revenue probability, commercial accessibility and controlled capital risk. This document specifies decisions only and implements no transaction, CRM, outreach, contract or automation.

## Inputs

| Input | Required content | Evidence rule |
|---|---|---|
| Opportunity record | Buyer need, Turkish supplier, fit, access, status | Accepted upstream record; `WATCH` caps model decision at `WATCH` |
| Parties and authority | Legal entities, roles, mandate, territory, products, channel conflicts | Authority and representation claims require first-party or accepted contractual evidence |
| Economics | Payer, revenue event, fee/commission/margin, currency, taxes, costs | `VERIFIED`, `ESTIMATED` or `UNKNOWN`; never invent prices or volumes |
| Risk allocation | Title, payment, quality, warranty, logistics, liability, working capital | Material obligations must have a named responsible party |
| Timing and repeatability | Gates to first revenue, payment timing, repeat-order logic | Assumptions and evidence expiry are explicit |

## Outputs

- Recommended model and fallback model, each with parties, Atlas role, payer and revenue event.
- Evidence state, economics range or `UNKNOWN`, capital exposure, responsibilities and key risks.
- Decision: `PROCEED`, `WATCH` or `DROP`, with exact next validation action.
- Non-authorization statement: output does not authorize contact, contracting, quotation, purchasing or trading.

## Commission representation

Atlas represents a Turkish supplier in a defined foreign scope; the supplier contracts and invoices the buyer, while Atlas earns commission on a precisely defined event, preferably collected customer payment. Require written authority, territory/product scope, lead attribution, commission basis, payment timing, term, termination and post-termination protection. Prefer when the supplier can quote, deliver and support directly.

## Sourcing partnership

Atlas partners with a verified sourcing company or procurement intermediary to identify or qualify Turkish supply. Define each party's mandate, buyer ownership, supplier ownership, work split, fee share, confidentiality, non-circumvention and conflict rules. Require evidence that the partner has relevant buyer access; network claims alone are insufficient.

## Buyer mandate

A foreign buyer formally authorizes Atlas to source or qualify Turkish suppliers against a defined requirement. The buyer is the client and payer unless the mandate explicitly states otherwise. Require written scope, specifications, decision rights, fee basis, expense treatment, confidentiality, supplier communication rules and conflict disclosure. Do not accept undisclosed dual compensation.

## Supplier introduction

Atlas makes a bounded introduction between a verified Turkish supplier and foreign buyer, without ongoing representation or taking title. Define the introduced parties, protected opportunity, introduction evidence, success event, fee, payment period, expiry and non-circumvention terms. Prefer only when ongoing service is unnecessary and fee enforceability is commercially credible.

## Back-to-back trading

Atlas buys from the Turkish supplier and resells to the foreign buyer as principal. Atlas carries contractual, payment, currency, tax, title, delivery, quality and warranty exposure. Require verified buy/sell prices, Incoterms, payment security, duties/taxes, inspection, insurance, sanctions/legal clearance, cash-flow coverage and positive downside-case margin. Use only when lower-capital models are unavailable or materially inferior.

## Success criteria

A model is successful only when the payer, revenue event and Atlas value are explicit; authority and access are verified; economics remain viable after costs and risk; responsibilities are assignable; time to first revenue is commercially useful; repeatability is plausible or one-off value is sufficient; and no material conflict, legal or integrity issue remains. A signed agreement without an accessible revenue path is not success.

## Selection rules

1. Apply [`ATLAS_RULES.md`](../ATLAS_RULES.md); Turkey → World only and no invented data.
2. Select the simplest model that preserves trust, captures fair value and maximizes evidence-backed first-revenue probability.
3. Prefer commission representation, buyer mandate, sourcing partnership or supplier introduction before principal trading when expected value is comparable.
4. Use a buyer mandate when the buyer controls the requirement and formally authorizes sourcing; use representation when the supplier authorizes market development.
5. Use a sourcing partnership only with verified intermediary mandate and access; use supplier introduction only for a bounded, protectable connection.
6. Use back-to-back trading only after verified economics, risk ownership, legal review and working-capital approval.
7. Disclose all compensation and conflicts. Never collect from both sides without informed written consent and legal acceptability.
8. Treat missing payer, authority, revenue event, mandatory price or risk owner as a hard gate; scores or enthusiasm cannot override it.
9. Stop when one preferred model and one next validation action are defensible.

## Decision

- **PROCEED:** opportunity and parties are verified; written authority or mandate is obtainable and evidenced; payer, revenue event, scope, responsibilities and access are clear; economics are viable; legal/sanctions/conflict gates pass; capital and liability are approved where applicable. Authorizes model-specific commercial validation only.
- **WATCH:** one potentially resolvable critical fact is `UNKNOWN`, contradictory or awaiting authorization. Record the missing fact, owner, deadline and expiry; no contact, agreement or transaction is authorized.
- **DROP:** authority, access, payer or revenue event is structurally absent; economics fail; risk is unacceptable; a conflict cannot be managed; evidence integrity fails; or expected value does not justify further work.

## Acceptance criteria

- [ ] All five models define Atlas role, payer logic, revenue event and principal risks.
- [ ] Selection is demand-led and evaluates accessibility, first-revenue probability and capital exposure.
- [ ] Missing evidence is `UNKNOWN`; hard gates override model preference.
- [ ] Dual compensation, authority, conflicts and back-to-back risk have explicit safeguards.
- [ ] `PROCEED`, `WATCH` and `DROP` state testable conditions and limited authorization.
- [ ] No model is implemented and no CRM, outreach, contract or transaction is created.
