---
type: source-note
source_type: document
title: "Thought session: Multi-agent communication challenges"
author: "Kushal (self)"
date_read: 2026-04-03
url: ""
tags: [multi-agent-systems, conversation-mechanics, agent-architecture, coordination, thought-session]
---

# Thought Session: Multi-Agent Communication Challenges

## Metadata
- **Author:** Kushal (self)
- **Context:** Ongoing exploration of engineering challenges in multi-agent AI systems, following OTP evaluation session
- **Read on:** 2026-04-03
- **Reading depth:** Thought Mode (Socratic dialogue, partially complete — conversational mechanics and authority enforcement explored, task assignment and discovery remaining)

## The Big Question
What are the fundamental engineering challenges in building multi-agent LLM systems that communicate and coordinate effectively, and how should they be solved?

## Core Challenges Identified
Three clusters of challenges were identified: (1) task assignment and information flow at scale (2→10→20 agents), (2) conversational mechanics (think/speak separation, turn-taking, conversation termination, multi-party dynamics), and (3) discovery and authority enforcement (agent/information discovery, hierarchical structures, enforcing decisions). The session focused on conversational mechanics as the most foundational cluster.

## My Assessment
The dual-prompt architecture evolved into a three-module agent design (observer, thinker, speaker) sharing a global workspace. The when-to-speak problem splits into two distinct sub-problems: starting (external signals, solvable by the observer) and stopping (requires feedback that doesn't exist in text-only API interactions). Two competing approaches emerged: activation-space observation (rich but requires local models) and text-native conversational protocols (practical with any LLM). Authority enforcement via activation steering was explored in depth: the Interpersonal Circumplex (Agency + Communion) provides a minimal two-axis framework, emotional valence may be upstream of behavioral traits in activation space (per Anthropic's 171 emotion vectors), and enforcement decomposes into a three-stage research pipeline (taxonomy → mapping → heuristics). Key insight: activation steering could bypass prompt-based behavioral enforcement entirely, freeing context window for task content.

## Evergreen Notes Extracted
- [[llm-agents-need-separate-modules-for-observation-reasoning-and-speech|LLM agents need separate modules for observation reasoning and speech]]
- [[the-when-to-speak-problem-in-multi-agent-ai-has-two-distinct-sub-problems-when-to-start-and-when-to-stop|The when-to-speak problem in multi-agent AI has two distinct sub-problems — when to start and when to stop]]
- [[text-native-conversational-protocols-may-be-more-practical-than-activation-space-observation-for-coordinating-llm-agents|Text-native conversational protocols may be more practical than activation-space observation for coordinating LLM agents]]
- [[activation-steering-could-enforce-behavioral-traits-in-llm-agents-without-consuming-prompt-context|Activation steering could enforce behavioral traits in LLM agents without consuming prompt context]]
- [[emotional-valence-may-be-upstream-of-behavioral-traits-in-transformer-activation-space|Emotional valence may be upstream of behavioral traits in transformer activation space]]
- [[the-interpersonal-circumplex-provides-a-minimal-two-axis-model-for-multi-agent-behavioral-dimensions|The Interpersonal Circumplex provides a minimal two-axis model for multi-agent behavioral dimensions]]
- [[enforcing-behavioral-norms-in-llm-agents-requires-a-three-stage-research-pipeline|Enforcing behavioral norms in LLM agents requires a three-stage research pipeline]]
- [[the-dyadic-agent-conversation-problem-must-be-solved-before-multi-party-dynamics-become-tractable|The dyadic agent conversation problem must be solved before multi-party dynamics become tractable]]

## Follow-Up (Remaining Challenge Clusters)
- Task assignment at scale: help desk patterns, A2A protocol, skill advertisement
- Discovery at scale: semantic search limitations, organizational structures (Confluence-like knowledge bases)
- Authority enforcement: further research into activation steering implementation, empirical validation of Circumplex mapping to activation space
- Multi-party conversation dynamics: not yet explored
