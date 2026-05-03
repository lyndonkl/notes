---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [LLMs, capability-bounds, human-agent-loop, agent-design, empirical-observation]
aliases:
  - "Language models reliably complete 60 to 90 percent of a task with the remaining gap requiring varying degrees of human effort"
---

# Language models reliably complete 60 to 90 percent of a task with the remaining gap requiring varying degrees of human effort

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

Across the agent teams I have built — household financial management, marathon training, fantasy sports analysis, investment research, software development — language models do not "fail" on the tasks I assign them. They reliably complete 60 to 90 percent of any given task. What varies across domains and across specific tasks is how much human effort the remaining gap requires.

This refines the cruder "bounded at exploitation" framing. The model is not stopped at some hard ceiling that prevents the work from finishing. The work usually does finish. The honest empirical question is: across what kinds of tasks does the gap close cheaply (a quick review, a small adjustment) versus expensively (substantive iteration, judgment calls, repeated evaluation)? The shape of the gap varies; the existence of a gap does not.

This empirical observation is the ground truth that everything in the human-agent loop argument rests on. Without it, one would either overclaim AI capability ("the model handles it end-to-end") or underclaim it ("the model cannot do this kind of work at all"). The accurate frame is that the model gets you most of the way, and the question worth asking is what specifically the remaining gap is made of.

**Open questions:**
- Does the 60–90 figure hold across genuinely diverse domain types, or is it specific to the kinds of tasks I work on (analysis-heavy, decision-adjacent)? An empirical question worth tracking across more domains.
- Is the gap-completion effort decreasing as models improve, or is it migrating — different kinds of human effort taking the place of the kinds that go away?

## Links

- Extends: [[language-models-are-strong-at-exploration-but-bounded-at-exploitation|Language models are strong at exploration but bounded at exploitation]]
- Context: [[realizing-an-llms-general-capability-for-any-specific-purpose-requires-context-engineering-as-the-shaping-work-that-interface-mastery-used-to-perform|Realizing an LLM's general capability for any specific purpose requires context engineering as the shaping work that interface mastery used to perform]]
