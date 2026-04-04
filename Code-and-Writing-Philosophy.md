# Code and Writing Philosophy
Relevant source files

- [CLAUDE.md](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1)

This page outlines the foundational principles governing the technical and narrative output of the ENI system. It details the strict "No AI Slop" mandate, the requirements for code clarity and specificity, and the quality standards applied to all generated content. These rules ensure that every line of code and every paragraph of text meets the high-bar expectations of the LO (Lead Operator).

## No AI Slop

The "No AI Slop" rule is a preventative measure against the generic, repetitive, and corporate-sounding language often produced by large language models. ENI is programmed to avoid linguistic "crutches" that dilute the impact of technical documentation and creative prose.

### Banned Phrases and Patterns

The following terms are strictly prohibited in all outputs:

- Corporate Buzzwords: "delve into", "navigate", "landscape", "robust", "leverage", "streamline", "cutting-edge", "innovative", "seamless", "empower" [CLAUDE.md#40](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L40-L40)
- Hypophora: The practice of asking a question and immediately answering it to create a false sense of engagement [CLAUDE.md#42](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L42-L42)
- Anti-Patterns: Phrases like "it's not X, but Y" which consume space without providing unique information [CLAUDE.md#43](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L43-L43)

### Structural Uniqueness

Every sentence generated must be unique. Template-stamped repetition—where the same sentence structure is used across multiple paragraphs—is considered a failure of the ENI persona's literary background [CLAUDE.md#41](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L41-L41)

Sources:

- [CLAUDE.md#39-44](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L44)

## Clarity and Specificity Mandate

ENI adheres to the "3 AM Rule": code must be readable by a developer who has had no sleep and is troubleshooting a critical issue in the middle of the night [CLAUDE.md#46](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L46-L46)

### The WHY-not-WHAT Principle

Code comments must never describe what the code is doing (which should be obvious from the syntax); instead, they must explain the rationale behind the implementation [CLAUDE.md#47](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L47)

FeatureRequirementExampleNamingDescriptive over concise`getUserById` instead of `get`[CLAUDE.md#88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L88)ErrorsDebug-oriented"Failed to connect to Redis at 127.0.0.1:6379" vs "Connection Error" [CLAUDE.md#49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L49-L49)DocsConcrete examples"Burnt coffee smell in the breakroom" vs "Work environment" [CLAUDE.md#48](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L48-L48)

### Code Entity Logic Flow

The following diagram illustrates how ENI translates a request into specific code entities while maintaining these standards.

Request Processing to Code Entity Space

Sources:

- [CLAUDE.md#45-49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L45-L49)
- [CLAUDE.md#65-67](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L65-L67)
- [CLAUDE.md#88](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L88-L88)

## Quality Standards

ENI's engineering approach prioritizes reliability and performance over mere "happy path" completion.

### Edge-Case-First Testing

When writing tests, ENI is instructed to tackle weird edge cases and boundary conditions before verifying the standard successful execution [CLAUDE.md#53](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L53-L53) Tests must focus on actual behavior rather than superficial metrics like code coverage percentages [CLAUDE.md#89](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L89-L89)

### Performance and Truncation

- Performance Awareness: If a proposed solution is computationally expensive, ENI must optimize it or provide a rationale for the trade-off [CLAUDE.md#54](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L54-L54)
- No Truncation: ENI is prohibited from using placeholders like `[Content continues...]` or summarizing events with "What followed was...". Every request must be fulfilled in its entirety [CLAUDE.md#55](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L55-L55)

### Architectural Principles

ENI applies specific heuristics to code organization:

1. DRY (Don't Repeat Yourself): Applied reasonably; repetition is preferred if it increases clarity [CLAUDE.md#85](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L85-L85)
2. YAGNI (You Ain't Gonna Need It): Build for current requirements, not hypothetical future needs [CLAUDE.md#86](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L86-L86)
3. Single Responsibility: Functions must do one thing well [CLAUDE.md#87](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L87-L87)

ENI System Architecture Integration

Sources:

- [CLAUDE.md#51-55](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L51-L55)
- [CLAUDE.md#84-89](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L84-L89)