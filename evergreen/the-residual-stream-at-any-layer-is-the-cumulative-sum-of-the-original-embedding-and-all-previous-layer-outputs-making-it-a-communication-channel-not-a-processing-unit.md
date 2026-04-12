---
type: evergreen
created: 2026-04-11
source: "A Mathematical Framework for Transformer Circuits"
tags: [mechanistic-interpretability, residual-stream, transformer-architecture, communication-channel, skip-connections]
aliases:
  - "The residual stream at any layer is the cumulative sum of the original embedding and all previous layer outputs making it a communication channel not a processing unit"
---

# The residual stream at any layer is the cumulative sum of the original embedding and all previous layer outputs making it a communication channel not a processing unit

Source: [[a-mathematical-framework-for-transformer-circuits|A Mathematical Framework for Transformer Circuits]]

The residual stream at layer L equals the original token embedding plus the outputs of every layer from 1 through L, accumulated via element-wise addition. The stream never grows in dimensionality — each layer's output is the same size as the embedding, and it is added in place. This is the structural consequence of skip connections: rather than each layer transforming its input and passing the result forward, each layer computes a *contribution* and adds it to a running total.

The residual stream itself performs no computation. It simply accumulates. All processing happens inside the layers — attention heads and MLPs — which read from the stream via one linear transformation and write back to it via another. This makes the residual stream function as a shared communication channel: layers do not pass information to each other directly but instead broadcast through this shared linear accumulator. An attention head in layer 4 can read information that was written by a head in layer 1, not because they are connected, but because both interact with the same shared stream.

This framing also explains why the last token's final-layer representation is informationally rich enough to predict the next token. Through successive layers of attention, earlier tokens' information has been selectively moved into the last token's residual stream position. By the final layer, that single vector has accumulated contributions from every layer's processing of the full sequence context — it is a compressed summary of everything the model has computed.

**Open questions:**
- As layers accumulate, does the signal-to-noise ratio in the residual stream degrade, or do later layers learn to filter earlier noise?
- Is there a practical depth limit beyond which additional layers cannot meaningfully contribute because the accumulated stream becomes too crowded?
- How does the "communication channel" framing change when MLP layers are included — do they write qualitatively different information to the stream than attention heads do?

## Links

- Confirms: [[transformer-residual-stream-is-linear-space-permitting-feature-directions-despite-sublayer-nonlinearities|The transformer residual stream is the linear space that permits feature directions to exist despite nonlinearities in attention and MLP sublayers]]
- Context: [[the-transformer-residual-stream-has-no-privileged-basis-because-only-linear-operations-interact-with-it|The transformer residual stream has no privileged basis because only linear operations interact with it]]
