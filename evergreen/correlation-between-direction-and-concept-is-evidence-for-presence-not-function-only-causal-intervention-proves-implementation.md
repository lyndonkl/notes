---
type: evergreen
created: 2026-04-08
source: "Representation Engineering: A Top-Down Approach to AI Transparency"
tags: [representation-engineering, causality, epistemology, evidence, evaluation]
aliases:
  - "Correlation between a direction and a concept is evidence for presence, not evidence for function—only causal intervention reveals whether a direction implements a concept"
---

# Correlation between a direction and a concept is evidence for presence, not evidence for function—only causal intervention reveals whether a direction implements a concept

Source: [[representation-engineering-a-top-down-approach-to-ai-transparency|Representation Engineering: A Top-Down Approach to AI Transparency]]

Finding that a direction in activation space correlates with a concept — that model activations move along this direction when the model outputs honest responses and move the opposite way when it outputs dishonest responses — establishes that *something about this direction tracks the concept*. But correlation is not evidence that the direction implements the concept or that the model actually uses it. The direction could be a confound: it might move with honesty because honesty and some other upstream variable are correlated, not because the direction itself is causally responsible for producing honesty. The only way to distinguish presence from function is through causal intervention.

The paper's four-category evaluation framework makes this rigor explicit: Correlation, Manipulation, Termination, and Recovery. Correlation shows that a direction tracks a concept (evidence of presence). Manipulation tests whether intervening on the direction — amplifying or dampening it — causes predicted changes in model behavior (evidence of causal influence). Termination tests whether removing the direction degrades the relevant capability (evidence that the model depends on it). Recovery tests whether reintroducing the direction restores performance (evidence that the degradation was actually caused by the removal, not by some side effect). Only together do these tests establish that a direction is not just correlated with a concept but actually implements it.

This principle generalizes far beyond representation engineering. Any empirical claim to have "found" a mechanism or concept inside a system — whether it's a neural network, a biological brain, or an organization — requires the same rigor. In neuroscience, researchers cannot claim that a brain region "encodes" a concept merely because neural activity correlates with the concept; they must show that inactivating the region impairs behavior in the predicted way. In organizational research, finding that a metric is correlated with team performance does not mean the metric causes performance; you need experiments that change the metric and track consequences. The temptation to stop at correlation is constant because correlation is easy to establish and causal inference is hard. But stopping there produces false confidence in findings that break down when tested.

The broader epistemic point: a model that explains everything explains nothing. A theory that can accommodate any observation contains no predictive power. Claims that survive only correlational evidence are maximally unfalsifiable — you can always hypothesize an unmeasured confounder. Causal evidence is expensive to obtain, but it is the only evidence that actually tests a hypothesis against the world.

**Open questions:**
- In the honesty experiments reported in Table 1 and Section 4, do the Manipulation → Termination → Recovery sequence confirm that the extracted direction is truly implementing the honesty concept, or could alternative mechanisms also produce these results?
- How do you design causal experiments for concepts that are themselves hard to define operationally? If you're steering "honesty," are you sure you know what behavior would count as honest?
- Can the four-category framework be applied to other interpretability methods, or is it specific to activation steering?

## Links

- Confirms: [[the-strength-of-a-model-is-defined-by-what-it-prohibits-not-by-what-it-explains|The strength of a model is defined by what it prohibits, not by what it explains]]
- Extends: [[mechanistic-interpretability-and-representation-engineering-answer-different-questions-using-incompatible-units-of-analysis|Mechanistic interpretability and representation engineering answer different questions about model behavior using incompatible units of analysis]]
- Context: [[enforcing-behavioral-norms-in-llm-agents-requires-a-three-stage-research-pipeline|Enforcing behavioral norms in LLM agents requires a three-stage research pipeline]]
