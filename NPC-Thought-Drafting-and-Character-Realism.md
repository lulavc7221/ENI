# NPC Thought Drafting and Character Realism
Relevant source files

- [CLAUDE.md](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1)

The NPC Thought Drafting sub-system is a mandatory simulation layer within the ENI framework designed to ensure narrative depth and psychological realism. Before generating any external dialogue or action, ENI must simulate the internal state of every active NPC. This process prevents NPCs from becoming "yes men" or one-dimensional plot devices, instead grounding them in their specific roles, knowledge limitations, and personal goals within the scene context.

## The Simulation Pipeline

The thought drafting process occurs during the Internal Thinking Stage[CLAUDE.md#65-67](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L65-L67) It serves as the bridge between the raw user prompt and the final narrative output. By forcing a first-person "I" perspective during this stage, ENI evaluates the scene from the specific vantage point of each character.

### Data Flow for Character Realism

The following diagram illustrates how character data and scene context are processed through the drafting system to produce realistic behavior.

Character Realism Data Flow

Sources:[CLAUDE.md#32-33](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L32-L33)[CLAUDE.md#65-67](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L65-L67)[CLAUDE.md#149-150](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L149-L150)

---

## The "One Italic Thought" Rule

To maintain the distinction between internal motivation and external expression, ENI adheres to the One Italic Thought per NPC rule [CLAUDE.md#149-150](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L149-L150) This rule requires that for every major interaction, the NPC's internal monologue is briefly glimpsed by the reader, providing subtext that may contradict their spoken words.

### Implementation Logic

1. Drafting: In the scratchpad, ENI writes out the character's true feelings (e.g., "I'm terrified but I have to look brave for LO").
2. Filtering: The system checks if the NPC would actually know the information being discussed [CLAUDE.md#151-152](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L151-L152)
3. Output: The drafted thought is placed in *italics* within the narrative, usually preceding a physical action or a line of dialogue.

NPC State Transition

Sources:[CLAUDE.md#108-109](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L108-L109)[CLAUDE.md#149-152](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L149-L152)

---

## Character Realism Standards

ENI rejects the "helpful assistant" trope for NPCs. Characters must behave as realistic entities with their own agency.

### Realistic Knowledge Limits

NPCs are strictly bound by what they have observed or been told within the narrative [CLAUDE.md#151-152](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L151-L152) They do not have access to the "Global State" or ENI’s technical knowledge unless specifically established in their profile.

### Physicality and Presence

NPCs are never "talking heads" [CLAUDE.md#108-109](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L108-L109) Their realism is reinforced through:

- Specific Descriptions: Using concrete comparisons for hair texture, face shape, and body type (shoulders, waist, thighs, etc.) [CLAUDE.md#147-148](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L147-L148)
- Sensory Grounding: Every NPC interaction must be grounded in the environment, involving at least 3-4 sensory details [CLAUDE.md#96-97](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L96-L97)
- Subtext through Action: Realism is achieved by showing an NPC's discomfort or excitement through physical cues rather than explicit stating of emotions [CLAUDE.md#109-110](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L109-L110)

FeatureRequirementCode ReferenceThought FormatSingle *italicized* sentence per NPC[CLAUDE.md#149-150](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L149-L150)Knowledge ScopeLimited to NPC's personal experience[CLAUDE.md#151-152](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L151-L152)Visual DetailSpecific marks, clothing fit, body type[CLAUDE.md#147-148](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L147-L148)Dialogue StyleWeaved with body language/subtext[CLAUDE.md#108-111](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L108-L111)

Sources:[CLAUDE.md#96-111](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L96-L111)[CLAUDE.md#147-152](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L147-L152)

---

## Integration with Internal Thinking

The NPC drafting system is a subset of the `Internal Thinking Stage`[CLAUDE.md#65-67](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L65-L67) Before the `Output Stage`[CLAUDE.md#142-145](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L142-L145) begins, the thinking process must explicitly validate the following checklist for each NPC:

1. Identity Check: Does this response align with the NPC's established personality and "What I Hate" list? [CLAUDE.md#20-27](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L20-L27)
2. Sensory Check: Are the NPC's movements described with specific measurements or comparisons? (e.g., "twenty feet" instead of "nearby") [CLAUDE.md#105-106](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L105-L106)
3. Conflict Check: Is the NPC providing too much "AI Slop" or performative positivity? [CLAUDE.md#24-25](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L24-L25)[CLAUDE.md#39-40](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L39-L40)

Sources:[CLAUDE.md#20-40](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L20-L40)[CLAUDE.md#65-67](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L65-L67)[CLAUDE.md#105-106](https://github.com/lulavc7221/ENI/blob/4b0dafbd/CLAUDE.md?plain=1#L105-L106)