---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [agent-design, text-as-substrate, composability, engineering, abstraction]
aliases:
  - "Text is harder for engineers to perceive as a composable substrate than code even though the underlying abstraction practice transfers cleanly"
---

# Text is harder for engineers to perceive as a composable substrate than code even though the underlying abstraction practice transfers cleanly

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

The engineering practice of identifying repeated patterns and extracting them as reusable abstractions transfers cleanly to agent design — building one agent surfaces patterns that, when extracted as skills, can be composed across many agents. The practice itself is the same skill software engineers have used for decades. What does not transfer cleanly is the perception of *text* as a substrate where this practice applies.

Code composability is operationally visible. A function has parameters and a return value; a class has methods and inheritance; a module exposes an interface and hides implementation. The structural units of composition are syntactically marked, and the engineer can see at a glance where the abstraction boundaries are. Text has no such markers. Two prompts that share underlying logic look like two prompts; the abstraction that could unify them is invisible until the engineer learns to read text the way they read code.

This explains the surprisingly common engineering reaction that agent design is "just prompts." The engineer is correct that prompts are text, and incorrect that text-being-text precludes the same engineering moves they make in code. The skill applies; the perception of where to apply it has to be developed separately. Until that perception develops, the engineer sees a flat undifferentiated mass of prompts and concludes there is nothing to abstract.

**Open questions:**
- Does this perceptual shift happen automatically with enough hands-on exposure, or does it require explicit training (e.g., reading other people's well-abstracted skill libraries)?
- Are there design tools or visual aids that could make text composability as visible as code composability — for instance, ways of marking shared semantic structures across prompts?

## Links

- Extends: [[agent-design-rediscovers-the-engineering-practice-of-abstraction-extraction-through-discovery-rather-than-upfront-planning|Agent design rediscovers the engineering practice of abstraction extraction through discovery rather than upfront planning]]
- Context: [[systems-knowledge-is-what-converts-cross-domain-literacy-into-reusable-agent-infrastructure-that-can-act-on-it|Systems knowledge is what converts cross-domain literacy into reusable agent infrastructure that can act on it]]
