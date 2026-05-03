---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [agent-design, software-engineering, abstraction, refactoring, multi-agent-systems]
aliases:
  - "Agent design rediscovers the engineering practice of abstraction extraction through discovery rather than upfront planning"
---

# Agent design rediscovers the engineering practice of abstraction extraction through discovery rather than upfront planning

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

Software engineers have a well-developed practice for handling complexity through abstraction: notice that two pieces of code do similar things, extract the shared functionality into a function or class, and let the original sites call the abstraction. Object-oriented programming formalizes this with superclasses and inheritance.

Building agents recapitulates this practice but with a different temporal shape. Where traditional refactoring assumes you can name the abstraction once you see the duplication — and where good upfront design assumes you can predict the abstraction in advance — agent design surfaces the abstractions only through use. You build an agent for a forecasting task, then another for code review, then notice that both rely on a common pattern of evidence assessment. You extract that pattern as a reusable skill. You give one agent access to a particular dataset, then realize a second agent needs the same data, so you extract the data access into an MCP server. The abstractions are discovered, not designed.

This makes agent composition a continuation of an old engineering practice rather than a fundamentally new skill. The reason this isn't obvious to people outside agent design is that the abstraction targets are unfamiliar — skills, roles, teams, MCP-backed data servers — even though the move (extract reusable functionality into a callable unit) is the same.

**Open questions:**
- Does discovery-driven abstraction converge on the same architecture across builders, or do different people extract different skill libraries from the same domain experiences? If the latter, agent design is more like writing than engineering.
- At what scale does discovery-driven abstraction give way to upfront design? When teams compose teams, can the team-level structure be designed in advance, or does the organizational layer also have to be discovered?

## Links

- Extends: [[realizing-an-llms-general-capability-for-any-specific-purpose-requires-context-engineering-as-the-shaping-work-that-interface-mastery-used-to-perform|Realizing an LLM's general capability for any specific purpose requires context engineering as the shaping work that interface mastery used to perform]]
- Context: [[organizational-science-is-an-untapped-design-source-for-multi-agent-ai-systems|Organizational science is an untapped design source for multi-agent AI systems]]
- Context: [[otp-models-mechanical-orchestration-but-multi-agent-ai-needs-organic-orchestration|OTP models mechanical orchestration but multi-agent AI needs organic orchestration]]
