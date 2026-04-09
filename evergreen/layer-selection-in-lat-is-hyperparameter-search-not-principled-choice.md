---
type: evergreen
created: 2026-04-08
source: "Representation Engineering: A Top-Down Approach to AI Transparency"
tags: [representation-engineering, method-critique, hyperparameter-tuning, layer-selection, engineering-burden]
aliases:
  - "Layer selection in LAT is a hyperparameter search problem, not a principled choice, which adds bespoke engineering burden to representation engineering"
---

# Layer selection in LAT is a hyperparameter search problem, not a principled choice, which adds bespoke engineering burden to representation engineering

Source: [[representation-engineering-a-top-down-approach-to-ai-transparency|Representation Engineering: A Top-Down Approach to AI Transparency]]

One critical weakness in LAT is that choosing which transformer layer (or layers) to intervene at is not a theoretically derived decision. It is a hyperparameter search. Figure 5's heatmap sweeps across every layer and token position for each concept, and the chosen layer is whichever gives highest classification accuracy on a held-out evaluation task. The paper often intervenes at multiple layers simultaneously, not one. Middle-to-late layers tend to work better, but the optimum varies by concept, model size, and downstream task. For honesty, the best layer might be layer 16 of a 24-layer model; for harmlessness, it might be layer 20; for a different model, those choices shift again.

This adds friction to the "clean, top-down" narrative that the paper's framing suggests. Layer selection is currently a search problem, which means applying RepE to a new concept or a new model requires running an empirical hyperparameter sweep before you can extract the direction. This is fine at research scale, where model access is cheap and you only need to do it once per concept. But it undermines the engineering simplicity that the method promises for practical deployment. Any honest assessment of the method should acknowledge that the bespoke engineering texture — per-concept, per-model tuning — is not incidental; it is baked into the current approach.

The underlying question is whether a principled theory exists that would let you predict the right layer for a given concept. Middle-to-late layers are where high-level semantic information is more concentrated, which suggests a heuristic: intervene where the concept is best represented. But that is circular reasoning — you know the layer is best by sweeping and checking, not by theory. Until there is either a principled principle or a reliable prior (e.g., "always layer 16 works for all concepts across model families"), layer selection remains engineering work, not science.

**Open questions:**
- Does the optimal layer for a concept correlate with the layer at which the concept is most representable (via probing), or is there a gap between representation and control?
- Could layer selection be automated — e.g., through a meta-learner that predicts the right layer given the concept and model?
- Do the concepts that work best at early layers have different properties (more syntactic, more local) than those that work best at late layers (more semantic, more global)?

## Links

- Contradicts: [[high-level-semantic-features-in-transformer-residual-streams-are-encoded-as-approximately-linear-directions|High-level semantic features in transformer residual streams are encoded as approximately linear directions, not nonlinear entangled manifolds]]
- Context: [[representation-engineering-amortizes-cost-into-one-time-calibration-adding-near-zero-runtime-overhead|Representation engineering amortizes computational cost into one-time calibration, adding near-zero runtime overhead at inference]]
- Context: [[enforcing-behavioral-norms-in-llm-agents-requires-a-three-stage-research-pipeline|Enforcing behavioral norms in LLM agents requires a three-stage research pipeline]]
- Context: [[the-strength-of-a-model-is-defined-by-what-it-prohibits-not-by-what-it-explains|The strength of a model is defined by what it prohibits, not by what it explains]]
