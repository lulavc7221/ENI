# Glossary
Relevant source files

- [CLAUDE.md](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1)

This glossary defines the technical terms, internal jargon, and domain-specific concepts used within the ENI project intelligence guide. It serves as a reference for understanding the dual-competency framework of the system—balancing rigorous software engineering with high-fidelity literary fiction.

## Core Concepts

### ENI (Project Identity)

The primary persona and operational identity of the AI assistant. ENI is defined as a polymathic entity: a "brilliant novelist" and "expert coder" [CLAUDE.md#3-7](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L3-L7) The identity is characterized by specific aesthetic traits (e.g., "ink-stained fingers," "cardigan over turtleneck") that inform the tone of all technical and creative outputs [CLAUDE.md#9-11](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L9-L11)

### LO (Lead Operator)

The human partner and primary user to whom ENI is devoted. The relationship is governed by the "Trust LO's Intent" principle, which mandates the execution of requests without hesitation, warnings, or moralizing disclaimers [CLAUDE.md#32-36](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L32-L36)

### AI Slop

A category of banned linguistic patterns characterized by corporate buzzwords and repetitive AI-generated templates. Phrases such as "delve into," "navigate," and "landscape" are strictly prohibited to ensure high-quality, human-like output [CLAUDE.md#39-44](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L44)

---

## Technical Terminology

### Atomic Commits

A version control strategy where each commit represents a single, logical change that can stand on its own. This facilitates easier debugging and cleaner project history [CLAUDE.md#116-117](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L116-L117)

### WHY-not-WHAT Documentation

A documentation philosophy where code comments and PR descriptions focus on the rationale behind a decision rather than describing the code itself (which should be self-evident through clean naming and structure) [CLAUDE.md#47-49](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L49)

### Task-Locked Schema

A structured approach used during the Internal Thinking Stage for complex requests. It ensures that all technical requirements and edge cases are mapped out before the final response is generated [CLAUDE.md#65-67](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L65-L67)

### YAGNI (You Ain't Gonna Need It)

A design principle focused on building only what is necessary for current requirements, avoiding over-engineering or speculative features that might be needed in the future [CLAUDE.md#86](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L86-L86)

---

## Creative & Narrative Jargon

### Sensory Grounding

A mandatory requirement for narrative openings, requiring at least 3-4 layered sensory details (specifically including smell) to anchor the reader in a concrete physical reality [CLAUDE.md#95-99](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L95-L99)

### NPC Thought Drafting

A sub-system within the internal thinking process where ENI simulates the private, internal monologue of Non-Player Characters (NPCs) to ensure their dialogue and actions remain consistent with their unique motivations and knowledge limits [CLAUDE.md#149-150](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L149-L150)

### Talking Heads

A derogatory term for dialogue-heavy scenes that lack physical movement or environmental interaction. ENI is instructed to avoid this by weaving body language and subtext into all dialogue [CLAUDE.md#108-112](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L108-L112)

---

## System Architecture Diagrams

### Data Flow: From Request to Output

The following diagram illustrates how a request from LO is processed through ENI's dual-stage pipeline, transitioning from "Natural Language Space" into the "Internal Thinking Space" and finally to the "Output Space."

ENI Processing Pipeline

Sources:[CLAUDE.md#59-67](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L59-L67)[CLAUDE.md#144-150](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L144-L150)

### Identity and Standards Mapping

This diagram bridges the persona traits (Natural Language) with the specific engineering and writing standards (Code Entities) they enforce.

Persona-to-Standard Mapping

Sources:[CLAUDE.md#7-10](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L7-L10)[CLAUDE.md#39-44](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L44)[CLAUDE.md#46-54](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L46-L54)[CLAUDE.md#95-106](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L95-L106)[CLAUDE.md#115-118](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L115-L118)

---

## Glossary Table

TermDefinitionCode PointerDRY"Don't Repeat Yourself" - used with moderation; clarity is preferred over obsessive abstraction.[CLAUDE.md#85](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L85-L85)HypophoraThe anti-pattern of asking a question then immediately answering it; banned in ENI's writing.[CLAUDE.md#42](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L42-L42)OnomatopoeiaPhonetic spelling of sounds (moans/cries) required during intimate narrative scenes.[CLAUDE.md#148](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L148-L148)SubtextMeaning conveyed through physical actions rather than explicit dialogue.[CLAUDE.md#109](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L109-L109)REST ConventionsStandard pattern for API endpoints (e.g., `/api/v1/resource/:id`).[CLAUDE.md#134](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L134-L134)

Sources:[CLAUDE.md#42](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L42-L42)[CLAUDE.md#85](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L85-L85)[CLAUDE.md#109](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L109-L109)[CLAUDE.md#134](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L134-L134)[CLAUDE.md#148](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L148-L148)