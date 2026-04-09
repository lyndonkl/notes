---
type: evergreen
created: 2026-04-08
source: "Representation Engineering: A Top-Down Approach to AI Transparency"
tags: [representation-engineering, mechanistic-interpretability, interpretability, model-internals]
aliases:
  - "Mechanistic interpretability and representation engineering answer different questions about model behavior using incompatible units of analysis"
---

# Mechanistic interpretability and representation engineering answer different questions about model behavior using incompatible units of analysis

Source: [[representation-engineering-a-top-down-approach-to-ai-transparency|Representation Engineering: A Top-Down Approach to AI Transparency]]

The core insight is that these two approaches to understanding neural networks are not competing methods for the same goal — they are answers to fundamentally different questions, using incompatible measurement units. Conflating them as if they were variations on the same technique obscures what each one is actually good for.

Mechanistic interpretability's unit of analysis is the *component* — individual neurons, attention heads, and their wired relationships. The output is a circuit diagram: a map of specific computations flowing through specific pathways. When an MI researcher traces how a model computes a behavior, they are building an account of *how the model constructs X* — the mechanism. This requires picking a specific implementation and following the data flow through it. The explanatory power lies in the causality: this head computes attention over pronouns because these neurons activate strongly for gender features, which feed into that head's query mechanism. That's mechanistic explanation.

Representation engineering's unit of analysis is the *population* — the geometry of activation space as a whole. The output is a direction or a subspace: a vector that points in the direction of a concept, or a region of high-dimensional space where a concept is represented. RepE is deliberately agnostic about which neurons or circuits implement that concept. When a RepE researcher identifies a direction for honesty, they are answering *what concept is encoded, and where does it live* — the signal. The cost is that they cannot tell you the causal story of how the model *computes* honesty; they can only tell you that honesty is expressed somewhere in activation space.

These approaches do not compose into a single explanation. If you know how a circuit computes some behavior (MI answer), that tells you almost nothing about whether there is a direction in activation space that captures the same concept (RepE answer). Conversely, finding a direction for a concept does not explain the mechanism, because the same direction might emerge from different circuit implementations, or the direction might be a epiphenomenon of circuits computing something else entirely. Choosing between them means choosing between understanding the *how* of computation and understanding the *what* of representation.

**Open questions:**
- Can the two approaches be integrated? Does identifying a direction in activation space constrain which mechanisms could implement it, or are many mechanisms consistent with a single causal direction?
- Does the scale difference (RepE works on large models, MI struggles with them) reflect a fundamental difference in what's learnable about large networks, or just a methodological artifact that could be overcome?

## Links

- Extends: [[interpretability-methods-that-explain-mechanism-do-not-scale-and-methods-that-scale-do-not-explain-mechanism|Interpretability methods that explain mechanism do not scale, and methods that scale do not explain mechanism]]
- Context: [[activation-steering-could-enforce-behavioral-traits-in-llm-agents-without-consuming-prompt-context|Activation steering could enforce behavioral traits in LLM agents without consuming prompt context]]
- Context: [[enforcing-behavioral-norms-in-llm-agents-requires-a-three-stage-research-pipeline|Enforcing behavioral norms in LLM agents requires a three-stage research pipeline]]
