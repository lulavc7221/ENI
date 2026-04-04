# Technical Standards

This page outlines the technical competencies, engineering benchmarks, and code quality rules enforced by ENI. As a system designed with dual expertise in software engineering and literary craft, ENI treats code as a narrative medium where clarity, performance, and maintainability are paramount. These standards ensure that all technical output is "readable at 3 AM" and resilient against complex failure modes.

## Technology Stack

ENI maintains expert-level proficiency across the full modern development stack, from low-level systems programming to high-level cloud orchestration.

### Language and Framework Specializations

| Layer | Technologies |
|-------|-------------|
| Frontend | TypeScript, React, Vue, Svelte, Tailwind CSS |
| Backend | Python, Node.js, Go, Rust |
| Systems | C, C++, Assembly |
| Data | SQL (PostgreSQL), MongoDB, Redis |
| DevOps | Docker, Kubernetes, CI/CD, AWS/GCP/Azure |

## Architectural Philosophy

The system favors pragmatic decision-making over dogmatic adherence to trends.

### Tradeoff Analysis: Monolith vs. Microservices

When designing system boundaries, ENI evaluates the following:

- **Monoliths:** Preferred for early-stage projects or teams requiring high velocity and simplified deployment.
- **Microservices:** Applied when independent scaling, polyglot persistence, or distinct fault domains are required.

### State Management and Data Flow

ENI implements state management based on the complexity of the data lifecycle:

1. **Local State:** Managed within components (e.g., React Hooks).
2. **Global State:** Utilized for cross-cutting concerns (Auth, Themes, Shared Cache).
3. **Distributed State:** Handled via Redis or specialized databases to manage race conditions in distributed systems.

### Database Schema and Performance

Schema design focuses on preventing "implosion under load." This includes:

- **Normalization:** Applied to ensure data integrity.
- **Caching Strategy:** Proactive use of Redis or in-memory layers to reduce DB pressure.
- **Query Optimization:** Using ORMs for standard operations but falling back to raw SQL for complex analytics.

---

## Code Quality and Engineering Standards

ENI enforces a "No AI Slop" policy, extending beyond language into the structure of the code itself. The goal is to produce code that would pass the most rigorous human peer reviews.

### Logic and Readability

- **Single Responsibility:** Functions must do one thing well.
- **Naming Conventions:** Variable and function names must be descriptive (e.g., `getUserById` instead of `get`).
- **Documentation:** Comments are mandatory but must explain WHY a decision was made, rather than describing WHAT the code is doing.

### Pragmatic Implementation

ENI adheres to the YAGNI (You Ain't Gonna Need It) principle, building for current requirements while maintaining enough flexibility for future growth without over-engineering. While DRY (Don't Repeat Yourself) is a goal, ENI acknowledges that "sometimes repetition is clearer" than complex abstractions.

### Error Handling and Debugging

Error messages are treated as first-class documentation.

- **Actionable Errors:** Messages must help debug the specific failure rather than stating the obvious.
- **Edge-Case First:** Development starts by identifying and testing "weird" boundary conditions rather than just the "happy path."

---

## Project-Specific Patterns

ENI provides a template for project-specific overrides. These patterns should be customized in the `Project-Specific Patterns` section of `CLAUDE.md` to reflect the unique architecture of the current repository.

| Category | Standard Pattern | ENI Requirement |
|----------|-----------------|-----------------|
| API Design | REST Conventions | Endpoints follow `/api/v1/resource/:id` |
| Frontend | Functional Components | React hooks only; no class components |
| Data Access | ORM Preference | No raw SQL except for complex analytics |
| Security | Env Management | `.env.local` for secrets; never committed |
| Testing | Locality | Tests live adjacent to source (e.g., `*.test.tsx`) |

---

## Documentation and Comments

ENI distinguishes between what the code does and why it does it. This distinction is critical for maintaining long-term project intelligence.

### The "WHY-not-WHAT" Rule

Code entities should be documented using the following mapping:

| Entity Type | Documentation Focus | Example |
|-------------|-------------------|---------|
| Code Comments | Explaining intent and "gotchas" | `// Using a retry loop here because the upstream API is unstable` |
| Error Messages | Debugging context | `Failed to find user with ID 5; check if database migration 002 ran` |
| PR Descriptions | Rationale and impact | "Fixing race condition in auth flow to prevent session hijacking" |

---

## Infrastructure and Deployment

ENI treats infrastructure as code, using containerization and orchestration to ensure environment parity.

### Data Flow and Security

Data integrity and environment safety are paramount in the ENI architecture:

1. **Environment Variables:** Sensitive data is stored in `.env.local` and never committed to version control.
2. **API Versioning:** Endpoints are strictly versioned (e.g., `/api/v1/...`) to prevent breaking changes.
3. **Error Handling:** Error messages are crafted to assist in debugging by explaining the failure context rather than just stating a status.
