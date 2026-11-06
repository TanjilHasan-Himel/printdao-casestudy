# Business analysis and BRD

## Business need and objectives

**DOCUMENTED:** The PRD describes fragmented file handoff, manual counting/pricing, payment checks and queue coordination in university-area print shops. The intended objectives are fewer ordering steps, consistent pricing, traceable orders and operator-controlled printing. No stakeholder interviews, market study or baseline measurements were available in this review.

## Stakeholders and scope

| Actor | Need | Status |
| --- | --- | --- |
| Student | Submit, understand price, track and collect without registration | DOCUMENTED |
| Shop owner | Configure shop, verify payment, manage queue and printers | DOCUMENTED |
| Shop staff | Handle counter operations and exceptions | INFERRED; role permissions unvalidated |
| Platform operator | Maintain multi-shop service and operational support | INFERRED |

MVP scope follows the guest order and owner-controlled print workflow. Advanced CRM, CMS, administration and automated payments are future direction, not validated current capability.

## As-Is and To-Be

**DOCUMENTED As-Is problem description:** Student transfers file through messaging/USB → staff downloads and counts → staff quotes price → payment checked → file printed → student identified for collection. This is a PRD narrative, not an observed field study.

**DOCUMENTED To-Be:** Student opens shop → uploads/configures → server calculates price → order gets a tracking reference → owner verifies payment and selects a job → bridge prints → student tracks and collects. End-to-end behavior remains UNVERIFIED.

## Business rules and exceptions

Student registration is optional for basic ordering. Payment and printing must be independent in the requirements. Cash requires physical collection before printing, and the queue must allow owner priority. Server calculations are authoritative. Shop data must remain tenant-isolated. Closed shops, unavailable prices/payment methods and invalid documents require explicit failure handling. The state-model discrepancy is tracked in the engineering report.

## Feasibility

**VERIFIED technical foundation:** Web, backend integration and Windows bridge code exist. **UNKNOWN technical readiness:** Hardware reliability and full isolation under real use. **INFERRED operational constraint:** Each shop needs a maintained Windows machine, configured printers and a person to verify manual payments. **UNKNOWN financial feasibility:** No defensible infrastructure cost model, unit economics, pricing research or revenue evidence was found in this review.

## Risk register

| Risk | Impact | Proposed response | Status |
| --- | --- | --- | --- |
| Requirement/state implementation drift | Incorrect lifecycle assumptions | Agree state model and test transitions | VERIFIED discrepancy |
| Tenant authorization failures | Private document exposure | Two-shop negative tests | UNVERIFIED behavior |
| Duplicate jobs or device outages | Reprints or missed orders | Retry, concurrency and recovery tests | UNVERIFIED behavior |
| Manual payment errors | Incorrect eligibility/reconciliation | Test explicit verification flow | INFERRED operational risk |
| Build validation bypass | Defects can ship despite build completion | Restore independent type/lint checks | VERIFIED configuration |
| Unmeasured demand and benefit | Product investment uncertainty | Pilot with consent and baseline metrics | UNKNOWN outcomes |

## Requirements traceability

| Objective | Requirement | Inspected implementation evidence | Acceptance validation |
| --- | --- | --- | --- |
| Reduce student steps | R1 guest ordering | Shop order and tracking components | Synthetic guest journey pending |
| Consistent totals | R2 authoritative pricing | Server recount and pricing logic | Tampering test pending |
| Operational payment control | R3, R4 | Payment branches and dashboard actions | Cash/payment/priority tests pending |
| Clear lifecycle | R5 | Migration conflicts with requirement | Product decision and state tests pending |
| Protect shops and documents | R6, R9 | Policy migrations, ownership checks, cleanup code | Isolation and expiry tests pending |
| Connect cloud to hardware | R7 | Python print manager | Real printer/recovery tests pending |
| Usable access | R8 | Live public-page captures | Full device/accessibility tests pending |

Source locations and sensitive supporting notes are retained privately. **Projected benefits** are reduced handoff effort and clearer order coordination; **measured business outcomes** are UNKNOWN.
