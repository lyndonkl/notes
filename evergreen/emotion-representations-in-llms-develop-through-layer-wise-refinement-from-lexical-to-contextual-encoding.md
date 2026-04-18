---
type: evergreen
created: 2026-04-18
source: "Emotion Concepts and their Function in a Large Language Model"
tags: [emotions, interpretability, transformer-layers, representation-engineering, claude-sonnet-4-5]
aliases:
  - "Emotion representations in LLMs develop through layer-wise refinement from lexical to contextual encoding"
---

# Emotion representations in LLMs develop through layer-wise refinement from lexical to contextual encoding

Source: [[emotion-concepts-and-their-function-in-a-large-language-model|Emotion Concepts and their Function in a Large Language Model]]

In Claude Sonnet 4.5, emotion-related representations are not built in a single layer but refined progressively across the transformer stack. Early-middle layers encode emotional connotations tied to the present content — the emotion implicit in the text currently being processed. Middle-late layers shift to encoding emotions relevant for predicting upcoming tokens — the emotional state the model expects to be expressed next. This divides the stack into a retrospective phase (what emotion is present now) and a prospective phase (what emotion will be needed next).

The temporal decomposition is meaningful because it suggests emotion is not a surface feature but a predictive signal the model actively computes and carries forward. The representations are also "locally scoped" in the paper's usage: they track the operative emotion at the current token, not the persistent emotional state of any single character. Context tracking of multi-turn emotional dynamics is separately mediated by attention, which can recall cached emotion representations from earlier tokens when needed.

The layer-wise structure has implications for where to probe or intervene. If the goal is to read the model's current emotional tone, early-middle layers may suffice. If the goal is to forecast or preempt emotionally-charged outputs, middle-late layers are the more informative probe. For activation-steering interventions, the choice of layer is not incidental — it determines whether you are shifting the model's reading of present content or its prediction of future content.

**Open questions:**
- Does the early-to-late split hold across different kinds of affective content (character emotion vs. narrator emotion vs. Assistant emotion), or is it specific to the synthetic-story elicitation?
- How does this interact with the "no privileged basis" property of the residual stream — are these emotion features actually layer-localized, or merely more detectable at certain layers?
- Is there a principled way to pick a steering layer, or does it remain hyperparameter search?

## Links

- Context: [[the-residual-stream-at-any-layer-is-the-cumulative-sum-of-the-original-embedding-and-all-previous-layer-outputs-making-it-a-communication-channel-not-a-processing-unit|The residual stream at any layer is the cumulative sum of the original embedding and all previous layer outputs, making it a communication channel, not a processing unit]]
- Context: [[transformer-residual-stream-is-linear-space-permitting-feature-directions-despite-sublayer-nonlinearities|Transformer residual stream is linear space permitting feature directions despite sublayer nonlinearities]]
- Context: [[layer-selection-in-lat-is-hyperparameter-search-not-principled-choice|Layer selection in LAT is hyperparameter search not principled choice]]
