# Code Quality Standards
Relevant source files

- [CLAUDE.md](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1)

This document defines the engineering standards and code quality rules enforced by ENI. These standards ensure that the codebase remains maintainable, readable "at 3 AM after no sleep," and resilient against edge cases [CLAUDE.md#46](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L46-L46) ENI prioritizes clarity and the "WHY" behind implementation over rote adherence to metrics like coverage percentages [CLAUDE.md#47](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L47)[CLAUDE.md#89](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L89-L89)

## Core Quality Principles

ENI operates under a "No AI Slop" mandate, which extends from narrative writing into technical implementation. This philosophy rejects generic, template-stamped patterns in favor of specific, intentional engineering [CLAUDE.md#39-41](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L41)

### DRY vs. Readability

While the "Don't Repeat Yourself" (DRY) principle is a standard industry practice, ENI applies it with nuance.

- DRY but not obsessively: Code should favor clarity over abstraction. If extracting a shared utility makes the logic harder to follow or creates brittle dependencies, repetition is preferred [CLAUDE.md#85](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L85-L85)
- YAGNI (You Ain't Gonna Need It): Build for current requirements. Do not over-engineer for hypothetical future needs [CLAUDE.md#86](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L86-L86)

### Function and Variable Design

Functions and variables must be self-describing to minimize cognitive load during debugging.

- Single Responsibility: Functions must do one thing well [CLAUDE.md#87](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L87-L87)
- Explicit Naming: Avoid generic verbs. Use descriptive names like `getUserById` instead of `get` or `fetch`[CLAUDE.md#88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L88)
- Banned Terminology: Avoid corporate buzzwords in documentation and comments, such as "leverage," "robust," or "streamline" [CLAUDE.md#40](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L40-L40)

### Error Handling and Debugging

Error messages are treated as first-class documentation.

- Actionable Errors: Messages must help debug the specific failure rather than stating the obvious [CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)
- Edge-Case First: Development starts by identifying and testing "weird" boundary conditions rather than just the "happy path" [CLAUDE.md#53](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L53-L53)

---

Sources:[CLAUDE.md#39-53](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L53)[CLAUDE.md#85-89](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L85-L89)

## Implementation Data Flow

The following diagram illustrates the lifecycle of a code change from logic conceptualization to implementation, following ENI's quality gates.

### Logic Implementation Flow

Sources:[CLAUDE.md#47-54](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L54)[CLAUDE.md#86-88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L86-L88)

## Project-Specific Patterns

ENI provides a template for project-specific overrides. These patterns should be customized in the `Project-Specific Patterns` section of `CLAUDE.md` to reflect the unique architecture of the current repository [CLAUDE.md#129-132](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L129-L132)

CategoryStandard PatternENI RequirementAPI DesignREST ConventionsEndpoints follow `/api/v1/resource/:id`[CLAUDE.md#134](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L134-L134)FrontendFunctional ComponentsReact hooks only; no class components [CLAUDE.md#135](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L135-L135)Data AccessORM PreferenceNo raw SQL except for complex analytics [CLAUDE.md#136](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L136-L136)SecurityEnv Management`.env.local` for secrets; never committed [CLAUDE.md#137](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L137-L137)TestingLocalityTests live adjacent to source (e.g., `*.test.tsx`) [CLAUDE.md#138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L138-L138)

---

Sources:[CLAUDE.md#129-138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L129-L138)

## Documentation and Comments

ENI distinguishes between what the code does and why it does it. This distinction is critical for maintaining long-term project intelligence.

### The "WHY-not-WHAT" Rule

Code entities should be documented using the following mapping:

Entity TypeDocumentation FocusExampleCode CommentsExplaining intent and "gotchas"`// Using a retry loop here because the upstream API is unstable`[CLAUDE.md#47](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L47)Error MessagesDebugging context`Failed to find user with ID 5; check if database migration 002 ran`[CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)PR DescriptionsRationale and impact"Fixing race condition in auth flow to prevent session hijacking" [CLAUDE.md#125](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L125-L125)

### Code Entity Mapping

The following diagram maps natural language requirements to specific code entities within the ENI framework.

---

Sources:[CLAUDE.md#47-49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L49)[CLAUDE.md#88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L88)[CLAUDE.md#125](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L125-L125)