---
type: evergreen
created: 2026-04-03
source: "Thought session: Multi-agent communication challenges"
tags: [research-pipeline, activation-steering, behavioral-dimensions, multi-agent-systems, representation-engineering]
aliases:
  - "Enforcing behavioral norms in LLM agents requires a three-stage research pipeline"
---

# Enforcing behavioral norms in LLM agents requires a three-stage research pipeline

Source: [[thought-session-multi-agent-communication-challenges|Thought Session: Multi-Agent Communication Challenges]]

The problem of enforcing behavioral norms in multi-agent LLM systems without relying on prompts or hardcoded rules decomposes into three sequential research stages, each with its own dependencies and open questions. This pipeline emerged from reasoning about what would need to be true for activation steering to work as a practical enforcement mechanism.

**Stage 1: Taxonomy.** Build a comprehensive taxonomy of behavioral dimensions that matter for agent-to-agent interaction. Candidate frameworks include the Interpersonal Circumplex (Agency + Communion), the Big Five personality traits, and domain-specific dimensions like epistemic confidence or information-sharing propensity. The taxonomy must be grounded in what actually affects coordination quality — not just what's measurable. This stage draws on social psychology, organizational science, and empirical observation of multi-agent system failures.

**Stage 2: Mapping.** Map the taxonomized behavioral dimensions to identifiable regions in the model's activation space. This requires representation engineering techniques: probing for linear directions that correspond to each behavioral dimension, validating that these directions are causally influential (not just correlated), and testing whether they compose well when multiple dimensions are steered simultaneously. The "From Traits to Circuits" research program and Anthropic's emotion vector work suggest this is feasible, but it has not been done specifically for the interaction-relevant dimensions that multi-agent systems need.

**Stage 3: Heuristics.** Develop heuristics — possibly LLM-driven — for when, why, and how to steer behavioral dimensions based on conversational context. A manager agent entering a conflict-resolution conversation needs different behavioral settings than the same agent assigning routine tasks. These heuristics must be dynamic (adjusting mid-conversation), context-aware (responding to what other agents are doing), and stable (not oscillating erratically). This is the least explored stage and may be the hardest.

Each stage depends on the previous one, and each has the potential to invalidate assumptions made upstream. If the taxonomy proves too coarse, the mapping will miss important dimensions. If the mapping reveals that behavioral dimensions don't decompose cleanly in activation space, the heuristics stage becomes intractable.

**Open questions:**
- Can Stage 1 be bootstrapped empirically — by observing multi-agent system failures and reverse-engineering which behavioral dimensions would have prevented them?
- At Stage 2, does the mapping need to be model-specific, or do behavioral directions transfer across model families?
- Could Stage 3 heuristics themselves be learned from data (reinforcement learning on coordination outcomes), or must they be designed?

## Links

- Extends: [[activation-steering-could-enforce-behavioral-traits-in-llm-agents-without-consuming-prompt-context|Activation steering could enforce behavioral traits in LLM agents without consuming prompt context]]
- Context: [[the-interpersonal-circumplex-provides-a-minimal-two-axis-model-for-multi-agent-behavioral-dimensions|The Interpersonal Circumplex provides a minimal two-axis model for multi-agent behavioral dimensions]]
- Context: [[emotional-valence-may-be-upstream-of-behavioral-traits-in-transformer-activation-space|Emotional valence may be upstream of behavioral traits in transformer activation space]]
