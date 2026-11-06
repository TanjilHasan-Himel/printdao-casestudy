# Decisions and trade-offs

The requirements establish product intent. Historical alternatives and the author's original reasoning were not independently established. Rationales below are explicitly **INFERRED / reconstructed**, not historical quotations.

| Choice | Evidence | Reconstructed rationale | Trade-off / validation needed |
| --- | --- | --- | --- |
| Guest student access | DOCUMENTED in PRD; order path observed | Reduce steps before placing an occasional order | Abuse controls and private tracking need validation |
| Server-side page counting and price calculation | VERIFIED in order source | Avoid trusting client totals | Server processing cost and malformed-document handling |
| Manual MVP payment confirmation | DOCUMENTED; payment branches observed | Accommodate existing cash and mobile-payment practices | Staff effort and reconciliation errors remain |
| Owner-controlled queue | DOCUMENTED | Reflect readiness and counter priorities | Requires clear eligibility and transition rules |
| Web platform plus Windows bridge | VERIFIED in repository structure | Connect browser ordering to local hardware | Installation, driver compatibility and outage recovery |
| Shared backend with tenant isolation | DOCUMENTED; policy files observed | Support multiple shops through one platform | Isolation must be proven with negative tests |

## Unresolved state-model decision

**VERIFIED — source comparison:** A later migration replaces separate payment/print fields with a unified order state. This conflicts with the documented independent-state principle. The original reason for this change is **UNKNOWN**. Do not present it as an approved architectural improvement without owner clarification and transition tests.
