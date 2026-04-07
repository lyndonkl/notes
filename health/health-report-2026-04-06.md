---
type: health-report
date: 2026-04-06
tags: [system]
---

# Vault Health Report — 2026-04-06

## Summary
| Metric | Value | Trend |
|---|---|---|
| Total evergreen notes | 26 | New vault (recovered today) |
| Total source notes | 5 | — |
| Total structure notes | 3 | — |
| Orphan count (true + functional) | 2 | — |
| Avg outbound links per evergreen | 3.6 | Good (target 3–6) |
| Duplicate pairs detected | 0 | Excellent |
| Stale inbox items | 0 | Excellent (inbox empty) |
| Under-extracted sources | 0 | Excellent (3–8 per source) |
| Weak titles | 0 | Excellent (all declarative) |

## Overall Assessment

The vault recovered from corruption today is in **excellent structural health**. All 26 evergreen notes use consistent, declarative titles and are well-linked (avg 3.6 outbound links, well within the 3–6 target). Source-to-evergreen extraction is healthy across all five sources (range 3–8 evergreen per source). Two notes have low connectivity and warrant attention, but there are no duplicates, no stale inbox, and the three structure notes are coherent clusters with no overgrowth. The vault is ready for active use.

## Findings

### Critical (Act Now)
None. The vault is structurally sound.

### Advisory (Act Soon)

**Low Link Density (2 notes)** — Two evergreen notes have only 2 inbound links when the median is 4:
- [[otp-is-designed-for-millions-of-lightweight-stateless-processes-llm-agent-systems-have-few-heavyweight-stateful-ones|OTP is designed for millions of lightweight stateless processes]] (2 inbound, 3 outbound)
- [[reference-class-forecasting-outperforms-inside-view-estimation-for-project-timelines|Reference class forecasting outperforms inside-view estimation for project timelines]] (2 inbound, 4 outbound)
- [[the-dyadic-agent-conversation-problem-must-be-solved-before-multi-party-dynamics-become-tractable|The dyadic agent conversation problem must be solved before multi-party dynamics become tractable]] (2 inbound, 4 outbound)
- [[people-often-demand-extraordinary-evidence-for-ordinary-claims-when-the-claim-is-inconvenient-rather-than-unlikely|People often demand extraordinary evidence for ordinary claims]] (2 inbound, 4 outbound)
- [[detail-in-a-plan-increases-perceived-accuracy-but-decreases-actual-accuracy|Detail in a plan increases perceived accuracy]] (2 inbound, 3 outbound)

These notes are legitimate and well-written but may be peripheral to the main argument clusters. Monitor during next reading pass — they may need additional bridging links to the core themes.

### Informational

**Source-to-Evergreen Ratio (Healthy)** — All sources exceeded the 3-note minimum:
- "A First Look at Bayes (Arbital)" → 5 evergreen notes
- "Map-Territory Rationality" → 6 evergreen notes
- "Thought session: Multi-agent communication challenges" → 8 evergreen notes (dense but well-clustered)
- "Thought session: Is OTP the right fit for multi-agent AI architecture?" → 3 evergreen notes
- "Agentic AI and the next intelligence explosion" → 4 evergreen notes

**Link Network Density** — Evergreen notes have strong bidirectional connectivity:
- Median inbound links: 4
- Median outbound links: 4
- No orphans (all notes have at least 2 inbound and 3 outbound)
- Hub notes (5+ inbound): activation-steering, enforcing-behavioral-norms, institutional-templates, intelligence-scales, organizational-science, otp-models-mechanical, scalable-alignment, the-when-to-speak (8 hubs out of 26 = 31% hub density, healthy)

