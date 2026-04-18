---
type: evergreen
created: 2026-04-18
source: "Emotion Concepts and their Function in a Large Language Model"
tags: [emotions, representation-engineering, interpretability, valence-arousal, affect-geometry, claude-sonnet-4-5]
aliases:
  - "LLM emotion representations organize along valence and arousal axes resembling human affect geometry"
---

# LLM emotion representations organize along valence and arousal axes resembling human affect geometry

Source: [[emotion-concepts-and-their-function-in-a-large-language-model|Emotion Concepts and their Function in a Large Language Model]]

When linear emotion vectors are extracted from Claude Sonnet 4.5's activations using synthetic stories that depict characters experiencing specified emotions, the resulting vector space has two leading principal components that encode valence (positive vs. negative) and arousal (intensity). Emotions cluster intuitively in this space — fear with anxiety, joy with excitement — echoing the two-dimensional affect geometry of Russell's circumplex model from human psychology. The model was not trained to represent emotions in this form; the geometry emerges from learning to predict text in which humans describe and enact emotional states.

This is a structural convergence between human cognitive models of affect and LLM internal representations, but it is not a claim about equivalence. The paper calls these "functional emotions": patterns of expression and behavior modeled after humans under the influence of an emotion, mediated by abstract emotion representations. The convergence at the geometric level does not imply convergence at the experiential level; it is a finding about representational organization, not about subjective experience.

The valence/arousal geometry is useful because it suggests a low-dimensional control surface. If only two principal components carry most of the variance in how emotions are encoded, then interventions aimed at steering emotional tone in generated text may only need to manipulate those two dimensions rather than a high-dimensional emotion taxonomy. How tightly this low-dimensional projection maps to observable behavior differences is a separate question.

**Open questions:**
- Are the top principal components always valence and arousal, or are they model- and context-dependent?
- Does the 2D projection lose information that matters for distinguishing emotions within a quadrant (e.g., anger vs. disgust, both high-arousal-negative)?
- How robust is the geometry to changes in the synthetic story generation pipeline used to elicit emotion vectors?

## Links

- Context: [[emotional-valence-may-be-upstream-of-behavioral-traits-in-transformer-activation-space|Emotional valence may be upstream of behavioral traits in transformer activation space]]
- Context: [[the-interpersonal-circumplex-provides-a-minimal-two-axis-model-for-multi-agent-behavioral-dimensions|The Interpersonal Circumplex provides a minimal two-axis model for multi-agent behavioral dimensions]]
- Context: [[high-level-semantic-features-in-transformer-residual-streams-are-encoded-as-approximately-linear-directions|High-level semantic features in transformer residual streams are encoded as approximately linear directions]]
