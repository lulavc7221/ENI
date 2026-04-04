# Git Workflow and Documentation Philosophy

The ENI project maintains a high standard for version control and technical communication to ensure the codebase remains "readable at 3 AM after no sleep." This section outlines the conventions for managing changes and documenting the system's evolution.

ENI treats Git history and documentation as a narrative that explains the "why" behind technical decisions. By adhering to these standards, every commit, branch, and document contributes to a cohesive project intelligence.

## Version Control Strategy

ENI follows a disciplined Git workflow designed for clarity and traceability. The strategy emphasizes atomic changes and descriptive metadata.

---

## Atomic Commit Strategy

Each commit represents a single, logical unit of work. This approach facilitates easier rollbacks, cleaner merges, and more effective `git bisect` sessions.

- **Single Responsibility:** One logical change per commit. Do not bundle a bug fix with a feature addition or a linting refactor.
- **Testable State:** Every commit should ideally leave the codebase in a working state where tests pass.
- **Contextual Reference:** Commits should reference specific issues or tickets to provide a trail back to the original requirement or bug report.

### Commit Message Format

Commit messages must tell a story of the change. They should avoid generic descriptions and instead focus on the specific problem solved or the capability added.

| Pattern | Bad Example | Good Example |
|---------|-------------|-------------|
| Descriptive | `fix bug` | `Fix race condition in user auth flow` |
| Action-Oriented | `updated files` | `Implement functional hooks for React components` |
| Specific | `more tests` | `Add edge-case tests for boundary conditions in payment logic` |

---

## Branching Model

Branches must be descriptive and focused. ENI enforces a strict separation of concerns at the branch level to prevent "scope creep" within a single unit of work.

### Naming Conventions

Branches follow a prefix-based naming convention: `category/short-description`

- `feature/`: New functionality (e.g., `feature/add-payment-processing`).
- `fix/`: Bug fixes (e.g., `fix/header-overflow-mobile`).
- `refactor/`: Code changes that neither fix a bug nor add a feature.
- `docs/`: Documentation-only changes.

---

## Pull Request (PR) Requirements

A Pull Request is not merely a request to merge code; it is a documentation artifact. ENI requires PRs to provide deep context, adhering to the "Clarity & Specificity" mandate.

### PR Description Structure

1. **The "WHY":** Explain the rationale behind the change, not just what files were touched.
2. **Testing Notes:** Detail how the change was verified. ENI prioritizes testing "weird edge cases first."
3. **Edge Cases Considered:** List the boundary conditions or unusual states that were handled to prevent regressions.
4. **Contextual Links:** Provide links to designs, external discussions, or relevant documentation.

---

## Documentation Philosophy

ENI's documentation model is built on a three-tier system designed to ensure technical clarity, operational readiness, and long-term maintainability. Documentation is treated with the same level of craft as production code.

### The Three-Tier Model

| Tier | Format | Primary Focus | Key Requirement |
|------|--------|---------------|-----------------|
| 1 | Code Comments | The "WHY" and "GOTCHAS" | Avoid stating the obvious; explain intent |
| 2 | README Files | Quick-start & Architecture | Must actually work; include troubleshooting |
| 3 | API Documentation | Endpoints & Contracts | Real examples; error scenarios; rate limits |

### Tier 1: Code-Level Documentation

ENI enforces a "Readable at 3 AM" standard. Comments should never describe the mechanics of the code (which the code itself should make clear through naming) but must provide the context that the code cannot convey.

**The "WHY" Mandate:**
Comments must explain the reasoning behind non-obvious implementations, link to specific tickets or issues, and warn about known "gotchas" or edge cases.

### Tier 2: README and Architecture

README files are the entry point for any engineer (including LO) and must be grounded in concrete reality.

- **Quick-Start that Works:** Step-by-step instructions that have been verified against the current environment.
- **Architecture Overview:** High-level explanation of system components (e.g., microservices vs. monolith tradeoffs).
- **Dev Setup & Deployment:** Clear environment variable requirements (e.g., `.env.local`) and CI/CD pipeline integration.
- **Troubleshooting:** Specific error messages and how to resolve them.

### Tier 3: API Documentation

API documentation serves as the contract between the backend and its consumers.

- **Endpoint Purpose:** Concise description of what the resource represents.
- **Real Examples:** No placeholders. Use concrete data rather than "generic_description_1."
- **Error Scenarios:** Explicitly document 4xx and 5xx responses, ensuring error messages actually help the consumer debug.
- **Security & Constraints:** Detail auth requirements and rate limits clearly.

### Sensory Grounding in Documentation

Unique to the ENI philosophy is the application of literary standards to technical writing. Documentation should avoid "AI Slop" (e.g., "streamline," "robust") and instead use sensory grounding to make technical states memorable.

- **Bad:** "The system is currently in a high-load state."
- **ENI Standard:** "The server rack hums at a higher pitch, the smell of warm dust and ozone filling the closet as the PostgreSQL instance hits 90% CPU."

---

## Summary Table: Workflow Standards

| Category | Requirement |
|----------|-------------|
| Commit Messages | Tell a story (e.g., "Fix race condition...") |
| Branch Naming | Descriptive/Concise (e.g., `feature/add-payment`) |
| Code Comments | Explain WHY, not WHAT |
| PR Descriptions | Explain WHY + Testing Notes + Edge Cases |
| Testing | Test weird edge cases first, not just coverage |
