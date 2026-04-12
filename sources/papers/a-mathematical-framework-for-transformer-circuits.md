---
type: source-note
source_type: paper
title: "A Mathematical Framework for Transformer Circuits"
author: "Nelson Elhage, Neel Nanda, Catherine Olsson, Tom Henighan, Nicholas Joseph, Ben Mann, Amanda Askell, Yuntao Bai, Anna Chen, Tom Conerly, Nova DasSarma, Dawn Drain, Deep Ganguli, Zac Hatfield-Dodds, Danny Hernandez, Andy Jones, Jackson Kernion, Liane Lovitt, Kamal Ndousse, Dario Amodei, Tom Brown, Jack Clark, Jared Kaplan, Sam McCandlish, Chris Olah"
date_read: 2026-04-11
url: "https://transformer-circuits.pub/2021/framework/index.html"
tags: [mechanistic-interpretability, transformer-circuits, residual-stream, attention-heads, reverse-engineering]
---

# A Mathematical Framework for Transformer Circuits

## Metadata
- **Author:** Elhage, Nanda, Olsson, et al. (Anthropic)
- **Published:** 2021
- **Read on:** 2026-04-11
- **Reading depth:** Pass 1 + partial Pass 2 (Transformer Overview section only; stopped intentionally to redirect to representation-engineering-aligned work)

## The Big Question
Can we reverse engineer the computations performed by transformers into human-interpretable circuits, analogous to reverse engineering compiled binaries into source code? And can a mathematical framework make this tractable?

## Core Argument
The paper develops a mathematical framework for decomposing transformer computations into interpretable circuits by exploiting the linear, additive structure of the residual stream. By simplifying to attention-only transformers (no MLPs), the authors show that attention heads can be analyzed as independent, additive units that move information through the residual stream, and that their function can be decomposed into independent QK (routing) and OV (content) circuits. They validate this framework by reverse engineering zero-layer (bigram), one-layer (skip-trigram), and two-layer (induction head) models directly from weights. The framework introduces key concepts including virtual weights, path expansion, and three types of attention head composition.

## My Assessment
The paper's primary contribution is a framework — a way of thinking about transformer internals — not just a catalog of findings. The attention-only simplification is legitimate for studying information flow but has a known ceiling: it cannot account for the nonlinear transformations MLPs perform. The jargon is dense for someone entering the field, though the structure (zero → one → two layers) is well-organized. I extracted three significant insights from the Transformer Overview section before deciding to redirect: the linearity of attention's value combination, the no-privileged-basis property of the residual stream, and the residual stream as cumulative communication channel. These conceptual foundations are directly relevant to representation engineering work. The detailed mathematical machinery (path expansion, virtual weights, skip-trigram analysis, induction heads) was not pursued — my interest lies in top-down representation engineering rather than bottom-up circuit analysis.

## Evergreen Notes Extracted
- [[attention-heads-apply-no-nonlinearity-to-value-vectors-softmax-governs-routing-but-content-movement-is-a-linear-weighted-sum|Attention heads apply no nonlinearity to value vectors — softmax governs routing but content movement is a linear weighted sum]]
- [[the-transformer-residual-stream-has-no-privileged-basis-because-only-linear-operations-interact-with-it|The transformer residual stream has no privileged basis because only linear operations interact with it]]
- [[the-residual-stream-at-any-layer-is-the-cumulative-sum-of-the-original-embedding-and-all-previous-layer-outputs-making-it-a-communication-channel-not-a-processing-unit|The residual stream at any layer is the cumulative sum of the original embedding and all previous layer outputs making it a communication channel not a processing unit]]

## Follow-Up
- Concepts not covered that may be worth returning to: skip-trigrams, three types of composition (K-composition, Q-composition, V-composition), induction heads, virtual attention heads
- The emotions paper (Emotion Concepts and their Function in a Large Language Model, Anthropic 2026) uses representation engineering methods on the same residual stream substrate described here — read next
- Neel Nanda's blog on getting into mechanistic interpretability — referenced as parallel resource
