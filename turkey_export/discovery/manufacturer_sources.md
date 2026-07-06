# Commercial Signal Source Map

## Source purpose

Sources are selected to detect signals, resolve entities and verify claims. Source count alone does not create confidence; independence, authority, recency and claim relevance matter.

## Layer 1 — Public digital sources

| Source | Signals detected | Verification use | Limitation |
|---|---|---|---|
| Company website | Products, new lines, facilities, export claims, partner search | Capability and company-stated activity | Self-reported |
| LinkedIn company page | Hiring, fairs, investment, launches, team growth | Current activity and operating presence | Self-reported; may be incomplete |
| Public job pages | Export/International Sales hiring | Intent to build foreign sales capability | Hiring may close without appointment |
| Google Business | Factory address, phone, operating presence | Entity and location corroboration | User-edited; not production proof |
| Trade directories | Category and company discovery | Candidate routing | Often stale or copied |
| Industry associations | Membership and specialization | Sector corroboration | Membership is not factory proof |
| Certification databases | New/valid certification | Quality and scope verification | Registry coverage varies |

## Layer 2 — Industrial sources

| Source | Signals detected | Verification use | Limitation |
|---|---|---|---|
| OSB directory | New tenant, expansion, industrial address | Factory-location corroboration | May be stale |
| Chamber of Industry | Industrial registration and category | Legal/operating identity | Limited capability detail |
| Chamber of Commerce | Registration and business activity | Entity resolution | Trading activity may dominate |
| Exporters' Association | Exporter membership and activity | Export-readiness corroboration | Membership is not a shipment |
| Industrial cluster | Specialization and partnerships | Capability/partner network | Promotional bias |
| Trade-fair exhibitor list | International fair participation | Market-development signal | Exhibitor may be intermediary |
| Government industrial directory | Facility/incentive/investment record | Authoritative operating signal | Publication lag |
| Machine-supplier reference | New machine or production-line installation | Capacity/investment signal | Marketing claim; scope may be vague |
| Certification registry | Certificate issue, upgrade, scope or expiry | Quality verification | Exact legal entity must match |

## Layer 3 — Commercial signal routes

| Signal | Preferred source combination | Default freshness window | Commercial interpretation |
|---|---|---:|---|
| New export activity/market | Export association or company release + independent entity record | 12 months | Foreign-market intent and learning cycle |
| New certification | Accredited registry + company/fair announcement | Certificate validity | Qualification barrier reduced |
| New machinery/line | Machine supplier or investment record + factory/company evidence | 18 months | Potential capacity or capability expansion |
| Capacity/facility expansion | Government/OSB/chamber + company evidence | 18 months | Need to fill capacity; verify commissioning |
| International fair participation | Official exhibitor list + company identity | 12 months | Active buyer/partner search hypothesis |
| Distributor/partner search | Official company notice + public business route | 6 months | Direct partnership accessibility |
| Export/International Sales hiring | Official job page + LinkedIn/company identity | 90 days | Export organization is being built |
| New product launch | Official launch + technical evidence | 12 months | New buyer segment or supply need |
| New buyer supplier portal/RFQ | Official procurement page + active registration | 90 days | Access route exists; demand still unverified |

Freshness is a review rule, not proof. Extend only with an explained durable effect.

## Source independence

- Multiple company-controlled pages equal one source class.
- A directory copying the company website is not independent.
- A chamber, government, accredited registry or official fair organizer can independently corroborate.
- Search snippets and AI summaries never count as final evidence.
- LinkedIn can support timing or team evidence but does not independently verify a factory claim.

## Weak-digital-presence protocol

When no credible website exists:

1. Start with OSB/chamber/government identity records.
2. Verify factory address and public phone through a second source class.
3. Use fair, machinery, association or certification records to establish capability/signal evidence.
4. Record website maturity as low—not automatic `DROP`.
5. Require higher source independence before `PROCEED`.

## Recording rules

Store direct URLs; source class; publication/event date; access date; evidence state; supported claim and contradiction. Write `UNKNOWN` when the claim cannot be verified.
