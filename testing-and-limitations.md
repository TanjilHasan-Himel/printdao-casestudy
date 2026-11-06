# Testing and limitations

## Observed in this review

| Check | Result | What it establishes |
| --- | --- | --- |
| Repository structure and dependency inspection | VERIFIED | Web, backend integration and bridge artifacts exist |
| Server order processing inspection | VERIFIED | Recount and pricing checks exist in the inspected source |
| PRD versus state migration comparison | VERIFIED discrepancy | Separate-state requirement and unified migration disagree |
| Build configuration inspection | VERIFIED | Production build configuration bypasses TypeScript and ESLint failures |
| Public landing/login browser capture | VERIFIED rendering only | Public interfaces rendered without authentication |
| Narrow login viewport | VERIFIED visual limitation | Right-side content is clipped in the captured browser window; mobile-device behavior needs separate testing |
| Additional developer-supplied screenshots | VERIFIED visual inspection only | Customer, discovery and seller interfaces are visible; capture dates, environment and end-to-end behavior are not independently established |

No application test command is declared in the inspected web package. No application test suite was executed in this review. Passing a deployment build would not establish a clean type/lint result with the current bypass configuration.

## Not verified

Guest submission, payment reconciliation, document access isolation, deployed RLS, retention jobs, load handling, accessibility, multi-device behavior, retries, physical printing and disaster recovery were not tested. No customer accounts, uploads, transactions or printer jobs were created for this review.

## Proposed acceptance run

Use two isolated demo shops and synthetic PDFs. Check guest ordering, invalid files, client-total tampering, cash and manual-payment approval, cross-shop read/write denial, offline bridge recovery, duplicate events, cancellation, printer failure and physical output. Record actual results and timestamps before upgrading any runtime claim to VERIFIED.

No business outcome measurements or security certification are claimed. Visual evidence is limited to the public pages in the screenshot index.
