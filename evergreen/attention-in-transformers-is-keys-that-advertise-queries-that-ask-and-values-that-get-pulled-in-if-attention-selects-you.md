---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [LLMs, attention, pedagogy, transformers, mechanism, plain-language]
aliases:
  - "Attention in transformers is keys that advertise queries that ask and values that get pulled in if attention selects you"
---

# Attention in transformers is keys that advertise queries that ask and values that get pulled in if attention selects you

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

Each token in a transformer learns to play three roles simultaneously, and the entire attention mechanism is the interaction of these three roles. Keys advertise what information the token has — they are what the token broadcasts to other tokens looking for relevant information. Queries ask what information the token needs — they are what the token sends out to find relevant tokens. Values are the content that gets pulled in if attention selects you — they are what flows from one token to another when a query and a key match.

The model learns these three representations per token from the training data. Nothing about the role assignment is hand-coded; what makes "the" useful as a determiner that signals "a noun is coming" is learned from billions of examples of that pattern. At inference time, every token simultaneously emits a query and a key and a value, and at each layer every token decides which other tokens to listen to based on how well its query matches another token's key. When the match is high, the value flows in; when the match is low, it does not.

This three-role framing is what makes attention more interesting than a simple lookup table. A token does not just retrieve information from a fixed memory; it actively shapes what it advertises (key), what it requests (query), and what it shares if attended to (value), and all three are determined by the model's learned representations of meaning, structure, and context. The mechanism is general — it does not specialize to language; it specializes to whatever the data trains it on, which is part of why the same architecture works for code, biology, music, and dozens of other domains.

**Open questions:**
- The advertise/ask/pull-in framing is pedagogical and lossy. It makes the mechanism intuitive but elides the actual mathematics (dot products, softmax, weighted sums) that make it precise. Where does the framing mislead, and where is it precise enough to be a reliable mental model?
- Multi-head attention runs many such interactions in parallel with different learned representations. The framing handles single-head attention cleanly; how does it extend to make the multi-head extension intuitive without losing the simplicity that makes the framing useful?

## Links

- Extends: [[engineers-underestimate-language-model-power-because-its-load-bearing-mechanism-lives-in-information-theory-rather-than-engineering|Engineers underestimate language model power because its load-bearing mechanism lives in information theory rather than engineering]]
- Context: [[stacking-attention-layers-tends-to-build-a-hierarchy-from-local-structure-to-abstract-concepts-though-layer-boundaries-are-fuzzy|Stacking attention layers tends to build a hierarchy from local structure to abstract concepts though layer boundaries are fuzzy]]
- Context: [[attention-heads-apply-no-nonlinearity-to-value-vectors-softmax-governs-routing-but-content-movement-is-a-linear-weighted-sum|Attention heads apply no nonlinearity to value vectors: softmax governs routing but content movement is a linear weighted sum]]
- Context: [[the-residual-stream-at-any-layer-is-the-cumulative-sum-of-the-original-embedding-and-all-previous-layer-outputs-making-it-a-communication-channel-not-a-processing-unit|The residual stream at any layer is the cumulative sum of the original embedding and all previous layer outputs making it a communication channel not a processing unit]]
