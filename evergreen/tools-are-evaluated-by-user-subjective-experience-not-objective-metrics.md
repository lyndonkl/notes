---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [tool-use, evaluation, subjective-experience, design-philosophy]
aliases:
  - "Tools are evaluated by user subjective experience not objective metrics"
---

# Tools are evaluated by user subjective experience not objective metrics

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

The question of whether a tool is doing its job does not bottom out in any metric measured external to the user. It bottoms out in whether the user, using the tool, finds that the work it enabled is what they wanted. A hammer that drives nails efficiently is not "doing its job" in a way settled by force-per-strike measurements; it is doing its job if the carpenter is satisfied with the joint that resulted. An IDE that compiles code quickly is not "doing its job" in a way settled by build times; it is doing its job if the developer's experience of writing code is supported. Tools serve human purposes, and the purposes are evaluated where the purposes live: in the user's experience of whether the work that mattered to them got done.

This is a general claim about tools, not specific to AI. AI is the case in which the gap between objective performance and subjective evaluation becomes most visible, because AI's outputs are sufficiently rich and ambiguous that two evaluators with the same metrics can come to opposite conclusions about whether the same output is good. The visibility of the divergence in AI is not new in tools; it is new in being unavoidable.

The implication is that any agentic AI system that optimizes for an objective metric without grounding in user evaluation eventually solves the wrong problem. The metric becomes the target, the target diverges from what the user wanted, and the tool stops doing its job in the only sense that matters.

**Open questions:**
- This claim is in tension with optimization-first design philosophies that treat user satisfaction as a noisy proxy for "real" performance metrics. Which view wins where? The tension is sharpest in domains where users have weak evaluative skill.
- Is "user subjective experience" the right grounding, or should it be "the user's actual interests" (which may diverge from their experience)? The first is operationally cleaner; the second is normatively stronger.

## Links

- Context: [[the-ultimate-feedback-signal-in-agentic-ai-is-human-subjective-satisfaction-not-objective-outcome|The ultimate feedback signal in agentic AI is human subjective satisfaction not objective outcome]]
