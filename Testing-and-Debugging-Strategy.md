# Testing and Debugging Strategy
Relevant source files

- [CLAUDE.md](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1)

This page outlines the ENI project's rigorous approach to software reliability. ENI prioritizes deep technical investigation over superficial metrics, focusing on the resilience of the system under stress and the clarity of the debugging process.

## Testing Philosophy

ENI’s testing philosophy is rooted in behavior over coverage. The goal is not to achieve a specific percentage of line coverage but to ensure the system handles reality—especially the parts of reality that are inconvenient or "weird" [CLAUDE.md#53](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L53-L53)

### What to Test: Edge-Case-First

ENI follows an "Edge-Case-First" mandate. While "happy paths" are necessary, they are often the least informative tests. Testing efforts are concentrated on:

- Boundary Conditions: Values at the extreme limits of allowed ranges.
- Weird Edge Cases: Unexpected user inputs, race conditions, and distributed systems failures [CLAUDE.md#53](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L53-L53)[CLAUDE.md#82](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L82-L82)
- Behavioral Integrity: Tests must validate that the code does what it is supposed to do for the user, rather than simply confirming that the code executes [CLAUDE.md#89](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L89-L89)

### What Not to Test

To maintain velocity and focus on high-value code, ENI avoids testing:

- Framework Internals: Trusting that third-party libraries (e.g., React, FastAPI) function as documented.
- Trivial Getters/Setters: If a function merely returns a property, it does not require a dedicated test.
- Coverage for Coverage's Sake: High coverage percentages can mask poor test quality. ENI prefers 60% coverage of critical logic over 100% coverage of boilerplate [CLAUDE.md#89](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L89-L89)

### Implementation Pattern

Tests are co-located with the source code to ensure they are updated alongside feature changes [CLAUDE.md#138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L138-L138)

AspectENI StandardLocationAdjacent to source (e.g., `component.tsx` and `component.test.tsx`) [CLAUDE.md#138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L138-L138)FocusWHY and HOW the system breaks [CLAUDE.md#53](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L53-L53)NamingDescriptive of the scenario being tested [CLAUDE.md#88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L88)

Sources:[CLAUDE.md#53](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L53-L53)[CLAUDE.md#82](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L82-L82)[CLAUDE.md#89](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L89-L89)[CLAUDE.md#138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L138-L138)

---

## Debugging Strategy

Debugging in ENI is a disciplined, five-step process designed to move from ambiguity to resolution without "guess-and-check" programming.

### The Five-Step Approach

1. Reproduce: Create a minimal, isolated environment where the bug consistently occurs.
2. Read Errors: Analyze the stack trace and error messages. ENI mandates that error messages must actually aid debugging rather than stating the obvious [CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)
3. Check the Obvious: Verify environment variables, network connectivity, and recent commits.
4. Binary Search: Isolate the fault by bisecting the code or the git history to find the exact point of failure.
5. Rubber Duck: Explain the logic out loud (or in internal thinking) to identify flaws in the mental model [CLAUDE.md#65-66](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L65-L66)

### Data Flow and Debugging Points

The following diagram illustrates how ENI approaches the debugging of a standard request flow, mapping natural language concepts to code entities.

Request-to-Resolution Debugging Flow

Sources:[CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)[CLAUDE.md#65-66](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L65-L66)[CLAUDE.md#116-117](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L116-L117)[CLAUDE.md#134](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L134-L134)[CLAUDE.md#138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L138-L138)

---

## Technical Standards for Reliability

ENI applies specific engineering patterns to minimize the need for debugging and maximize testability.

### Code Quality as Prevention

- Single Responsibility: Functions must do one thing well, making them easier to isolate and test [CLAUDE.md#87](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L87-L87)
- Clear Naming: Variables and functions must be descriptive (e.g., `getUserById` instead of `get`) to prevent logic errors during development [CLAUDE.md#88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L88)
- Performance Awareness: If a system is slow, it is treated as a bug that requires optimization [CLAUDE.md#54](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L54-L54)

### Error Message Standards

Generic error messages are forbidden. Every error caught by the system should provide context that answers "What happened?" and "Where did it happen?" [CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)

Mapping Strategy to Code Entities

Sources:[CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)[CLAUDE.md#54](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L54-L54)[CLAUDE.md#86-88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L86-L88)[CLAUDE.md#117](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L117-L117)[CLAUDE.md#138](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L138-L138)