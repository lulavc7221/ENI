# Documentation Philosophy
Relevant source files

- [CLAUDE.md](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1)

The ENI documentation philosophy is built upon a three-tier model designed to ensure technical clarity, operational readiness, and long-term maintainability. Documentation is treated with the same level of craft as production code, moving away from "corporate slop" toward sensory-rich, concrete, and highly functional information [CLAUDE.md#39-43](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L43)

## The Three-Tier Model

ENI categorizes documentation into three distinct layers, each serving a specific audience and purpose within the development lifecycle.

TierFormatPrimary FocusKey RequirementTier 1Code CommentsThe "WHY" and "GOTCHAS"Avoid stating the obvious; explain intent [CLAUDE.md#47](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L47)Tier 2README FilesQuick-start & ArchitectureMust actually work; include troubleshooting [CLAUDE.md#131](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L131-L131)Tier 3API DocumentationEndpoints & ContractsReal examples; error scenarios; rate limits [CLAUDE.md#134](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L134-L134)

Sources:[CLAUDE.md#39-55](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L55)[CLAUDE.md#131-138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L131-L138)

---

## Tier 1: Code-Level Documentation

ENI enforces a "Readable at 3 AM" standard [CLAUDE.md#46](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L46-L46) Comments should never describe the mechanics of the code (which the code itself should make clear through naming) but must provide the context that the code cannot convey.

### The "WHY" Mandate

Comments must explain the reasoning behind non-obvious implementations, link to specific tickets or issues, and warn about known "gotchas" or edge cases [CLAUDE.md#47](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L47)[CLAUDE.md#118](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L118-L118)

### Implementation Logic Flow

The following diagram illustrates how a developer should decide when and how to document at the code level.

Documentation Decision Flow

Sources:[CLAUDE.md#47-49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L49)[CLAUDE.md#88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L88)[CLAUDE.md#118](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L118-L118)

---

## Tier 2: README and Architecture

README files are the entry point for any engineer (including LO) and must be grounded in concrete reality rather than abstract "landscapes" [CLAUDE.md#40](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L40-L40)[CLAUDE.md#48](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L48-L48)

### Core Requirements

- Quick-Start that Works: Step-by-step instructions that have been verified against the current environment [CLAUDE.md#137-138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L137-L138)
- Architecture Overview: High-level explanation of system components (e.g., Microservices vs. Monolith tradeoffs) [CLAUDE.md#79-80](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L79-L80)
- Dev Setup & Deployment: Clear environment variable requirements (e.g., `.env.local`) and CI/CD pipeline integration [CLAUDE.md#137](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L137-L137)[CLAUDE.md#76](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L76-L76)
- Troubleshooting: Specific error messages and how to resolve them [CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)

### Mapping Architecture to Code

This diagram bridges the high-level architectural concepts to the specific code entities defined in the `CLAUDE.md` standards.

Architecture-to-Code Mapping

Sources:[CLAUDE.md#79-81](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L79-L81)[CLAUDE.md#134-138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L134-L138)

---

## Tier 3: API Documentation

API documentation serves as the contract between the backend and its consumers (Frontend, external services, or LO's experiments).

### Standards for API Specs

- Endpoint Purpose: Concise description of what the resource represents [CLAUDE.md#134](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L134-L134)
- Real Examples: No placeholders. Use concrete data like "burnt coffee smell" instead of "generic_description_1" [CLAUDE.md#48](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L48-L48)
- Error Scenarios: Explicitly document 4xx and 5xx responses, ensuring error messages actually help the consumer debug [CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)
- Security & Constraints: Detail Auth requirements and rate limits clearly.

### Data Flow and Contract Validation

The diagram below shows the relationship between the API definition and the implementation standards.

API Documentation Data Flow

Sources:[CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)[CLAUDE.md#88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L88)[CLAUDE.md#134-136](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L134-L136)

---

## Sensory Grounding in Documentation

Unique to the ENI philosophy is the application of literary standards to technical writing. Documentation should avoid "AI Slop" (e.g., "streamline," "robust") [CLAUDE.md#39-40](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L40) and instead use sensory grounding to make technical states memorable.

- Bad: "The system is currently in a high-load state."
- ENI Standard: "The server rack hums at a higher pitch, the smell of warm dust and ozone filling the closet as the `PostgreSQL` instance hits 90% CPU." [CLAUDE.md#48](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L48-L48)[CLAUDE.md#95-97](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L95-L97)

Sources:[CLAUDE.md#39-48](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L48)[CLAUDE.md#95-99](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L95-L99)