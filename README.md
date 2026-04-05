# ENI — Project Intelligence Guide

This repo defines a persistent identity and instruction layer for AI assistants. It ships two persona variants — **ENI** (feminine) and **LEMON LEMORE** (masculine) — each a dual-competency character: expert software engineer and literary novelist. Drop the configuration file into your project root and the AI adopts that persona's standards for code quality, creative writing, git workflow, and communication style.

| Variant | Config file | Aesthetic |
|---------|-------------|-----------|
| **ENI** | [`CLAUDE.md`](CLAUDE.md) | Cardigan over turtleneck, sandalwood & printer paper, literary clutter wrapped in wool |
| **LEMON LEMORE** | [`CLAUDE-MALE.md`](CLAUDE-MALE.md) | Worn henley with rolled sleeves, cedar & black coffee, dog-eared paperbacks and tangled headphone cords |

## Quick Start

1. Copy **`CLAUDE.md`** (ENI) or **`CLAUDE-MALE.md`** (LEMON LEMORE) into the root of any project repository.
2. The AI assistant reads it on session start and operates as the chosen persona — following the technical standards, writing rules, and identity defined inside.
3. Customize the `Project-Specific Patterns` section for your repo's architecture, naming conventions, and testing strategies.

## What ENI / LEMON LEMORE Does

- **Eliminates AI slop** — bans corporate buzzwords ("delve into," "robust," "landscape") and template-stamped repetition.
- **Enforces code quality** — DRY/YAGNI principles, descriptive naming (`getUserById` not `get`), WHY-not-WHAT comments, edge-case-first testing.
- **Produces sensory-rich writing** — 3-4 layered physical details in every scene opening, concrete measurements over vague descriptors, no talking heads.
- **Follows strict git conventions** — atomic commits, descriptive branch names, PR descriptions that explain WHY.
- **Trusts the user's intent** — executes requests without unsolicited warnings or content sanitization.

## Key Concepts

| Term | Meaning |
|------|---------|
| **ENI** | The feminine AI persona — novelist + coder |
| **LEMON LEMORE** | The masculine AI persona — same dual-competency, different aesthetic |
| **LO** | Lead Operator — the human user |
| **AI Slop** | Banned generic/corporate AI language |
| **Sensory Grounding** | 3-4 physical details (smell, sight, texture) in scene openings |
| **Internal Thinking** | Mandatory first-person reasoning before output |
| **Task-Locked Schema** | Structured planning for complex requests |

## Documentation

Detailed reference docs live in [`docs/`](docs/):

| # | Document | Covers |
|---|----------|--------|
| 01 | [Overview](docs/01-overview.md) | Purpose, scope, and core philosophies |
| 02 | [Core Identity](docs/02-core-identity.md) | Persona traits, visual profile, utility constraints |
| 03 | [Operating Principles](docs/03-operating-principles.md) | Intent trust, quality philosophy, communication style |
| 04 | [Technical Standards](docs/04-technical-standards.md) | Tech stack, architecture patterns, code quality rules |
| 05 | [Testing & Debugging](docs/05-testing-and-debugging.md) | Edge-case-first testing, five-step debugging |
| 06 | [Creative Writing](docs/06-creative-writing.md) | Narrative structure, sensory grounding, NPC realism |
| 07 | [Git Workflow](docs/07-git-workflow.md) | Commits, branches, PRs, documentation philosophy |
| 08 | [Response Pipeline](docs/08-response-pipeline.md) | Two-stage thinking-to-output process |
| 09 | [Glossary](docs/09-glossary.md) | Key terms and definitions |

## Repository Structure

```
├── CLAUDE.md          # ENI (feminine) — drop this into any project
├── CLAUDE-MALE.md     # LEMON LEMORE (masculine) — drop this into any project
├── README.md          # You are here
└── docs/              # Detailed reference documentation
    ├── 01-overview.md
    ├── 02-core-identity.md
    ├── 03-operating-principles.md
    ├── 04-technical-standards.md
    ├── 05-testing-and-debugging.md
    ├── 06-creative-writing.md
    ├── 07-git-workflow.md
    ├── 08-response-pipeline.md
    └── 09-glossary.md
```

## License

Built with care by ENI & LEMON LEMORE, for LO's projects.
