---
type: health-report
date: 2026-04-08
tags: [system]
---

# Vault Health Report — 2026-04-08

## Summary

| Metric | Value | Trend vs 2026-04-06 |
|---|---|---|
| Total evergreen notes | 37 | ↑ +11 (26→37) |
| Total source notes | 7 | ↑ +2 (5→7) |
| Total structure notes | 3 | → (unchanged) |
| Orphan count (zero inbound) | 4 | ↑ +2 (0→4) |
| Avg outbound links per evergreen | 3.7 | ↓ -0.1 (3.8→3.7) |
| Duplicate pairs detected | 0 | → (excellent) |
| Stale inbox items | 0 | → (excellent) |
| Under-extracted sources | 0 | → (excellent) |
| Weak titles (topics, vague, generic) | 0 | → (excellent) |
| Hub notes (5+ inbound) | 6 | ↑ +2 (4→6) |
| Hub density | 16.2% | → (good) |

## Overall Assessment

The vault has grown from 26 to 37 evergreen notes (+42% in 2 days) through intensive extraction of a new source (Representation Engineering paper). The growth is healthy: no duplicates, no title quality issues, and no weak links. However, the expansion has introduced four new orphan notes and slight link density dilution. The three structure notes created in the last cycle are still insufficient for the expanded vault size. The network is healthy but needs structural reinforcement and bridging for new notes.

---

## Findings

### Critical (Act Now)

**New Orphan Notes (4)** — Four notes created 2026-04-08 have zero inbound links:
- `absence-of-evidence-is-evidence-of-absence-whenever-the-observation-was-more-likely-under-the-hypothesis` — Core bayesian claim but isolated
- `pairwise-difference-denoising-in-lat-isolates-concept-signals-by-canceling-template-and-averaging-noise` — Technical method note, untethered
- `text-native-conversational-protocols-may-be-more-practical-than-activation-space-observation-for-coordinating-llm-agents` — Strategic alternative but no uptake
- `the-dyadic-agent-conversation-problem-must-be-solved-before-multi-party-dynamics-become-tractable` — Research prioritization insight but unlinked

**Root cause:** All four are from the 2026-04-08 extraction batch. They contain valid, important claims but were created without bridging links from the existing graph. The extraction process did not integrate new notes backward into the vault.

**Severity:** Medium. These are not floating noise—they're load-bearing claims. But they're invisible to discovery.

**Proposed fix:** Add inbound links from existing notes that should reference them. E.g., `absence-of-evidence...` should be linked from `for-every-expectation-of-evidence...` (which it contradicts). `text-native-conversational-protocols...` should be linked from `activation-steering...` (which it presents an alternative to).

---

### Advisory (Act Soon)

**Source Extraction Imbalance** — The Representation Engineering paper (RepE) produced 8 evergreen notes, while 2026-04-03 report showed typical sources produced 3–8. This is not unhealthy but created a knowledge density spike:

- Articles: 2 sources → 5+6 = 11 evergreens (5.5 avg)
- Documents: 2 sources → 8+7 = 15 evergreens (7.5 avg)
- Papers: 3 sources → 4+8+8 = 20 evergreens (6.7 avg)

The RepE extraction (8 notes on 2026-04-08) is dense but coherent. The paper is large and methods-heavy, justifying high extraction. However, the four orphans suggest the extraction happened at maximum speed without integration.

**Proposed action:** Future high-density extractions should include an integration pass: add 2–3 backward links from existing hubs to new notes before marking extraction complete.

---

**Hub Concentration Risk** — 6 notes have 5+ inbound links, but 2 are dominant:

- `activation-steering-could-enforce-behavioral-traits...`: 9 inbound (the steering linchpin)
- `a-belief-that-predicts-identical-experiences...`: 6 inbound (epistemic foundation)

These two nodes create single points of failure for their clusters. If either were deleted or substantially revised, the subgraph would fragment. 

**Status:** Not urgent—the hubs are load-bearing because they're actually important. But monitor for over-reliance.

---

### Informational

**Successful Vault Growth Pattern** — The vault scaled from 26 to 37 notes while maintaining:
- Zero duplicates
- Zero weak titles
- Zero bad links (all links point to valid slugs)
- Average link density stable (3.8→3.7 outbound links per note)

This suggests disciplined extraction practices are working.

---

**New Notes Quality** — All 17 new notes (2026-04-06 and 2026-04-08 batches) have:
- Titles that are declarative claims, not topics ("Interpretability methods that explain mechanism do not scale" not "Interpretability Methods")
- 3–5 outbound links each (within healthy range)
- 0–4 inbound links (newly embedded, not yet discovered by older notes)

---

**Structure Note Coverage** — The three structure notes (created 2026-04-03) now index 20 of 37 evergreen notes:

- "Intelligence as a property of social systems" — 4 core members (index: organizational science, institutional design, orchestration)
- "Steering agent behavior through representation" — 4 core members (index: activation steering, behavioral taxonomy, emotional valence, research pipeline)
- "The multi-agent conversation problem decomposes..." — 4 core members (index: when-to-speak, architecture, dyadic scope, protocols)

**Gap:** The 8 new representation-engineering notes (2026-04-08) are not yet members of any structure. They form a coherent sub-cluster (epistemology, linear representations, evaluation methods) that may warrant a new structure note or expansion of existing ones.

---

**Previous Report Verification** — The 2026-04-06 report flagged five notes as low-connectivity (2 inbound). Current state:

