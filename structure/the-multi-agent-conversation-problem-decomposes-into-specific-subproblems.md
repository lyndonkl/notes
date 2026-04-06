---
type: structure-note
created: 2026-04-03
tags: [conversation-mechanics, agent-architecture, coordination, turn-taking, multi-agent-systems]
---

# The multi-agent conversation problem decomposes into specific subproblems

How do LLM agents actually coordinate in real time? This cluster treats multi-agent conversation as a solvable engineering problem with distinct sub-components: the when-to-speak problem (starting vs. stopping), the architectural separation of observation from reasoning from speech, the scoping decision to solve dyadic conversation before multi-party, and the practical choice between protocol-based and representation-based coordination.

## Core Notes

- [[the-when-to-speak-problem-in-multi-agent-ai-has-two-distinct-sub-problems-when-to-start-and-when-to-stop|The when-to-speak problem in multi-agent AI has two distinct sub-problems — when to start and when to stop]] — Decomposes turn-taking into two asymmetric problems: starting is an external signal problem (solvable by an observer module), stopping requires internal judgment about conversation state (harder, no feedback channel in text-only APIs)
- [[llm-agents-need-separate-modules-for-observation-reasoning-and-speech|LLM agents need separate modules for observation reasoning and speech]] — Proposes a three-module architecture (observer/thinker/speaker) sharing a global workspace, inspired by Global Workspace Theory; separates the functions that current monolithic prompts collapse together
- [[the-dyadic-agent-conversation-problem-must-be-solved-before-multi-party-dynamics-become-tractable|The dyadic agent conversation problem must be solved before multi-party dynamics become tractable]] — Establishes scope and sequencing: multi-party introduces emergent phenomena (coalitions, bystander effects, information cascades) that depend on having a working dyadic model first
- [[text-native-conversational-protocols-may-be-more-practical-than-activation-space-observation-for-coordinating-llm-agents|Text-native conversational protocols may be more practical than activation-space observation for coordinating LLM agents]] — Proposes Slack/email-like structured protocols as a coordination mechanism that works with any LLM via API, without requiring access to model internals

## Borderline / Adjacent

None strong enough to list — institutional templates and behavioral control are adjacent domains but address different questions (what norms to follow vs. how to mechanically coordinate).

## Open Questions

- Can observer and thinker modules be collapsed without sacrificing behavior quality, or is the separation essential?
- What's a minimal "good enough" heuristic for the when-to-stop problem?
- How do text-native protocols handle the transition from dyadic to multi-party conversation?
- What specific multi-party dynamics (coalition formation, information cascades) require new architectural components beyond what the dyadic solution provides?

## Connections to Other Clusters

- [[steering-agent-behavior-through-representation]] — Behavioral steering would operate within the conversation mechanics this cluster defines; the observer module would need to integrate with steering heuristics
- [[intelligence-as-a-property-of-social-systems-not-individual-agents]] — The institutional norms from that cluster would be expressed through the conversation protocols and architectures described here
