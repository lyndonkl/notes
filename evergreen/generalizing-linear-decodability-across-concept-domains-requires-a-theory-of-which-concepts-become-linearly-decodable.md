---
type: evergreen
created: 2026-04-18
source: "Emotion Concepts and their Function in a Large Language Model"
tags: [interpretability, representation-engineering, linear-probes, guardrails, research-methodology]
aliases:
  - "Generalizing linear decodability across concept domains requires a theory of which concepts become linearly decodable"
---

# Generalizing linear decodability across concept domains requires a theory of which concepts become linearly decodable

Source: [[emotion-concepts-and-their-function-in-a-large-language-model|Emotion Concepts and their Function in a Large Language Model]]

A demonstration that one concept family (e.g., emotions) is linearly decodable from model activations and stable across contexts does not, by itself, warrant the inference that arbitrary other concept families (e.g., healthcare conditions, legal categories, safety-relevant intents) will be equally decodable and stable. The warrant for such generalization is analogy: "both are concepts, so if one works, the other should." This is a weak warrant. Analogy is a suggestive prior, not evidence.

A stronger warrant would rest on an explicit theory of which concepts become linearly decodable in LLM activations. Candidate features of such a theory: frequency in training data, sharpness of category boundaries, degree of human linguistic standardization, relevance to next-token prediction, or the presence of dedicated feature directions in the residual stream. Until a theory of this form is articulated and tested, cross-domain generalization of representation-engineering findings should be treated as a hypothesis to be validated in each new domain, not a property that propagates freely from one demonstration.

The practical consequence is that engineering projects that rely on linear decodability in a new domain — for instance, building activation-level classification heads as guardrails for content outside the training distribution of the original interpretability study — should budget empirical validation in the new domain as a first-class step, rather than assuming transfer from published results.

**Open questions:**
- What is the minimal set of concept properties that predict linear decodability in transformer residual streams?
- Are there concept types that are reliably *not* linearly decodable, and do those have shared structural features?
- How stable is linear decodability across prompt variations within a single domain, let alone across domains?

## Links

- Context: [[high-level-semantic-features-in-transformer-residual-streams-are-encoded-as-approximately-linear-directions|High-level semantic features in transformer residual streams are encoded as approximately linear directions]]
- Context: [[representation-engineering-amortizes-cost-into-one-time-calibration-adding-near-zero-runtime-overhead|Representation engineering amortizes cost into one-time calibration, adding near-zero runtime overhead]]
- Context: [[interpretability-methods-that-explain-mechanism-do-not-scale-and-methods-that-scale-do-not-explain-mechanism|Interpretability methods that explain mechanism do not scale and methods that scale do not explain mechanism]]
