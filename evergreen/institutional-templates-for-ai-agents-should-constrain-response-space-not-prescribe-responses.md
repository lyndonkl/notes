---
type: evergreen
created: 2026-04-02
source: "Thought session: Is OTP the right fit for multi-agent AI architecture?"
tags: [institutional-design, multi-agent-systems, orchestration, soft-templates, AI-alignment]
aliases:
  - "Institutional templates for AI agents should constrain response space not prescribe responses"
---

# Institutional templates for AI agents should constrain response space not prescribe responses

Source: [[thought-session-otp-for-multi-agent-ai|Thought Session: Is OTP the Right Fit for Multi-Agent AI Architecture?]]

The Evans et al. paper argues that scalable AI alignment requires institutional templates — persistent structures of roles, norms, and protocols that govern agent behavior. But the comparison with OTP reveals that not all institutional templates are equal. OTP-style templates are deterministic supervision specs: if X happens, do Y. These are recipe cards. The institutional templates that multi-agent AI actually needs are closer to organizational norms and principles — guidelines that constrain the space of possible responses without prescribing the exact response.

The difference is between a supervision tree config that says "restart process with init/1 on crash" and an employee handbook that says "we support people through setbacks." The first specifies the outcome; the second shapes behavior while leaving room for adaptation. For AI agent systems, this means designing templates that define what kinds of actions are acceptable, what goals matter, and what values should guide decisions — without hardcoding the specific response to every situation. The agents themselves, powered by LLMs, would interpret and apply these guidelines contextually, much as human team members interpret organizational norms.

This refines the Evans et al. concept of institutional templates from a general prescription ("design institutions for AI") into a specific design principle: soft constraints over hard rules, response-space shaping over response prescription.

**Open questions:**
- How do you make soft templates enforceable? In human organizations, cultural norms are enforced through social pressure, performance reviews, and hiring/firing. What's the equivalent enforcement mechanism for AI agents operating under soft guidelines?
- Is there a risk that soft templates are too vague to produce reliable behavior? Where's the line between useful flexibility and dangerous ambiguity?
- Could LLMs themselves serve as the "interpretation layer" that translates soft templates into specific actions — essentially acting as the judgment that humans apply to organizational norms?

## Links

- Extends: [[scalable-ai-alignment-requires-institutional-templates-not-individual-virtue|Scalable AI alignment requires institutional templates not individual virtue]]
- Extends: [[otp-models-mechanical-orchestration-but-multi-agent-ai-needs-organic-orchestration|OTP models mechanical orchestration but multi-agent AI needs organic orchestration]]
- Context: [[activation-steering-could-enforce-behavioral-traits-in-llm-agents-without-consuming-prompt-context|Activation steering could enforce behavioral traits in LLM agents without consuming prompt context]]
