---
type: evergreen
created: 2026-04-11
source: "A Mathematical Framework for Transformer Circuits"
tags: [mechanistic-interpretability, attention-mechanism, linearity, transformer-architecture, QK-OV-decomposition]
aliases:
  - "Attention heads apply no nonlinearity to value vectors — softmax governs routing but content movement is a linear weighted sum"
---

# Attention heads apply no nonlinearity to value vectors — softmax governs routing but content movement is a linear weighted sum

Source: [[a-mathematical-framework-for-transformer-circuits|A Mathematical Framework for Transformer Circuits]]

The projection matrices W_Q, W_K, and W_V are purely linear transformations of input embeddings — no activation function is applied. The softmax operation that produces attention weights is nonlinear, but it operates on the routing side: which positions attend to which. Once the attention weights are computed, they are applied to value vectors as a weighted sum, which is a linear operation. This means attention heads move information linearly through the residual stream.

The nonlinearity in softmax determines *where* information flows, but not *what* is moved — the payload itself is a linear combination of value vectors. This is the basis for the paper's decomposition of each attention head into two independent circuits: the QK circuit (which tokens attend to which — involving softmax, therefore nonlinear) and the OV circuit (what information gets moved — purely linear). You can analyze these circuits separately because they operate on different aspects of the head's function.

This distinction has a practical consequence: because the OV circuit is linear, you can inspect what an attention head *does* to information by examining the OV weight matrices directly, without running the model on any inputs. The linearity makes the content-movement side of attention heads directly readable from weights.

**Open questions:**
- Does the linearity of value combination limit what individual attention heads can compute, or is expressiveness recovered through stacking layers and composing heads?
- How does this interact with the nonlinearities in MLP layers that this paper deliberately excludes?

## Links

- Extends: [[transformer-residual-stream-is-linear-space-permitting-feature-directions-despite-sublayer-nonlinearities|The transformer residual stream is the linear space that permits feature directions to exist despite nonlinearities in attention and MLP sublayers]]