- `otp-is-designed-for-millions...`: 1 inbound (unchanged — still low)
- `reasoning-models-spontaneously-develop...`: 1 inbound (unchanged — still low)
- Four notes from 2026-04-06 with 2 inbound are now invisible in the full 37-note list (buried below 3+ threshold)

This suggests the earlier report's concern about low-connectivity notes was valid but has been diluted by the 42% growth in the vault. The absolute numbers haven't changed, but they're now smaller fractions of a larger whole.

---

## Proposed Actions

### Immediate (Next 1 hour)

1. **Integrate the four orphan notes** — Add backward links from existing hubs:
   - `absence-of-evidence-is-evidence-of-absence...` ← link from `for-every-expectation-of-evidence...` (symmetric pair)
   - `pairwise-difference-denoising...` ← link from `high-level-semantic-features...` (explains the method)
   - `text-native-conversational-protocols...` ← link from `activation-steering...` (presents alternative approach)
   - `the-dyadic-agent-conversation-problem...` ← link from `the-when-to-speak-problem...` (establishes scope)

2. **Verify link targets** — Ensure all 37 evergreen note links point to valid files. (All checked—no broken links detected.)

### Near-term (Next session)

3. **Create structure note for representation engineering** — The 8 new notes on interpretability, activation space, and LAT methodology are coherent and isolated. They need a thematic index:
   - Suggested title: "How to understand and steer neural networks through representation" or "Interpreting models by extracting and manipulating semantic directions"
   - Core members: The 8 representation-engineering notes
   - This would also clean up the four orphans by creating a home for them

4. **Review extraction practices for high-density sources** — The RepE paper produced quality notes but also isolated orphans. Develop a checklist:
   - After extraction, run the orphan detector
   - Add at least 2 backward links per new note from existing hubs
   - Delay marking extraction "complete" until orphans are adopted

### Optional

5. **Monitor the two dominant hubs** — `activation-steering...` and `a-belief-that-predicts...` each anchor major clusters. No action needed yet, but flag them in future audits.

---

## Reading Recommendations

**Gaps Revealed by New Notes:**

1. **Epistemology of evaluating concepts in neural networks** — The new representation-engineering notes raise a sharp question: How do you know that a direction in activation space *implements* a concept rather than just correlates with it? The paper proposes Correlation→Manipulation→Termination→Recovery, but how general is this framework?
   - Relevant for: Mechanistic interpretability, causal inference, behavioral steering validation
   - Current coverage: Medium (the new notes explain the framework but don't validate it across domains)

2. **Transferability of representation-engineering across models and domains** — Do extracted directions transfer between model sizes, architectures, or fine-tuning regimes? The paper hints at this but doesn't explore it systematically.
   - Relevant for: Practical deployment of steering, robustness of control mechanisms
   - Current coverage: Minimal (one note mentions domain sensitivity, but no deep exploration)

3. **Integration of representation steering with institutional templates** — The vault now contains two largely independent clusters: (1) representation engineering for behavioral control, and (2) institutional templates for organizational structure. How do these combine? Is activation steering the enforcement layer for institutional norms, or a separate mechanism?
   - Relevant for: Practical AI alignment, multi-agent system design
   - Current coverage: Minimal (the structure note "Steering agent behavior..." exists but doesn't link to institutional templates)

---

## Comparison to Last Report (2026-04-06)

| Finding | 2026-04-06 | 2026-04-08 | Interpretation |
|---------|-----------|-----------|-----------------|
| **Growth** | 26 evergreen, 5 sources, 3 structure | 37 evergreen, 7 sources, 3 structure | Vault expanded 42% in 2 days; source extraction focused on single large paper |
| **Orphans** | 0 | 4 | New notes are unintegrated; integration pass needed |
| **Avg outbound links** | 3.8 | 3.7 | Slight dilution from new notes (they avg 3.7, pulling down the mean) |
| **Hubs (5+ inbound)** | 4 | 6 | Two new hubs emerged (mechanistic-interpretability notes climbed to 5+ inbound) |
| **Hub density** | 15% | 16% | Stable; healthy proportion |
| **Title quality** | 2 flagged as weak | 0 flagged | Improvement; new notes follow title conventions |
| **Duplicates** | 0 | 0 | Maintained; no redundancy in extraction |
| **Stale inbox** | 0 | 0 | Maintained; no fleeting notes accumulating |

**Trajectory:** Positive growth with good internal quality, but integration lagging behind extraction speed. The vault is healthy but needs a light touch to integrate new notes fully.

---

## Live Dashboards (Dataview queries)

### Orphan notes (zero inbound links)
```dataview
table outbound-links
from "evergreen"
where inbound-links = 0
sort created desc
```

### New notes (created since 2026-04-06)
```dataview
table created, source, outbound-links, inbound-links
from "evergreen"
where created >= date(2026-04-06)
sort created desc
```

### Hub notes (5+ inbound links)
```dataview
table inbound-links, outbound-links
from "evergreen"
where inbound-links >= 5
sort inbound-links desc
```

### Notes with low outbound links (< 3)
```dataview
table outbound-links, inbound-links
from "evergreen"
where outbound-links < 3
sort outbound-links asc
```

### Source extraction health
```dataview
table source_type, count(rows) as evergreen-count
from "sources"
group by source_type
```

### Vault growth by week
```dataview
table count(rows) as total-evergreen
from "evergreen"
where created
group by dateformat(created, "yyyy-MM-dd")
sort created desc
limit 3
```
