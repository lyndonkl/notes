---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [LLMs, engineering, information-theory, attention-mechanism, perception]
aliases:
  - "Engineers underestimate language model power because its load-bearing mechanism lives in information theory rather than engineering"
---

# Engineers underestimate language model power because its load-bearing mechanism lives in information theory rather than engineering

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

The standard engineering response to language models is dismissive: the model produces sometimes-unreliable code, the prompts are "just text," and the system feels like a fancy autocomplete. This response is widespread enough among technically sophisticated engineers to suggest a structural cause rather than individual failure to engage.

The structural cause is that the mechanism producing language model behavior — attention dynamics across enormous parameter spaces, the combinatorial structure of activation interactions — lives in information theory, not in software engineering. Engineers without information-theoretic background can see the surface output (text, sometimes-buggy code) but cannot see why the output behaves the way it does. Without the mechanism in view, the surface output is the only evidence available, and the surface output is evaluated by engineering criteria (correctness, reliability, performance) where the model's average-quality-across-everything property reads as inadequate.

This is a particular case of a more general failure mode: evaluating a system whose load-bearing mechanism you don't understand by criteria appropriate to systems whose mechanism you do understand. The engineer's evaluative frame is rigorous and earned, but it was earned in a different domain, and applying it to language models without first internalizing their mechanism produces a confident but mistaken assessment.

**Open questions:**
- Would an engineer who took the time to understand the attention mechanism and the parameter-space combinatorics actually update their assessment, or would the surface-quality concerns remain dominant?
- Are there other technical communities (e.g., applied mathematicians, signal processing engineers) whose existing frames are closer to information theory and who therefore see language models more accurately on first contact?

## Links

- Confirms: [[evaluating-agi-from-inside-one-specialty-hides-that-the-same-tool-generalizes-across-every-other-domain-too|Evaluating AGI from inside one specialty hides that the same tool generalizes across every other domain too]]
- Context: [[engineer-skepticism-that-ai-produces-bad-code-is-a-special-case-of-specialty-blindness-not-a-domain-specific-limitation|Engineer skepticism that AI produces bad code is a special case of specialty-blindness not a domain-specific limitation]]
