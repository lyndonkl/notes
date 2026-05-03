---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [agent-design, LLMs, attention, exploration, structured-output, agent-communication]
aliases:
  - "Inter-agent text communication preserves productive output diversity through attention over next-token generation that structured output formats would constrain"
---

# Inter-agent text communication preserves productive output diversity through attention over next-token generation that structured output formats would constrain

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

Language models, when generating output token by token over attention across enormous parameter spaces, produce a distribution of plausible continuations rather than a single deterministic answer. Two slightly different prompts to the same model — same role, same task, slightly different framings — return meaningfully different outputs. Across a team of agents, this combinatorial spread is productive: it surfaces variation in framing, variation in emphasis, and variation in approach that a single agent or a deterministic pipeline would not produce. Clustering across these outputs lets the system identify themes that no single run would have made visible.

Forcing structured output formats — JSON, function calls, schema-bound responses — constrains this spread. The model's combinatorial freedom collapses to fit the schema, and outputs across runs become more similar to each other than they would have been in free text. This is sometimes desirable: when the consumer is a deterministic system that needs predictable fields, structure is necessary. But when the consumer is another agent or an aggregation step that benefits from variation, structure sacrifices the diversity that made parallel agent work valuable in the first place.

The implication is that the choice between text and structured output is a choice between exploration and predictability. Text preserves exploration; structured output enables reliable downstream consumption. Architectures that need both — most architectures, in practice — must layer these: agents communicate in text where exploration matters, and structuring happens at the boundary where outputs need to be machine-consumed by deterministic systems or human-presented at scale.

**Open questions:**
- How much of the diversity benefit is genuinely exploratory vs. just stochastic noise that doesn't carry useful variation? Empirically distinguishing the two is hard but consequential.
- Are there structured output formats expressive enough to preserve much of the diversity? Some structured formats (e.g., free-text fields nested in light schemas) preserve more flexibility than rigid JSON schemas.

## Links

- Context: [[text-is-poorly-suited-as-the-human-consumption-layer-for-outputs-from-many-parallel-agents-even-though-it-works-as-the-inter-agent-communication-medium|Text is poorly suited as the human-consumption layer for outputs from many parallel agents even though it works as the inter-agent communication medium]]
- Context: [[text-native-conversational-protocols-may-be-more-practical-than-activation-space-observation-for-coordinating-llm-agents|Text-native conversational protocols may be more practical than activation-space observation for coordinating LLM agents]]
- Confirms: [[language-models-are-strong-at-exploration-but-bounded-at-exploitation|Language models are strong at exploration but bounded at exploitation]]
