---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [AGI, LLMs, context-engineering, agent-design, generality]
aliases:
  - "Realizing an LLM's general capability for any specific purpose requires context engineering as the shaping work that interface mastery used to perform"
---

# Realizing an LLM's general capability for any specific purpose requires context engineering as the shaping work that interface mastery used to perform

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

The collapse of specialized tool interfaces into a single text medium does not eliminate the work of using a tool — it relocates it. Where a financial analyst once spent years learning Excel formulas and a biochemist learned to operate PCR machines, the user of an LLM spends their effort engineering context: deciding what the model should know about the situation, what role it should adopt, what skills it should compose, what data sources it should access, and what constraints it should operate under.

This is why the "general" in AGI is invisible to people who use AI in chat-based question-and-answer mode. Without the shaping work, the LLM defaults to its average behavior across all domains, which is competent but mediocre per domain. The generality is intrinsic to the tool, but its realization for any specific purpose is loaned to the user — through context.

This explains why people working in different modes report wildly different perceptions of LLM capability. Q&A users see a chat assistant. Engineers using agents on bounded coding problems see a coding helper. Builders composing skills, roles, and teams see a substrate for unbounded work. They are all using the same model. They are doing different amounts and kinds of shaping. The taxonomy of usage modes is not a separate observation from the AGI claim — one is the cause of how the other appears.

**Open questions:**
- Is "context engineering" the right term, or a placeholder? It implies craft but understates the architectural and orchestration work involved when shaping extends to multi-agent systems.
- This implies a literacy asymmetry: the value an LLM produces for a user scales with that user's shaping skill. Is that asymmetry transient (as defaults improve) or permanent (the price of using a general tool well)?

## Links

- Extends: [[llms-collapse-the-specialized-interfaces-of-every-prior-domain-tool-into-a-single-universal-medium-of-text|LLMs collapse the specialized interfaces of every prior domain tool into a single universal medium of text]]
- Confirms: [[intelligence-scales-through-social-organization-not-individual-cognitive-upgrades|Intelligence scales through social organization not individual cognitive upgrades]]
- Context: [[organizational-science-is-an-untapped-design-source-for-multi-agent-ai-systems|Organizational science is an untapped design source for multi-agent AI systems]]
