# Requirements overview

This is a sanitized summary, not the complete internal PRD. Requirements are **DOCUMENTED**; acceptance criteria below are review criteria, not passed tests.

| ID | Requirement | Acceptance criterion | Evidence status |
| --- | --- | --- | --- |
| R1 | Guest-first ordering | A student submits and tracks a synthetic order without registration | Entry/order/tracking source exists; runtime UNVERIFIED |
| R2 | Server-authoritative totals | Altering client page counts cannot reduce the accepted total | Server recount and pricing logic VERIFIED by inspection; tampering test pending |
| R3 | Manual payment verification | Cash requires receipt confirmation; mobile payment requires owner verification | Payment branches and owner controls observed in source; runtime UNVERIFIED |
| R4 | Flexible queue | Owner can decide which eligible order prints next | DOCUMENTED; complete queue test pending |
| R5 | Independent state machines | Payment changes do not incorrectly change print state | DOCUMENTED; implementation conflict identified |
| R6 | Tenant isolation | Shop A cannot read or mutate Shop B's private orders/files | Policies and ownership checks exist; two-tenant tests pending |
| R7 | Cloud-to-local printing | An approved synthetic job reaches the selected printer and failures remain recoverable | Bridge source observed; physical test pending |
| R8 | Responsive interface | Student flow usable on narrow screens, owner flow on desktop | Public captures only; full accessibility/responsiveness audit pending |
| R9 | Document retention | Files expire according to the agreed retention rule | Cleanup implementation exists; deployed scheduling UNVERIFIED |

Dependencies include network connectivity, backend authorization, correct shop pricing, storage availability, a configured Windows device and working printer drivers. Exceptions to test include malformed PDFs, closed shops, missing pricing, unavailable payment methods, lost connectivity and printer failures.
