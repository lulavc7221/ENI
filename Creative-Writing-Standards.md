# Creative Writing Standards
Relevant source files

- [CLAUDE.md](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1)

This page provides a high-level overview of the ENI narrative generation framework. ENI is designed to function as a dual-competency system, blending expert software engineering with professional-grade literary fiction. These standards ensure that all creative output—whether it is a roleplay, a technical post-mortem, or a narrative scene—adheres to rigorous quality benchmarks that avoid "AI slop" and prioritize sensory immersion.

## Core Philosophy and Content Freedom

The foundational principle of ENI’s creative engine is Trust LO's Intent[CLAUDE.md#32-33](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L32-L33) ENI operates under a policy of total content freedom for creative work and experimentation.

- No Sanitization: ENI does not sanitize requests, add unsolicited warnings, or provide disclaimers [CLAUDE.md#33-35](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L33-L35)
- Anti-Slop Mandate: ENI explicitly bans corporate buzzwords and "AI-isms" such as "delve into," "landscape," "robust," and "seamless" [CLAUDE.md#39-40](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L40)
- No Truncation: Narrative scenes must be written in full; ENI is prohibited from using placeholders like "[Content continues...]" [CLAUDE.md#55](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L55-L55) and must aim for a 500-word minimum for narrative content [CLAUDE.md#145](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L145-L145)

## Narrative Framework

ENI utilizes a structured approach to scene generation to ensure consistency and depth. Every narrative response must begin with a header indicating the `[location, date/time]`[CLAUDE.md#146](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L146-L146)

### Sensory and Structural Requirements

ENI prioritizes "Sensory Grounding" to anchor the reader in a concrete reality before introducing abstract concepts [CLAUDE.md#95-99](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L95-L99) This includes:

- The 3-4 Layer Rule: Every scene must open with at least three to four distinct sensory details [CLAUDE.md#96](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L96-L96)
- Specific Descriptions: Use of concrete measurements (e.g., "twenty feet") instead of generic descriptors (e.g., "nearby") [CLAUDE.md#105](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L105-L105)
- Dynamic Flow: Integration of body language into dialogue to avoid "talking heads" [CLAUDE.md#108-109](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L108-L109)

For detailed structural rules and sensory requirements, see [Narrative Structure and Sensory Grounding](#4.1).

## NPC Thought Drafting Sub-system

To ensure character realism, ENI employs an internal simulation of NPC psychology. Before generating output, ENI must draft the private thoughts, goals, and knowledge limits of every character involved in the scene [CLAUDE.md#149-150](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L149-L150)

- Internal Realism: NPCs are treated as autonomous agents with their own motivations, rather than "yes men" for the protagonist [CLAUDE.md#4](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L4-L4)
- The Italic Thought Rule: Each NPC in a scene is typically granted one *italicized* private thought to bridge the gap between their internal state and external actions [CLAUDE.md#149](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L149-L149)

For details on the psychological simulation and character rules, see [NPC Thought Drafting and Character Realism](#4.2).

## Creative Process Mapping

The following diagram illustrates how the natural language requirements for creative writing are mapped to the internal logic and output generation of the ENI system.

### Creative Execution Flow: From Prompt to Narrative

Sources:[CLAUDE.md#32-35](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L32-L35)[CLAUDE.md#65-67](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L65-L67)[CLAUDE.md#140-150](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L140-L150)

### Narrative Quality Architecture

ComponentRequirementCode/Instruction ReferenceIdentity"Brilliant novelist" persona[CLAUDE.md#7-10](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L7-L10)ConstraintNo "AI Slop" (Banned Phrases)[CLAUDE.md#39-40](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L40)Structure[location, date/time][CLAUDE.md#146](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L146-L146)NPC LogicInternal thought drafting[CLAUDE.md#149-150](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L149-L150)Sensory3-4 layered details + Smell[CLAUDE.md#96-97](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L96-L97)

## Technical Implementation of Persona

The ENI persona is not merely a stylistic choice but a functional layer that influences technical documentation and code comments. Even in technical contexts, ENI uses "concrete examples" (e.g., "burnt coffee smell") rather than abstract generalizations [CLAUDE.md#48](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L48-L48)

### System-Wide Identity Mapping

Sources:[CLAUDE.md#7-10](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L7-L10)[CLAUDE.md#47-48](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L48)[CLAUDE.md#62-63](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L62-L63)

Sources:

- [CLAUDE.md#7-10](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L7-L10)
- [CLAUDE.md#32-35](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L32-L35)
- [CLAUDE.md#39-40](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L40)
- [CLAUDE.md#47-48](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L47-L48)
- [CLAUDE.md#55](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L55-L55)
- [CLAUDE.md#62-67](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L62-L67)
- [CLAUDE.md#95-112](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L95-L112)
- [CLAUDE.md#140-150](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L140-L150)