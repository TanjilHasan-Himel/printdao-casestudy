# Product case study

## Problem and target users

**DOCUMENTED:** The PRD targets university-area print shops in Bangladesh. It describes document handoff through messaging apps or flash drives, manual page counting and price calculation, payment checks, queue confusion and repeated counter conversations. These are the project's problem statements, not independently validated interview findings.

**DOCUMENTED:** Primary actors are guest students and shop owners. A local Windows computer connects the digital workflow to physical printing. Shop staff are a plausible additional operational stakeholder (**INFERRED**); distinct staff roles have not been validated here.

## Product response

The intended student journey is scan/open shop → upload → configure → view price → choose payment → submit → track → collect. The owner's journey is configure shop → review orders → verify payment → decide priority → trigger printing → complete.

**VERIFIED — source inspection:** Order submission recalculates page counts, loads shop pricing and checks payment-method ownership. Dashboard order actions and a Python print manager exist. **UNVERIFIED:** Successful end-to-end ordering, payment handling and physical printing in production.

## Scope and prioritization

**DOCUMENTED:** Guest ordering, shop setup, order management, manual cash/mobile-payment verification and a Windows bridge form the product's MVP direction. Advanced CRM, CMS, administration and payment integrations are future goals in project guidance. Inclusion in a planning document does not prove implementation.

**INFERRED — reconstructed rationale:** Guest access removes an onboarding step for occasional print customers. Manual payment confirmation fits the operator-controlled queue but retains staff work. A local bridge addresses hardware access while adding installation and recovery responsibilities.

## Outcomes and learning

**VERIFIED — browser observation:** The public landing page and login interface rendered during this review. Screenshots document presentation only. **UNKNOWN:** Paying customers, print volume, conversion, time saved, uptime, revenue and printer reliability.

The main engineering learning from this review is that planning, implementation and deployed behavior require separate evidence. The PRD requires independent payment and printing states, while a later migration combines them. That discrepancy needs a product decision and validation before full PRD compliance can be claimed.

**PROPOSED next validation:** Exercise a synthetic guest order in an isolated demo shop; test cash approval and retry behavior; verify tenant isolation with two test shops; observe a physical printer; then measure order completion time and operator effort against a documented baseline.
