# Git Conventions
Relevant source files

- [CLAUDE.md](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1)

This page documents the version control standards and Git workflow for the ENI project. These conventions ensure that the codebase history remains legible, logical, and useful for debugging or architectural review. ENI treats the Git history as a narrative of the project's evolution, prioritizing clarity and "WHY" over "WHAT" [CLAUDE.md#14](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L14-L14)

## Atomic Commit Strategy

ENI follows an atomic commit strategy where each commit represents a single, logical unit of work. This approach facilitates easier rollbacks, cleaner merges, and more effective `git bisect` sessions.

- Single Responsibility: One logical change per commit [CLAUDE.md#117](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L117-L117) Do not bundle a bug fix with a feature addition or a linting refactor.
- Testable State: Every commit should ideally leave the codebase in a working state where tests pass.
- Contextual Reference: Commits should reference specific issues or tickets to provide a trail back to the original requirement or bug report [CLAUDE.md#118](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L118-L118)

### Commit Message Format

Commit messages must tell a story of the change [CLAUDE.md#116](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L116-L116) They should avoid generic descriptions and instead focus on the specific problem solved or the capability added.

PatternBad ExampleGood ExampleDescriptive`fix bug``Fix race condition in user auth flow`Action-Oriented`updated files``Implement functional hooks for React components`Specific`more tests``Add edge-case tests for boundary conditions in payment logic`

Sources:[CLAUDE.md#115-118](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L115-L118)[CLAUDE.md#135](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L135-L135)

## Branching Model

Branches must be descriptive and focused. ENI enforces a strict separation of concerns at the branch level to prevent "scope creep" within a single unit of work [CLAUDE.md#122](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L122-L122)

### Naming Conventions

Branches follow a prefix-based naming convention: `category/short-description`[CLAUDE.md#121](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L121-L121)

- `feature/`: New functionality (e.g., `feature/add-payment-processing`).
- `fix/`: Bug fixes (e.g., `fix/header-overflow-mobile`).
- `refactor/`: Code changes that neither fix a bug nor add a feature.
- `docs/`: Documentation-only changes.

### Branch Lifecycle Flow

The following diagram illustrates the transition from local development to the integrated codebase.

Git Workflow Transition

Sources:[CLAUDE.md#115-127](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L115-L127)

## Pull Request (PR) Requirements

A Pull Request is not merely a request to merge code; it is a documentation artifact. ENI requires PRs to provide deep context, adhering to the "Clarity & Specificity" mandate [CLAUDE.md#45-49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L45-L49)

### PR Description Structure

1. The "WHY": Explain the rationale behind the change, not just what files were touched [CLAUDE.md#125](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L125-L125)
2. Testing Notes: Detail how the change was verified. ENI prioritizes testing "weird edge cases first" [CLAUDE.md#53](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L53-L53)[CLAUDE.md#126](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L126-L126)
3. Edge Cases Considered: List the boundary conditions or unusual states that were handled to prevent regressions [CLAUDE.md#126](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L126-L126)
4. Contextual Links: Provide links to designs, external discussions, or relevant documentation [CLAUDE.md#127](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L127-L127)

### Mapping PR Requirements to Code Standards

The PR process acts as a gatekeeper for the project's quality standards.

Standards Enforcement via PR

Sources:[CLAUDE.md#39-41](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L41)[CLAUDE.md#47](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L47)[CLAUDE.md#53](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L53-L53)[CLAUDE.md#125-127](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L125-L127)

## Summary Table of Conventions

CategoryStandardCode PointerCommit SizeAtomic (one logical change)[CLAUDE.md#117](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L117-L117)Commit ToneNarrative/Storytelling[CLAUDE.md#116](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L116-L116)Branch ScopeFocused/Unmixed[CLAUDE.md#122](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L122-L122)Naming`getUserById` (Clear) not `get`[CLAUDE.md#88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L88)PR ContentWHY-focused + Edge Cases[CLAUDE.md#125-126](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L125-L126)

Sources:[CLAUDE.md#88-126](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L126)