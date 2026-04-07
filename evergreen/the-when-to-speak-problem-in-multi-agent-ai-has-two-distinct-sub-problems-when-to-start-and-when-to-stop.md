---
type: evergreen
created: 2026-04-03
source: "Thought session: Multi-agent communication challenges"
tags: [multi-agent-systems, conversation-mechanics, turn-taking, coordination]
aliases:
  - "The when-to-speak problem in multi-agent AI has two distinct sub-problems — when to start and when to stop"
---

# The when-to-speak problem in multi-agent AI has two distinct sub-problems — when to start and when to stop

Source: [[thought-session-multi-agent-communication-challenges|Thought Session: Multi-Agent Communication Challenges]]

Coordinating conversation among multiple LLM agents requires solving two fundamentally different problems that are often conflated. The when-to-start problem is about an agent recognizing that it should contribute — that the conversation has reached a point where its expertise, perspective, or role is relevant. This is an external signal problem: the agent's observer module monitors the conversational environment and identifies triggers like direct questions, topic relevance, or conversational pauses.

The when-to-stop problem is harder and fundamentally different. It requires the speaking agent to sense whether its contribution is landing, whether others need to respond, whether it's dominating the conversation. In human interaction, these are read through facial cues, body language, and vocal tone — rich nonverbal channels that don't exist in text-based LLM communication. The speaking agent gets no real-time feedback while generating output. This makes stopping a harder problem than starting, because starting can be triggered externally while stopping requires either internal judgment or a protocol-based mechanism.

The asymmetry between these two sub-problems suggests they may need different solutions: external environmental monitoring for when to start, and either explicit conversational protocols or internal generation-time heuristics for when to stop.

**Open questions:**
- Could activation-space observation (reading another model's internal state) serve as an analogue to facial cues, if models are run locally?
- Is there a simple heuristic for stopping — like a token budget per turn, or a self-evaluation step after each paragraph — that's "good enough" without solving the deeper problem?

## Links

- Extends: [[the-multi-agent-conversation-problem-decomposes-into-specific-subproblems|The multi-agent conversation problem decomposes into specific subproblems]]
- Context: [[llm-agents-need-separate-modules-for-observation-reasoning-and-speech|LLM agents need separate modules for observation reasoning and speech]]
