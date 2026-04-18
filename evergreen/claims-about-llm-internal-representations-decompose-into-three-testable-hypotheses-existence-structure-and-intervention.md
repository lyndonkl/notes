---
type: evergreen
created: 2026-04-18
source: "Emotion Concepts and their Function in a Large Language Model"
tags: [interpretability, research-methodology, reading-frame, hypothesis-decomposition]
aliases:
  - "Claims about LLM internal representations decompose into three testable hypotheses: existence, structure, and intervention"
---

# Claims about LLM internal representations decompose into three testable hypotheses: existence, structure, and intervention

Source: [[emotion-concepts-and-their-function-in-a-large-language-model|Emotion Concepts and their Function in a Large Language Model]]

Most claims that "LLMs represent X" collapse three independently testable hypotheses into one. Separating them sharpens evaluation and reveals which parts of a paper's argument are actually supported by its evidence.

**Existence.** Is a representation of X present in the model's activations? This is the lowest bar and typically demonstrated via probing or linear decoding. A successful existence test shows correlation between a direction in activation space and the target concept, but does not show that the direction is functionally used.

**Structure.** How is the representation geometrically organized? Does it cluster, project onto low-dimensional axes that correspond to a meaningful taxonomy, or form hierarchies? Structure claims depend on existence but go further — they assert something about internal organization and its relationship to external theories (e.g., human affect geometry).

**Intervention.** Does causally manipulating the representation change model behavior? This is the strongest hypothesis because it establishes functional role, not just presence. Intervention evidence can be further divided into sufficiency (manipulation changes output) and necessity (ablating the representation removes the behavior); most activation-steering papers establish the former but not the latter.

Using this frame as a reading lens catches conflation: a paper that only tests existence but concludes "LLMs use X to produce behavior Y" is overreaching; a paper that tests intervention but not structure is agnostic about how the representation is organized. For a reader, the frame converts vague impressions into a checklist — for each of the three hypotheses, what evidence does this paper provide, and at what strength?

**Open questions:**
- Are there intermediate hypotheses between structure and intervention — e.g., a "selective use" hypothesis that the representation is read by specific downstream circuits but not others?
- How should the frame adapt for multimodal models, where "representation" may refer to shared or modality-specific structures?

## Links

- Context: [[correlation-between-direction-and-concept-is-evidence-for-presence-not-function-only-causal-intervention-proves-implementation|Correlation between direction and concept is evidence for presence, not function; only causal intervention proves implementation]]
- Context: [[interpretability-methods-that-explain-mechanism-do-not-scale-and-methods-that-scale-do-not-explain-mechanism|Interpretability methods that explain mechanism do not scale and methods that scale do not explain mechanism]]
- Context: [[mechanistic-interpretability-and-representation-engineering-answer-different-questions-using-incompatible-units-of-analysis|Mechanistic interpretability and representation engineering answer different questions using incompatible units of analysis]]
