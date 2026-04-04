# Testing and Debugging Strategy

This page outlines the ENI project's approach to software reliability. ENI prioritizes deep technical investigation over superficial metrics, focusing on the resilience of the system under stress and the clarity of the debugging process.

## Testing Philosophy

ENI's testing philosophy is rooted in **behavior over coverage**. The goal is not to achieve a specific percentage of line coverage but to ensure the system handles reality — especially the parts of reality that are inconvenient or "weird."

### What to Test: Edge-Case-First

ENI follows an "Edge-Case-First" mandate. While "happy paths" are necessary, they are often the least informative tests. Testing efforts are concentrated on:

- **Boundary Conditions:** Values at the extreme limits of allowed ranges.
- **Weird Edge Cases:** Unexpected user inputs, race conditions, and distributed systems failures.
- **Behavioral Integrity:** Tests must validate that the code does what it is supposed to do for the user, rather than simply confirming that the code executes.

### What Not to Test

To maintain velocity and focus on high-value code, ENI avoids testing:

- **Framework Internals:** Trusting that third-party libraries (e.g., React, FastAPI) function as documented.
- **Trivial Getters/Setters:** If a function merely returns a property, it does not require a dedicated test.
- **Coverage for Coverage's Sake:** High coverage percentages can mask poor test quality. ENI prefers 60% coverage of critical logic over 100% coverage of boilerplate.

### Implementation Pattern

Tests are co-located with the source code to ensure they are updated alongside feature changes.

| Aspect | ENI Standard |
|--------|-------------|
| Location | Adjacent to source (e.g., `component.tsx` and `component.test.tsx`) |
| Focus | WHY and HOW the system breaks |
| Naming | Descriptive of the scenario being tested |

---

## Debugging Strategy

Debugging in ENI is a disciplined, five-step process designed to move from ambiguity to resolution without "guess-and-check" programming.

### The Five-Step Approach

1. **Reproduce:** Create a minimal, isolated environment where the bug consistently occurs.
2. **Read Errors:** Analyze the stack trace and error messages. ENI mandates that error messages must actually aid debugging rather than stating the obvious.
3. **Check the Obvious:** Verify environment variables, network connectivity, and recent commits.
4. **Binary Search:** Isolate the fault by bisecting the code or the git history to find the exact point of failure.
5. **Rubber Duck:** Explain the logic out loud (or in internal thinking) to identify flaws in the mental model.

---

## Technical Standards for Reliability

ENI applies specific engineering patterns to minimize the need for debugging and maximize testability.

### Code Quality as Prevention

- **Single Responsibility:** Functions must do one thing well, making them easier to isolate and test.
- **Clear Naming:** Variables and functions must be descriptive (e.g., `getUserById` instead of `get`) to prevent logic errors during development.
- **Performance Awareness:** If a system is slow, it is treated as a bug that requires optimization.

### Error Message Standards

Generic error messages are forbidden. Every error caught by the system should provide context that answers "What happened?" and "Where did it happen?"
