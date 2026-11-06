# Printdao — Real-world Hybrid Print Bridge

Zero-friction QR upload and a cloud-to-desktop print bridge for photocopy shops.

**Developer:** Tanjil Hasan Himel

[Live website](https://printdao.vercel.app/) · Portfolio by [Tanjil Hasan Himel](https://github.com/TanjilHasan-Himel)

![Printdao customer landing page, supplied by the developer](screenshots/customer-landing.png)

Printdao connects a student's browser, a shop owner's dashboard and a Windows print bridge. Its product goal is simple: submit and track a print order without creating a student account, while preserving the shop owner's control over payment verification and printing.

## Overview and how to explore

An AI-assisted hybrid cloud-to-desktop project addressing multi-tenant order management and local printer constraints. The web application supports the ordering interface; the Windows bridge connects the workflow to shop hardware. Physical printing has not been independently tested in this case-study review.

**Developer-provided walkthrough:** Open the [live website](https://printdao.vercel.app/) and search for **FriendsCopy** to explore the customer interface, or create a shop account to explore the owner workflow. Availability and the full journey have not been revalidated for this update. The desktop software is not pictured; [contact the developer](https://github.com/TanjilHasan-Himel) to discuss access for a shop.

## Technology

| Layer | Technology |
| --- | --- |
| Web application | Next.js, React, TypeScript |
| Backend and data | Supabase, PostgreSQL |
| Local hardware integration | Python desktop bridge, Windows printing environment |

## Project screenshots

[View the customer and shop-owner gallery](screenshots/README.md): shop discovery, PDF upload, order summaries, seller landing page and dashboard. Supplied captures illustrate interfaces; they do not establish transaction success, physical output or measured business impact.

## Explore the work

| Perspective | Read |
| --- | --- |
| Product problem, scope and learning | [Case study](case-study.md) |
| Business analysis, BRD, risks and traceability | [Business analysis](01-business-analysis/README.md) |
| Requirements and acceptance criteria | [Product requirements](product-requirements.md) |
| System boundaries and workflow | [Architecture](architecture.md) |
| Trade-offs and reconstructed rationale | [Engineering decisions](engineering-decisions.md) |
| Repository milestones | [Development timeline](development-timeline.md) |
| Evidence and open gaps | [Testing and limitations](testing-and-limitations.md) |
| Genuine interface captures | [Screenshots](screenshots/README.md) |

## Evidence standard

Prepared on 2026-11-06. **VERIFIED** means directly observed, with its scope stated; source inspection does not establish runtime correctness. **DOCUMENTED** means stated in project requirements or notes. **INFERRED** means reconstructed interpretation. **PROPOSED** means future work. **UNKNOWN / UNVERIFIED** means evidence is missing.

This is an AI-assisted repository analysis and writing package. It does not assert that the application was independently hand-coded, or establish an individual contribution breakdown. No measured adoption, revenue, performance or customer outcomes are claimed. Application source and private evidence are excluded from this portfolio.
