---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [agentic-AI, AI-alignment, institutional-design, human-agent-loop]
aliases:
  - "Institutional templates and human-in-loop operate at different levels of an agentic AI system"
---

# Institutional templates and human-in-loop operate at different levels of an agentic AI system

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

Two claims about agentic AI design appear to be in tension but are not. The first claims that scalable AI alignment requires designing institutional templates so that agents behave well due to structural constraints rather than individual correction. The second claims that the human cannot be removed from the loop because the loop's terminal feedback is human satisfaction. Both are correct, and they apply at different levels of the system.

Institutional templates govern *how AI agents collaborate with one another*. They are the design layer for inter-agent dynamics: roles, protocols, constraints on how one agent communicates with another, the structural shape of the collaboration. At this level, human-by-human correction is intractable — there are too many interactions to oversee, and the value of multi-agent systems is precisely in their ability to do work humans cannot directly supervise.

Human-in-loop operates at a different level: *who ultimately evaluates whether the system's work was the right work*. This is not about overseeing every agent-to-agent exchange; it is about the terminal evaluation of the system's output, which must remain with a human because the agency that gives the work its purpose is loaned from the human.

Most arguments about "AI autonomy" conflate these two levels. The conflation produces unproductive disagreements where one side defends institutional autonomy (correctly) while the other defends human evaluation (also correctly), each thinking they are arguing about the same thing.

**Open questions:**
- Are there design patterns for cleanly separating these two levels in actual agent system architectures? The literature treats them as one thing.
- At what scale does the level distinction itself become unstable — e.g., when institutional templates can be modified by agents during operation, do they remain at the inter-agent level or migrate into the human-evaluation level?

## Links

- Confirms: [[scalable-ai-alignment-requires-institutional-templates-not-individual-virtue|Scalable AI alignment requires institutional templates not individual virtue]]
- Extends: [[the-human-agent-loop-is-a-permanent-architecture-for-agentic-ai-not-a-transitional-stage|The human-agent loop is a permanent architecture for agentic AI not a transitional stage]]
- Context: [[institutional-templates-for-ai-agents-should-constrain-response-space-not-prescribe-responses|Institutional templates for AI agents should constrain response space not prescribe responses]]
