---
type: structure-note
created: 2026-04-03
tags: [activation-steering, representation-engineering, behavioral-control, multi-agent-systems]
---

# Steering agent behavior through representation rather than text

Can LLM agent behavior be controlled at the representation level (activation space) rather than through prompts, and what cognitive taxonomy would make that control tractable? This cluster traces a research program from identifying the right behavioral dimensions, through mapping them to activation space, to developing dynamic steering heuristics.

## Core Notes

- [[activation-steering-could-enforce-behavioral-traits-in-llm-agents-without-consuming-prompt-context|Activation steering could enforce behavioral traits in LLM agents without consuming prompt context]] — The foundational claim: behavioral enforcement can move from prompt-level to weight-level, freeing context window and enabling dynamic mid-conversation adjustment
- [[the-interpersonal-circumplex-provides-a-minimal-two-axis-model-for-multi-agent-behavioral-dimensions|The Interpersonal Circumplex provides a minimal two-axis model for multi-agent behavioral dimensions]] — Proposes Agency and Communion as the two orthogonal axes that generate the full range of interpersonal behavior, collapsing a combinatorial problem into two parameters
- [[emotional-valence-may-be-upstream-of-behavioral-traits-in-transformer-activation-space|Emotional valence may be upstream of behavioral traits in transformer activation space]] — Suggests that steering emotional dimensions (fewer, more fundamental) might cascade into behavioral traits, further reducing the dimensionality of the control problem
- [[enforcing-behavioral-norms-in-llm-agents-requires-a-three-stage-research-pipeline|Enforcing behavioral norms in LLM agents requires a three-stage research pipeline]] — Synthesizes the above into a sequential research program: taxonomy → mapping → heuristics, with dependencies between stages

## Borderline / Adjacent

- [[text-native-conversational-protocols-may-be-more-practical-than-activation-space-observation-for-coordinating-llm-agents|Text-native conversational protocols may be more practical than activation-space observation for coordinating LLM agents]] — The pragmatic alternative when model internals aren't accessible; represents the other side of a strategic fork (representation control vs. protocol control)

## Open Questions

- Does activation steering compose well when multiple behavioral dimensions are steered simultaneously, or do they interfere?
- Is the Circumplex's two-axis model sufficient, or do multi-agent coordination tasks require additional dimensions (epistemic confidence, information-sharing propensity)?
- Can the three-stage pipeline be bootstrapped empirically — observing multi-agent failures and reverse-engineering which behavioral dimensions would have prevented them?
- If emotional valence is upstream of traits, does the taxonomy stage simplify dramatically?

## Connections to Other Clusters

- [[intelligence-as-a-property-of-social-systems-not-individual-agents]] — The institutional templates concept motivates the need for behavioral enforcement; this cluster proposes the mechanism
- [[the-multi-agent-conversation-problem-decomposes-into-specific-subproblems]] — Conversation mechanics are the context in which behavioral steering would operate; the observer/thinker/speaker architecture would need to integrate with steering
