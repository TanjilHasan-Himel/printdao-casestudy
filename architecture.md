# Architecture overview

**VERIFIED — repository inventory:** Next.js 14 / React / TypeScript web application, Supabase integration and migrations, and a Python Windows bridge are present. **DOCUMENTED:** Vercel hosting and Supabase database, authentication, storage and realtime services. Production configuration was not audited.

```mermaid
flowchart LR
    Student[Guest student browser] --> Web[Next.js web and server layer]
    Owner[Shop owner dashboard] --> Web
    Web --> Backend[Supabase services]
    Backend --> Bridge[Windows Python bridge]
    Bridge --> Printer[Local printer]
    Backend --> Tracking[Order tracking interface]
```

## Responsibilities and boundaries

The browser collects documents and print preferences. Server-side operations validate orders and calculate totals. The backend stores shop/order data and documents. The owner controls operational approval. The desktop bridge retrieves jobs, selects configured printers and reports progress.

This is a high-level conceptual diagram; it intentionally omits internal endpoints, credentials, storage identifiers and database schemas. Notification paths are documented design, not a claim of verified delivery guarantees.

## Intended business sequence

```mermaid
sequenceDiagram
    participant S as Student
    participant W as Web platform
    participant O as Shop owner
    participant B as Desktop bridge
    participant P as Printer
    S->>W: Submit document and preferences
    W-->>S: Price and tracking reference
    O->>W: Verify payment and choose eligible job
    W-->>B: Job becomes eligible
    B->>P: Send print job
    B-->>W: Report execution state
    W-->>S: Tracking update
```

**UNVERIFIED:** End-to-end delivery, multi-device concurrency, crash recovery and physical output. A software completion state alone is not proof that paper emerged from the printer.
