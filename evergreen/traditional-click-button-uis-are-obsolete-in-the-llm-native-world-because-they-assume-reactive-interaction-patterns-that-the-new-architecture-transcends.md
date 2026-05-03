---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [interfaces, UI-design, LLM-native, design-philosophy, reactive-vs-proactive]
aliases:
  - "Traditional click-button UIs are obsolete in the LLM-native world because they assume reactive interaction patterns that the new architecture transcends"
---

# Traditional click-button UIs are obsolete in the LLM-native world because they assume reactive interaction patterns that the new architecture transcends

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

Traditional graphical user interfaces — buttons, menus, forms, dropdowns — are designed around a specific interaction pattern: the user holds the initiative, the system presents a fixed set of possible actions, and the user selects from them. This pattern made sense when systems lacked the capacity to maintain rolling context, infer what action would be useful, or generate appropriate next steps without explicit instruction. The button-based UI was the right interface for the reactive machine.

Language-model-backed systems have those capacities. A system that maintains context about its user, infers what action would be useful, and initiates appropriately doesn't need to surface a fixed menu of choices for the user to click through. The button-pressing pattern, when carried into the LLM era unchanged, forces a powerful underlying system into the interaction shape of a less powerful one. The interface becomes the bottleneck on what the system can do.

The replacement is not a single new pattern but a shift in what interfaces are for. They are less menus of pre-defined actions and more bidirectional channels: the system surfaces context-aware initiatives, the user accepts, refines, or redirects. The visual elements that survive (charts, diagrams, structured summaries) survive because they support comprehension at scale, not because they are the locus of input. Input is increasingly natural-language refinement of system-initiated work.

**Open questions:**
- Are there domains where the button-based UI remains the right pattern even in an LLM-native world? Safety-critical applications, regulated workflows, and tasks with limited valid action space might preserve it.
- How does the transition happen in practice? Most products today use LLMs behind traditional UIs; the inertia of existing interface patterns is significant and the migration path is unclear.

## Links

- Confirms: [[language-models-enable-a-shift-from-reactive-to-context-aware-initiative-in-machine-interfaces|Language models enable a shift from reactive to context-aware initiative in machine interfaces]]
- Context: [[chatbots-are-not-the-primary-interface-for-serious-ai-work-in-the-long-run-because-they-impose-high-cognitive-load-and-negate-the-combinatorial-power-of-language-models|Chatbots are not the primary interface for serious AI work in the long run because they impose high cognitive load and negate the combinatorial power of language models]]
- Context: [[the-interface-of-the-future-may-separate-cognition-by-an-agent-team-in-natural-language-from-presentation-by-a-second-team-in-structured-visual-outputs|The interface of the future may separate cognition by an agent team in natural language from presentation by a second team in structured visual outputs]]
