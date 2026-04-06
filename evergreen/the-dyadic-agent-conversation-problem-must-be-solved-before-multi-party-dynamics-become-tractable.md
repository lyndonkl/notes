---
type: evergreen
created: 2026-04-03
source: "Thought session: Multi-agent communication challenges"
tags: [multi-agent-systems, group-dynamics, dyadic-interaction, coordination, research-prioritization]
aliases:
  - "The dyadic agent conversation problem must be solved before multi-party dynamics become tractable"
---

# The dyadic agent conversation problem must be solved before multi-party dynamics become tractable

Source: [[multi-agent-communication-challenges|Multi-agent communication challenges]]

Multi-party conversation among LLM agents is not simply the two-agent case scaled up. Group dynamics introduce emergent phenomena that don't exist in dyadic exchange: coalition formation, bystander effects (everyone assumes someone else will respond), information cascades (anchoring on the first confident statement), and the gap between shared knowledge and common knowledge. The when-to-speak problem also changes qualitatively — in a two-party exchange, silence is unambiguous; in a five-agent conversation, one agent's silence could mean thinking, deferring, disengagement, or having nothing to add.

However, none of these multi-party problems are tractable until the two-agent case is solved. The observer/thinker/speaker module architecture, the when-to-speak mechanics, the activation steering approach to behavioral enforcement — these are all foundational components that multi-party coordination will build on top of. Attempting to solve group dynamics without a working model for how two agents coordinate would be building on sand.

The remaining challenge clusters — task assignment at scale and discovery — are being actively addressed by existing engineering efforts (Google's A2A protocol, retrieval-augmented memory systems, skill registries). These are worth monitoring but not worth original research investment at this stage. The one gap in current approaches: they solve reactive discovery ("find me an agent that can do X") but not proactive task identification ("figure out that X needs doing in the first place"). That distinction — help desk vs. good manager — may become important later.

## Links

- Extends: [[the-when-to-speak-problem-in-multi-agent-ai-has-two-distinct-sub-problems-when-to-start-and-when-to-stop|The when-to-speak problem in multi-agent AI has two distinct sub-problems — when to start and when to stop]]
- Context: [[llm-agents-need-separate-modules-for-observation-reasoning-and-speech|LLM agents need separate modules for observation reasoning and speech]]
- Context: [[enforcing-behavioral-norms-in-llm-agents-requires-a-three-stage-research-pipeline|Enforcing behavioral norms in LLM agents requires a three-stage research pipeline]]
