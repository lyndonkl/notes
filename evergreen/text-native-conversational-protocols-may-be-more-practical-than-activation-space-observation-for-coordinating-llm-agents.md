---
type: evergreen
created: 2026-04-03
source: "Thought session: Multi-agent communication challenges"
tags: [multi-agent-systems, conversation-protocols, activation-steering, API-constraints, coordination]
aliases:
  - "Text-native conversational protocols may be more practical than activation-space observation for coordinating LLM agents"
---

# Text-native conversational protocols may be more practical than activation-space observation for coordinating LLM agents

Source: [[multi-agent-communication-challenges|Multi-agent communication challenges]]

There are two competing approaches to coordinating turn-taking and conversation flow among LLM agents. The first is activation-space observation: reading the internal representations of other models to detect signals analogous to human facial cues and body language — a rich but technically demanding approach that requires local model access and is impossible through commercial LLM APIs. The second is text-native conversational protocols: designing explicit turn markers, handoff signals, and structured metadata that agents include in their text output — like how humans coordinate effectively in Slack, email, and asynchronous collaboration without any nonverbal cues at all.

The text-native approach has a significant practical advantage: it works with any LLM, whether API-based or local, and requires no access to model internals. Humans have already solved the text-only coordination problem through cultural conventions — "thoughts?", "over to you", structured formats, explicit questions. These are essentially soft institutional templates for conversation, constraining the space of how agents communicate without prescribing what they say.

However, activation-space observation remains an open and potentially powerful research direction. Work on emotional circuits in transformer activation spaces suggests that behavioral traits can be identified and steered at the representation level. If models are run locally, reading another agent's activation state during conversation could provide richer feedback than text alone — potentially enabling more natural, adaptive coordination. The two approaches are not mutually exclusive: text protocols for API-based systems, activation observation for local deployments.

**Open questions:**
- What would a minimal set of text-native conversational protocols look like? What markers and conventions would agents need to coordinate effectively?
- Could activation-space signals be distilled into text-level metadata that agents expose alongside their output — a middle ground between full activation access and pure text?
- How do you enforce protocol compliance without consuming prompt context with behavioral instructions?

## Links

- Extends: [[the-when-to-speak-problem-in-multi-agent-ai-has-two-distinct-sub-problems-when-to-start-and-when-to-stop|The when-to-speak problem in multi-agent AI has two distinct sub-problems — when to start and when to stop]]
- Extends: [[institutional-templates-for-ai-agents-should-constrain-response-space-not-prescribe-responses|Institutional templates for AI agents should constrain response space not prescribe responses]]
- Context: [[activation-steering-could-enforce-behavioral-traits-in-llm-agents-without-consuming-prompt-context|Activation steering could enforce behavioral traits in LLM agents without consuming prompt context]]
