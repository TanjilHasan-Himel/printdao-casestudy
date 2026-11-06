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

### Developer reflection: working with AI

**DOCUMENTED — developer's account, supplied for this case study:** Tanjil Hasan Himel describes taking AI-generated code toward a hybrid cloud-to-desktop product. Working from a strict PRD, he found that the agent tended toward happy-path CRUD implementations and needed explicit requirements for local background processing, hardware constraints and lifecycle handling. He reports using direct feedback and migrations to address state-model problems.

This records the developer's experience, rather than a general claim about every AI tool. The assertion that state corruption was fully solved is not independently verified: the inspected migration still conflicts with the PRD's independent payment/printing requirement. That limitation remains open below.

### Visible product capabilities

Developer-supplied screenshots show customer shop discovery, PDF upload, populated and empty order summaries, owner onboarding messaging and an owner dashboard. The dashboard capture displays zero values; it is not an adoption or revenue metric. [Browse the annotated gallery](screenshots/README.md).

### Impact evidence

The intended benefit is less document-handoff effort and clearer coordination between students, shop staff and printers. No measured impact metric was supplied. Hybrid deployment is an architectural characteristic, not a business outcome.

**VERIFIED — browser observation:** The public landing page and login interface rendered during this review. Screenshots document presentation only. **UNKNOWN:** Paying customers, print volume, conversion, time saved, uptime, revenue and printer reliability.

The main engineering learning from this review is that planning, implementation and deployed behavior require separate evidence. The PRD requires independent payment and printing states, while a later migration combines them. That discrepancy needs a product decision and validation before full PRD compliance can be claimed.

**PROPOSED next validation:** Exercise a synthetic guest order in an isolated demo shop; test cash approval and retry behavior; verify tenant isolation with two test shops; observe a physical printer; then measure order completion time and operator effort against a documented baseline.