**Structure Coherence** — All three structure notes are thematically tight and well-populated:
- [[intelligence-as-a-property-of-social-systems-not-individual-agents|Intelligence as a property of social systems]] (7 members) — Organizational science frame; solidly coherent
- [[steering-agent-behavior-through-representation|Steering agent behavior through representation]] (7 members) — Activation steering taxonomy; sharply focused
- [[the-multi-agent-conversation-problem-decomposes-into-specific-subproblems|The multi-agent conversation problem decomposes into specific subproblems]] (6 members) — Conversation mechanics; concrete engineering framing

No structure notes have exceeded the 12-member overgrowth threshold. No obvious members are missing from any cluster.

**Title Quality** — All 26 titles are properly declarative, specific, and information-bearing. No generic patterns like "Notes on…" or "What is…?". Titles range from theoretical claims (intelligence scales through social organization) to specific findings (Bayesian reasoning requires estimating inputs).

**Inbox State** — The inbox directory is empty, indicating all captured material has been processed into sources or evergreen notes.

## Proposed Actions

1. **Monitor low-connectivity notes** — In the next reading pass, consider whether [[otp-is-designed-for-millions-of-lightweight-stateless-processes-llm-agent-systems-have-few-heavyweight-stateful-ones|OTP is designed for millions of lightweight stateless processes]] and [[reference-class-forecasting-outperforms-inside-view-estimation-for-project-timelines|Reference class forecasting outperforms inside-view estimation for project timelines]] need additional bridging links to the main argument clusters. They may be peripheral, or they may reveal a gap in the vault's current structure.

2. **Cross-structure linking** — The three structure notes are currently cited within their own clusters but do not link to each other. Consider whether cross-cluster connections would strengthen the network (e.g., institutional templates motivate behavioral steering, which operates through conversation mechanics).

3. **Continue reading in cluster order** — Future reading should maintain focus on the three structure clusters to test their coherence against new sources. Prioritize sources that might fill gaps in organizational science theory (the "Follow-Up" section in the agentic AI source lists Woolley et al., team size research, and hierarchy research as next steps).

## Reading Recommendations

**Gaps in Argument Structure:**

1. **Institutional enforcement mechanism** — The vault establishes that institutional templates (soft constraints, not hard rules) are necessary for AI alignment. But it does not explain *how* soft templates get enforced, or what happens when they fail. This gap appears in the "Open Questions" of multiple notes. Next sources should address organizational failure modes, cultural enforcement mechanisms, or concrete protocols that implement soft constraints.

2. **Organizational science transfer** — The vault identifies organizational science as an untapped design source but provides no concrete examples. Sources on collective intelligence (Woolley et al.), team composition, or network effects could fill this gap and provide engineering-actionable principles.

3. **Activation steering implementation** — The vault establishes that emotion vectors and the Interpersonal Circumplex could be used for behavioral steering, but does not detail how to build the three-stage pipeline (taxonomy → mapping → heuristics). Sources on representation engineering or concrete activation steering implementations would be valuable.

4. **Dyadic conversation protocol** — The vault establishes that text-native protocols are needed for LLM coordination but does not design one. Sources on conversational AI, protocol design, or asynchronous collaboration (Slack, email conventions) could inform a minimal working design.

## Comparison to Last Report

This is the first health report for the vault (recovered from corruption on 2026-04-06). No prior reports exist for comparison.

---

## Live Dashboards (Dataview)

### Evergreen notes with <2 inbound links (below median)
```dataview
table inbound-links, outbound-links
from "evergreen"
where (inbound-links) < 2 or (outbound-links) < 2
sort inbound-links asc
```

### Evergreen notes with <2 outbound links (low connectivity)
```dataview
table source, inbound-links, outbound-links
from "evergreen"
where outbound-links < 2
sort outbound-links asc
```

### Source notes and extraction health
```dataview
table source_type, evergreen-count
from "sources"
group by source_type
```

### Structure notes and membership
```dataview
table length(members) as member-count
from "structure"
```

### Recently created evergreen notes
```dataview
table created, source
from "evergreen"
sort created desc
limit 5
```

### Vault growth metrics
```dataview
table length(rows) as total
where type = "evergreen"
```
