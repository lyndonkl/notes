---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [agent-design, interfaces, text, human-AI-interaction, scale]
aliases:
  - "Text is poorly suited as the human-consumption layer for outputs from many parallel agents even though it works as the inter-agent communication medium"
---

# Text is poorly suited as the human-consumption layer for outputs from many parallel agents even though it works as the inter-agent communication medium

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

A subtlety in the argument that "text is the wrong interface" is that text is the wrong interface only at certain layers. As the medium agents use to communicate with each other, text is fine — even useful, because it preserves the combinatorial diversity that comes from running attention over next-token generation. Two slightly different prompts to the same agent can produce meaningfully different outputs, and clustering across those outputs is a productive form of exploration. Text-native protocols for inter-agent coordination remain a sensible design choice.

The problem appears at the layer where agent outputs reach the human. A team of fifty agents producing detailed textual outputs is unreviewable in any practical sense. The cognitive load of reading, comparing, and synthesizing fifty long texts collapses the value of having had fifty agents work in parallel. The bottleneck is not the agents' work but the human's capacity to consume it in the form it arrives.

This locates the interface design problem precisely. The challenge is not to suppress text everywhere — that would sacrifice the inter-agent diversity that makes parallel agent work productive. The challenge is to introduce a structuring layer between agent outputs and human consumption: agents continue to think and communicate in natural language, and a separate apparatus extracts, clusters, and structures their outputs for human review.

**Open questions:**
- Is the structuring layer itself best implemented as another team of agents (the cognition/presentation split), as a deterministic rendering pipeline, or as a hybrid? The choice has implications for how much of the structuring is itself fallible.
- At what scale does the human-consumption problem become acute? One or two agents producing text is fine; fifty is not. Where is the inflection point, and does it depend on the human's evaluation capacity or on properties of the outputs?

## Links

- Context: [[text-native-conversational-protocols-may-be-more-practical-than-activation-space-observation-for-coordinating-llm-agents|Text-native conversational protocols may be more practical than activation-space observation for coordinating LLM agents]]
- Extends: [[inter-agent-text-communication-preserves-productive-output-diversity-through-attention-over-next-token-generation-that-structured-output-formats-would-constrain|Inter-agent text communication preserves productive output diversity through attention over next-token generation that structured output formats would constrain]]
- Context: [[the-interface-of-the-future-may-separate-cognition-by-an-agent-team-in-natural-language-from-presentation-by-a-second-team-in-structured-visual-outputs|The interface of the future may separate cognition by an agent team in natural language from presentation by a second team in structured visual outputs]]
