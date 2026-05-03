---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [interfaces, agent-design, design-hypothesis, presentation, cognition]
aliases:
  - "The interface of the future may separate cognition by an agent team in natural language from presentation by a second team in structured visual outputs"
---

# The interface of the future may separate cognition by an agent team in natural language from presentation by a second team in structured visual outputs

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

A candidate design for the post-chatbot interface separates two layers that the chatbot conflates. The first layer is cognition: a team of agents thinks, explores, and communicates in natural language, exploiting the combinatorial diversity that text-as-medium provides. The second layer is presentation: a separate team takes the cognitive layer's outputs and structures them into visual diagrams, tables, charts, and other forms that humans can review at a glance rather than by reading.

This separation respects the architectural reality that text serves agents and structure serves humans. Forcing structure into the cognitive layer constrains the model's combinatorial power; forcing text into the presentation layer collapses the human's review capacity. Splitting the layers lets each operate in its right medium.

This is held as a design hypothesis rather than a verified pattern. The proposal is empirically testable — by building it and measuring whether the resulting interface scales the human's productive review capacity in proportion to the number of agents involved. The proposal also has open questions: whether the presentation team should itself be agentic (introducing fallibility into the visualization layer) or deterministic rendering pipelines, and how the human should communicate back into the cognitive layer to refine its work.

**Open questions:**
- Should the presentation layer be agentic (with its own diversity) or deterministic (with predictable rendering)? The choice trades off flexibility against trust in the visualization.
- How does the human direct refinement when the cognitive and presentation layers are separate? The chatbot's strength is that user redirection happens in the same medium as model output; this design loses that simplicity and needs to recover it differently.

## Links

- Extends: [[text-is-poorly-suited-as-the-human-consumption-layer-for-outputs-from-many-parallel-agents-even-though-it-works-as-the-inter-agent-communication-medium|Text is poorly suited as the human-consumption layer for outputs from many parallel agents even though it works as the inter-agent communication medium]]
- Context: [[chatbots-are-not-the-primary-interface-for-serious-ai-work-in-the-long-run-because-they-impose-high-cognitive-load-and-negate-the-combinatorial-power-of-language-models|Chatbots are not the primary interface for serious AI work in the long run because they impose high cognitive load and negate the combinatorial power of language models]]
- Context: [[traditional-click-button-uis-are-obsolete-in-the-llm-native-world-because-they-assume-reactive-interaction-patterns-that-the-new-architecture-transcends|Traditional click-button UIs are obsolete in the LLM-native world because they assume reactive interaction patterns that the new architecture transcends]]
