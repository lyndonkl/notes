---
type: evergreen
created: 2026-04-02
source: "Thought session: Is OTP the right fit for multi-agent AI architecture?"
tags: [OTP, Erlang, multi-agent-systems, LLM, architecture-mismatch, fault-tolerance]
aliases:
  - "OTP is designed for millions of lightweight stateless processes — LLM agent systems have few heavyweight stateful ones"
---

# OTP is designed for millions of lightweight stateless processes — LLM agent systems have few heavyweight stateful ones

Source: [[is-otp-the-right-fit-for-multi-agent-ai-architecture|Is OTP the right fit for multi-agent AI architecture?]]

OTP's fault tolerance model rests on a core assumption: that process state is cheap to reconstruct. When a GenServer crashes, the supervisor calls init/1 fresh — internal state and mailbox are lost. This works brilliantly for telecom switches, chat servers, and IoT brokers where processes are stateless or derive state from external sources. But LLM-based AI agents accumulate rich conversational context, memory, and task progress that cannot be cheaply reconstructed. A crash that wipes an agent's accumulated intelligence is not a recoverable event without an explicit persistence layer — and once you add that layer, OTP's supervision model offers little beyond what Kubernetes or systemd provides.

The scale mismatch compounds the problem. OTP's lightweight processes (2-3 KB each, microseconds to spawn) shine when you need millions of concurrent connections. But a realistic multi-agent AI system runs 50-100 agents, not 10,000. At that scale, memory footprint is irrelevant, process discovery is trivial in any language, and the real bottleneck is LLM API latency and cost — constraints that OTP cannot address. The BEAM's elegant concurrency model solves a problem that LLM-based multi-agent systems simply don't have.

**Open questions:**
- Could AI agents be redesigned to be more stateless — pulling context from a shared store on each invocation rather than accumulating internal state? Would that change the calculus?
- Are there hybrid approaches where OTP manages the communication infrastructure while a persistence layer handles agent state?

## Links

- Context: [[otp-models-mechanical-orchestration-but-multi-agent-ai-needs-organic-orchestration|OTP models mechanical orchestration but multi-agent AI needs organic orchestration]]
- Extends: [[organizational-science-is-an-untapped-design-source-for-multi-agent-ai-systems|Organizational science is an untapped design source for multi-agent AI systems]]
