---
type: evergreen
created: 2026-04-03
source: "Thought session: Multi-agent communication challenges"
tags: [multi-agent-systems, agent-architecture, global-workspace, cognitive-architecture, LLM]
aliases:
  - "LLM agents need separate modules for observation reasoning and speech"
---

# LLM agents need separate modules for observation reasoning and speech

Source: [[multi-agent-communication-challenges|Multi-agent communication challenges]]

An LLM agent participating in multi-agent conversation needs at least three distinct modules sharing a global workspace: an observer that monitors the conversational environment, a thinker that reasons internally about what is happening and what to do, and a speaker that synthesizes the thinker's output into appropriate communication for other agents. This mirrors Global Workspace Theory from cognitive science, where consciousness arises from a shared workspace that broadcasts to specialized processors.

The separation matters because LLMs generate a single text stream — they don't natively distinguish between internal reasoning and external speech. Without architectural separation, an agent's raw chain-of-thought would be transmitted directly to other agents, which is not how effective communication works. Humans think, then frame sentences appropriate to their audience and context. The observer feeds environmental signals into the thinker, the thinker reasons about what matters and what to say, and the speaker synthesizes that reasoning into contextually appropriate output.

The cost implication is significant: each "turn" in a multi-agent conversation potentially requires multiple LLM calls per agent (observe, think, speak), multiplied across all participating agents. This is a real constraint when using API-based LLMs with per-token pricing and rate limits.

**Open questions:**
- Can the observer and thinker be collapsed into a single module with structured output (internal reasoning + speech decision), or does separation produce meaningfully better behavior?
- How does the global workspace get managed? What goes in, what gets pruned, and how does context window pressure affect it?

## Links

- Context: [[the-multi-agent-conversation-problem-decomposes-into-specific-subproblems|The multi-agent conversation problem decomposes into specific subproblems]]
- Extends: [[the-when-to-speak-problem-in-multi-agent-ai-has-two-distinct-sub-problems-when-to-start-and-when-to-stop|The when-to-speak problem in multi-agent AI has two distinct sub-problems — when to start and when to stop]]
