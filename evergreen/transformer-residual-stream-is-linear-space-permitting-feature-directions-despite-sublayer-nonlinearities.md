---
type: evergreen
created: 2026-04-08
source: "Representation Engineering: A Top-Down Approach to AI Transparency"
tags: [representation-engineering, transformer-architecture, residual-streams, linearity, nonlinearity, sublayer-computation]
aliases:
  - "The transformer residual stream is the linear space that permits feature directions to exist despite nonlinearities in attention and MLP sublayers"
---

# The transformer residual stream is the linear space that permits feature directions to exist despite nonlinearities in attention and MLP sublayers

Source: [[representation-engineering-a-top-down-approach-to-ai-transparency|Representation Engineering: A Top-Down Approach to AI Transparency]]

A naive reader might think that transformers are deeply nonlinear systems — softmax in attention, GELU or SiLU in MLPs — and therefore cannot support clean vector arithmetic on their hidden states. But there is a critical structural fact that makes the linear representation hypothesis mechanically possible: each transformer layer adds its outputs to the running residual stream via skip connections. The architectural pattern is `h_L = h_{L-1} + Attention(h_{L-1}) + MLP(h_{L-1})`. The nonlinearities are encapsulated inside the sublayers (attention and MLP compute what to write), while what flows forward along the residual stream is a linear superposition of all the contributions every layer has written into it.

This design is the source of the geometry that representation engineering exploits. The residual stream is the linear space between nonlinear blocks. Features can live as additive directions precisely because the architecture has this structural property: nonlinear computation happens at the leaf level, but the trunk of the network is a linear accumulator. Without skip connections, without the residual stream as a central linear pathway, the linear representation hypothesis could not hold, and representation engineering would have no substrate to operate on.

This is not accidental architectural elegance — it is a design choice that has downstream consequences. Models with different residual stream structures (different skip connection patterns, different layer sizes, recurrent gates instead of feed-forward passes) might not support the same linear feature geometry. This makes the architectural property load-bearing for the entire approach.

**Open questions:**
- Does residual stream linearity remain a good approximation deeper in the network, or does it degrade as nonlinear operations accumulate?
- Could an architecture without explicit skip connections (e.g., a dense net or a fully recurrent model) still support linear feature directions through emergent redundancy in the weight matrix?
- How does residual stream linearity interact with normalization layers, which also shape activation geometry?

## Links

- Explains: [[high-level-semantic-features-in-transformer-residual-streams-are-encoded-as-approximately-linear-directions|High-level semantic features in transformer residual streams are encoded as approximately linear directions, not nonlinear entangled manifolds]]
- Context: [[mechanistic-interpretability-and-representation-engineering-answer-different-questions-using-incompatible-units-of-analysis|Mechanistic interpretability and representation engineering answer different questions about model behavior using incompatible units of analysis]]
- Context: [[activation-steering-could-enforce-behavioral-traits-in-llm-agents-without-consuming-prompt-context|Activation steering could enforce behavioral traits in LLM agents without consuming prompt context]]
