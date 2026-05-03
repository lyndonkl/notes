---
type: structure-note
created: 2026-05-03
tags: [AGI, LLMs, intrinsic-vs-loaned, generality, context-engineering]
---

# Intrinsic Generality and Loaned Realization: How LLMs Differ from Every Prior Tool

The historical novelty of LLMs is not "as capable as humans" but the combination of two intrinsic properties that no prior tool ever combined: general-purpose knowledge contained in the tool itself, and a single universal interface (text) that collapses the specialized interfaces of every prior domain tool. Realizing that intrinsic generality for any specific purpose still requires shaping work, but that work has moved from interface mastery to context engineering — and the empirical pattern across many domains is that the model completes 60–90% of the task with the human supplying the rest at the act-of-decision moment. The pattern that runs through every claim in this cluster: substrate is intrinsic, realization is loaned.

## Core Notes

- [[the-llm-is-a-substrate-of-intrinsic-generality-whose-realization-in-the-world-is-loaned-by-humans-through-context-direction-and-evaluation|The LLM is a substrate of intrinsic generality whose realization in the world is loaned by humans through context, direction, and evaluation]] — The organizing spine: the fundamental pattern that structures all five session arcs
- [[llms-are-the-first-tools-whose-general-purpose-knowledge-is-contained-in-the-tool-itself-rather-than-supplied-by-the-user|LLMs are the first tools whose general-purpose knowledge is contained in the tool itself rather than supplied by the user]] — The intrinsic half: what makes LLMs historically unique
- [[llms-collapse-the-specialized-interfaces-of-every-prior-domain-tool-into-a-single-universal-medium-of-text|LLMs collapse the specialized interfaces of every prior domain tool into a single universal medium of text]] — The complementary novelty: universal interface paired with intrinsic knowledge
- [[realizing-an-llms-general-capability-for-any-specific-purpose-requires-context-engineering-as-the-shaping-work-that-interface-mastery-used-to-perform|Realizing an LLM's general capability for any specific purpose requires context engineering as the shaping work that interface mastery used to perform]] — The realization half: how the loaning works in practice
- [[language-models-are-strong-at-exploration-but-bounded-at-exploitation|Language models are strong at exploration but bounded at exploitation]] — The empirical boundary: maps where realization succeeds and where it requires human completion
- [[language-models-reliably-complete-60-to-90-percent-of-a-task-with-the-remaining-gap-requiring-varying-degrees-of-human-effort|Language models reliably complete 60 to 90 percent of a task with the remaining gap requiring varying degrees of human effort]] — The refinement: quantifies the loaning pattern across diverse domains
- [[the-gap-between-language-model-output-and-complete-work-lives-at-the-act-of-decision-moment-not-the-analysis-moment|The gap between language model output and complete work lives at the act-of-decision moment not the analysis moment]] — Locates the boundary: analysis is loaned by the model; decisions remain human

## Borderline / Adjacent

- [[agent-design-rediscovers-the-engineering-practice-of-abstraction-extraction-through-discovery-rather-than-upfront-planning|Agent design rediscovers the engineering practice of abstraction extraction through discovery rather than upfront planning]] — Related: applies the loaning pattern to agent team design but focuses on architectural discovery method rather than the generality/realization split itself

## Open Questions

- Does the intrinsic/loaned distinction remain stable as model capability improves, or does the loaned half progressively shrink? At minimum the loaned half could compress (better defaults reducing required shaping) without the intrinsic half ever absorbing it entirely.
- The intrinsic half rests on architecture-specific properties (transformer attention, parameter scale). What happens to the cluster if the underlying architecture shifts to something fundamentally different?
- Is "context engineering" the right term for the realization work, or a placeholder that understates the architectural and orchestration scope of what's actually involved?

## Connections to Other Clusters

- [[loaned-agency-why-the-human-agent-loop-is-permanent-not-transitional|Loaned Agency: Why the Human-Agent Loop Is Permanent, Not Transitional]] — Realization of generality requires loaned agency; the two clusters are halves of the same pattern at different scales
- [[intelligence-as-a-property-of-social-systems-not-individual-agents|Intelligence as a Property of Social Systems, Not Individual Agents]] — The intrinsic knowledge in LLMs IS social intelligence (trained on human text); confirms intelligence is a property of collective production, not the individual model
