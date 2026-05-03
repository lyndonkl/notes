---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [LLMs, attention, layer-hierarchy, mechanistic-interpretability, transformers, abstraction, pedagogy]
aliases:
  - "Stacking attention layers tends to build a hierarchy from local structure to abstract concepts though layer boundaries are fuzzy"
---

# Stacking attention layers tends to build a hierarchy from local structure to abstract concepts though layer boundaries are fuzzy

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

A single attention layer routes information among tokens based on per-token query-key matches, with values flowing where matches are high. A single layer alone is limited — it can attend over local relationships but cannot build representations more abstract than its inputs. What makes transformers powerful is that attention layers are stacked, and the routing at each layer operates on the representations produced by all previous layers.

The broad shape that mechanistic interpretability research tends to find is roughly this: early layers attend over local syntactic and structural relationships (which words go with which, what role each token plays in the sentence); middle layers attend over context (what this passage is about, what the entities and relationships in it are); deeper layers attend over abstract concepts and their associations (this passage is making an argument that connects X to Y, this code is implementing a particular pattern). Each layer's routing operates on representations that are themselves the product of routing in earlier layers, which is what produces compositional depth.

This is a pedagogical heuristic, not a clean empirical fact. The boundaries between "structural" and "contextual" and "conceptual" layers are fuzzy; specific features can appear at unexpected depths; interpretability work has found circuits that span many layers and features that resist clean layer-type labels. The honest version of the claim is that depth-of-composition is what enables a model to operate at multiple levels of abstraction simultaneously, and that the levels do tend to order roughly from local to abstract as you move deeper, but the picture is messier than the heuristic suggests.

The implication for understanding what LLMs are doing is that the model's apparent ability to reason at high levels of abstraction is not a separate cognitive faculty bolted on top of a language model. It is the same attention mechanism applied recursively, with each layer producing representations that subsequent layers can route over. The depth is the cognition.

**Open questions:**
- How many layers are needed before the hierarchy stabilizes? Empirically the answer seems to depend on task and architecture, but no clean theory predicts the minimum depth for any given level of abstraction.
- Does the hierarchy claim hold for non-language domains (vision, code, music)? The same architecture shows similar depth effects, but the layer-type labels (structural / contextual / conceptual) may not transfer cleanly.
- The claim that "depth is the cognition" is suggestive but underspecified. Are there cognitive operations that depth alone cannot produce — that would require a different architectural ingredient?

## Links

- Extends: [[attention-in-transformers-is-keys-that-advertise-queries-that-ask-and-values-that-get-pulled-in-if-attention-selects-you|Attention in transformers is keys that advertise queries that ask and values that get pulled in if attention selects you]]
- Confirms: [[emotion-representations-in-llms-develop-through-layer-wise-refinement-from-lexical-to-contextual-encoding|Emotion representations in LLMs develop through layer-wise refinement from lexical to contextual encoding]]
- Context: [[engineers-underestimate-language-model-power-because-its-load-bearing-mechanism-lives-in-information-theory-rather-than-engineering|Engineers underestimate language model power because its load-bearing mechanism lives in information theory rather than engineering]]
- Context: [[high-level-semantic-features-in-transformer-residual-streams-are-encoded-as-approximately-linear-directions|High-level semantic features in transformer residual streams are encoded as approximately linear directions]]
