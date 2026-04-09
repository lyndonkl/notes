---
type: evergreen
created: 2026-04-08
source: "Representation Engineering: A Top-Down Approach to AI Transparency"
tags: [representation-engineering, mechanistic-interpretability, interpretability, tradeoffs]
aliases:
  - "Interpretability methods that explain mechanism do not scale, and methods that scale do not explain mechanism"
---

# Interpretability methods that explain mechanism do not scale, and methods that scale do not explain mechanism

Source: [[representation-engineering-a-top-down-approach-to-ai-transparency|Representation Engineering: A Top-Down Approach to AI Transparency]]

There is a fundamental tension in interpretability research between two desiderata: understanding the detailed causal mechanism of how a model produces behavior, and scaling that understanding to realistic model sizes. Methods that prioritize mechanism necessarily do not scale; methods that prioritize scale necessarily sacrifice mechanistic understanding. This is not a temporary artifact of current research capacity — it appears to be structural.

Mechanistic interpretability offers genuine explanatory understanding. When you trace a circuit and identify which neurons fire for which inputs and how their outputs propagate to influence behavior, you know *how* the model computes. You can then manipulate that circuit, predict what will happen, and verify your prediction. But this work is labor-intensive in a way that does not parallelize well. Finding and validating a single circuit in a toy model can take weeks. Scaling this approach to large modern models (70B+ parameters) is not a matter of engineering optimization — it is conceptually unclear whether the entire codebase of a large model is even interpretable in this way, given that circuits interact at scale in ways we don't yet understand.

Representation engineering offers scalability. The Linear Algebraic Transformation (LAT) method can be applied to a 70B parameter model in an afternoon on standard hardware. You can extract directions from large models, validate their causal influence through targeted experiments, and deploy steering interventions. The cost is that you learn *that* a concept direction exists without learning *how* the model constructs or uses it. You know honesty is represented; you don't know which layers compute it, how those layers receive inputs, or what happens downstream when the direction is steered. Your understanding is descriptive, not mechanistic.

Generalizing beyond this specific pair of methods: every interpretability approach sits somewhere on this continuum. Methods offering deeper causal understanding trade away coverage. Methods that scale to real models trade away mechanism. The frontier of interpretability research is this boundary itself — new methods must choose which tradeoff to accept. Some problems may require mechanism (understanding failure modes in high-stakes systems); others may require only signal-level understanding (steering behavior, controlling outputs). The mistake is believing that advancing interpretability means advancing equally on both axes, when the tradeoff appears to be fundamental.

**Open questions:**
- Is the mechanism-scale tradeoff truly fundamental, or is it an artifact of current techniques? Could hybrid approaches (circuit identification at population level rather than individual component level) bridge it?
- Do practitioners actually need mechanistic understanding for interpretability to be useful? Or is signal-level understanding sufficient for most applications?
- What changes as models scale beyond 100B parameters? Does the mechanistic interpretability problem become harder, or does it fundamentally change into a different problem?

## Links

- Confirms: [[mechanistic-interpretability-and-representation-engineering-answer-different-questions-using-incompatible-units-of-analysis|Mechanistic interpretability and representation engineering answer different questions about model behavior using incompatible units of analysis]]
- Context: [[activation-steering-could-enforce-behavioral-traits-in-llm-agents-without-consuming-prompt-context|Activation steering could enforce behavioral traits in LLM agents without consuming prompt context]]
