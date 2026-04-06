---
type: source-note
source_type: document
title: "Thought session: Is OTP the right fit for multi-agent AI architecture?"
author: "Kushal (self)"
date_read: 2026-04-02
url: "https://github.com/lyndonkl/learning-erlang-otp"
tags: [OTP, Erlang, Elixir, multi-agent-systems, architecture-evaluation, thought-session]
---

# Thought Session: Is OTP the Right Fit for Multi-Agent AI Architecture?

## Metadata
- **Author:** Kushal (self)
- **Context:** After completing 26 Livebook notebooks learning Erlang/OTP through Elixir (Phases 1-3: Core Elixir, Concurrency Model, OTP Behaviours)
- **Read on:** 2026-04-02
- **Reading depth:** Thought Mode (Socratic dialogue)

## The Big Question
Can the challenges I face in multi-agent AI architecture — dynamic role assignment, inter-agent communication, emergent hierarchy, output validation — be solved using Erlang/OTP, or is OTP designed for a fundamentally different problem shape?

## Core Argument
Through systematic pressure-testing, each claimed advantage of OTP for multi-agent AI was found insufficient for this specific use case. OTP excels at high-concurrency, lightweight, stateless systems (telecom, chat, IoT) — but LLM-based multi-agent systems have few, heavyweight, stateful agents bottlenecked by API rate limits. More fundamentally, OTP models mechanical orchestration (deterministic restart rules) while multi-agent AI needs organic orchestration (fuzzy guidelines that constrain response space without prescribing responses).

## My Assessment
The learning wasn't wasted — OTP is a concrete example of organizational science applied to process coordination, and the patterns (supervision hierarchies, role separation, fault isolation) are valuable mental models. But the implementation doesn't fit my use case. The most valuable insight was the distinction between mechanical and organic orchestration, which refines what the Evans et al. paper means by "institutional templates."

## Evergreen Notes Extracted
- [[otp-is-designed-for-millions-of-lightweight-stateless-processes-llm-agent-systems-have-few-heavyweight-stateful-ones|OTP is designed for millions of lightweight stateless processes — LLM agent systems have few heavyweight stateful ones]]
- [[otp-models-mechanical-orchestration-but-multi-agent-ai-needs-organic-orchestration|OTP models mechanical orchestration but multi-agent AI needs organic orchestration]]
- [[institutional-templates-for-ai-agents-should-constrain-response-space-not-prescribe-responses|Institutional templates for AI agents should constrain response space not prescribe responses]]

## Follow-Up
- What does "organic orchestration" actually look like in code? If not OTP supervision specs, then what?
- Are there existing frameworks that model fuzzy guidelines rather than deterministic rules?
- How do you implement "soft institutional templates" for AI agent coordination?
- The learning of OTP patterns (supervision trees, restart strategies, role separation) may still inform architecture design in other languages
