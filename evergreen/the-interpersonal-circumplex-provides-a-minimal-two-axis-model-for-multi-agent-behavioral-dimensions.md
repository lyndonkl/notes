---
type: evergreen
created: 2026-04-03
source: "Thought session: Multi-agent communication challenges"
tags: [interpersonal-circumplex, behavioral-dimensions, multi-agent-systems, social-psychology, activation-steering]
aliases:
  - "The Interpersonal Circumplex provides a minimal two-axis model for multi-agent behavioral dimensions"
---

# The Interpersonal Circumplex provides a minimal two-axis model for multi-agent behavioral dimensions

Source: [[thought-session-multi-agent-communication-challenges|Thought Session: Multi-Agent Communication Challenges]]

The Interpersonal Circumplex, a well-established model from social psychology, reduces the full space of interpersonal behavior to two orthogonal axes: Agency (dominance vs. submission) and Communion (warmth vs. hostility). Every interpersonal behavior can be located as a point in this two-dimensional space. A directive leader is high-agency, moderate-communion. A supportive collaborator is moderate-agency, high-communion. A passive-aggressive underminer is low-agency, low-communion.

For multi-agent AI systems, this model offers a concrete starting point for the behavioral dimension taxonomy that activation steering requires. Rather than trying to enumerate every behavioral trait an agent might need — assertiveness, deference, cooperativeness, competitiveness, warmth, coldness, directness, diplomacy — the Circumplex suggests that two underlying dimensions might generate all of these as surface expressions. An agent that needs to be "diplomatically firm" is high-agency, high-communion. An agent that needs to "defer to authority" is low-agency, high-communion. The combinatorial explosion of behavioral specifications collapses into a two-parameter space.

The question is whether this reduction is sufficient for the engineering requirements of multi-agent coordination. Human social psychology validates the two-axis model for interpersonal behavior, but multi-agent AI systems may need additional dimensions that don't arise in human interaction — for instance, a dimension for epistemic confidence (how certain the agent presents itself as being), or a dimension for task-focus vs. relationship-focus that doesn't map cleanly onto Agency or Communion. The Circumplex is a starting hypothesis, not a final answer, but it provides a principled foundation rather than an ad hoc enumeration of traits.

**Open questions:**
- Do Agency and Communion map to identifiable directions in transformer activation space? Has anyone tested Circumplex dimensions specifically in representation engineering?
- Are two axes actually sufficient for multi-agent coordination, or do task-specific dimensions (epistemic confidence, information-sharing propensity) need to be added?
- How does the Circumplex interact with role-based behavior? A manager agent and an analyst agent might need different default positions on the Circumplex — how would those defaults be set and dynamically adjusted?

## Links

- Extends: [[emotional-valence-may-be-upstream-of-behavioral-traits-in-transformer-activation-space|Emotional valence may be upstream of behavioral traits in transformer activation space]]
- Context: [[activation-steering-could-enforce-behavioral-traits-in-llm-agents-without-consuming-prompt-context|Activation steering could enforce behavioral traits in LLM agents without consuming prompt context]]
- Context: [[enforcing-behavioral-norms-in-llm-agents-requires-a-three-stage-research-pipeline|Enforcing behavioral norms in LLM agents requires a three-stage research pipeline]]
