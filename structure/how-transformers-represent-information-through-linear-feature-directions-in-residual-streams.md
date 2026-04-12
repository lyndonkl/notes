---
type: structure-note
created: 2026-04-11
tags: [transformer-architecture, residual-stream, linearity, mechanistic-interpretability, representation-engineering]
---

# How transformers represent information through linear feature directions in residual streams

This cluster explains the architectural foundation that makes representation engineering possible: transformers encode high-level semantic features as linear directions in the residual stream. The residual stream acts as a linear accumulator between nonlinear sublayers, providing the geometric substrate where features can be represented additively and manipulated through vector arithmetic. Understanding this structure is critical for both mechanistic interpretability and for designing interventions in activation space.

## Core Notes

- [[transformer-residual-stream-is-linear-space-permitting-feature-directions-despite-sublayer-nonlinearities|The transformer residual stream is the linear space that permits feature directions to exist despite nonlinearities in attention and MLP sublayers]] — Explains why skip connections create a linear pathway despite the nonlinearities in attention and feedforward sublayers, making linear feature geometry mechanically possible.

- [[high-level-semantic-features-in-transformer-residual-streams-are-encoded-as-approximately-linear-directions|High-level semantic features in transformer residual streams are encoded as approximately linear directions, not nonlinear entangled manifolds]] — The empirical claim underlying representation engineering: semantic concepts like honesty and harmlessness are encoded as linear directions that can be located and steered via vector operations.

- [[the-transformer-residual-stream-has-no-privileged-basis-because-only-linear-operations-interact-with-it|The transformer residual stream has no privileged basis because only linear operations interact with it]] — Clarifies that individual dimensions in the residual stream have no intrinsic meaning; the meaningful units are arbitrary directions that the model learned during training, not the coordinate axes.

- [[attention-heads-apply-no-nonlinearity-to-value-vectors-softmax-governs-routing-but-content-movement-is-a-linear-weighted-sum|Attention heads apply no nonlinearity to value vectors — softmax governs routing but content movement is a linear weighted sum]] — Shows that the OV circuit (content movement) in attention is purely linear, enabling direct inspection of how information flows without actually running the model.

- [[the-residual-stream-at-any-layer-is-the-cumulative-sum-of-the-original-embedding-and-all-previous-layer-outputs-making-it-a-communication-channel-not-a-processing-unit|The residual stream at any layer is the cumulative sum of the original embedding and all previous layer outputs making it a communication channel not a processing unit]] — Describes the residual stream as a shared linear accumulator where all layers deposit their contributions, functioning as a broadcast channel rather than a pipeline.

## Borderline / Adjacent

- [[correlation-between-direction-and-concept-is-evidence-for-presence-not-function-only-causal-intervention-proves-implementation|Correlation between a direction and a concept is evidence for presence, not evidence for function—only causal intervention reveals whether a direction implements a concept]] — Important caveat: finding a linear direction aligned with a concept does not prove the direction implements that concept; causal intervention is required.

- [[mechanistic-interpretability-and-representation-engineering-answer-different-questions-using-incompatible-units-of-analysis|Mechanistic interpretability and representation engineering answer different questions about model behavior using incompatible units of analysis]] — Clarifies the distinction between understanding circuits mechanistically versus understanding activation geometry; this cluster takes the geometric view.

## Open Questions

- Does residual stream linearity remain a good approximation deeper in layers as nonlinearities accumulate, or does it degrade?
- How do normalization layers (LayerNorm) interact with the lack of a privileged basis — do they reintroduce coordinate dependence?
- Do all high-level concepts exhibit the linear representation property, or only certain types? What properties of a concept predict linearity?
- How does this geometry depend on model architecture — would it hold in models without explicit skip connections or with different normalization schemes?

## Connections to Other Clusters

- [[steering-agent-behavior-through-representation|Steering agent behavior through representation rather than text]] — This cluster provides the geometric foundation; the representation cluster builds on it to show how linear feature directions can be used for behavioral control in multi-agent systems.
