---
type: health-report
date: 2026-04-24
tags: [system]
---

# Vault Health Report — 2026-04-24

## Summary

| Metric | Value | Trend (vs 2026-04-03) |
|---|---|---|
| Total evergreen notes | 57 | ↑ +42 |
| Total source notes | 10 | ↑ +7 |
| Total structure notes | 6 | ↑ +6 (was 0) |
| Orphan count | 0 | → unchanged |
| Avg outbound links per evergreen | 2.8 | ↓ from 3.8 (fresh extractions) |
| Duplicate pairs detected | 0 | → unchanged |
| Stale inbox items | 0 | → unchanged |
| Under-extracted sources | 0 | → unchanged |
| Notes with single outbound link | 1 | ↑ from 0 |
| Notes with 2 outbound links (borderline) | 17 | ↑ (mostly new Pollan extractions) |

## Overall Assessment

The vault is in **excellent health** with strong growth trajectory. Over 21 days since the last report, it has nearly quadrupled in size (15 → 57 evergreen notes), added 7 new sources spanning four new domains (mechanistic interpretability, Bayesian epistemology, LLM emotion research, and consciousness philosophy), and built out the structural infrastructure that the previous report flagged as the only gap (0 → 6 structure notes).

Zero structural decay across all seven diagnostics — no orphans, no duplicates, clean inbox, all sources properly extracted. The dip in average outbound link density (3.8 → 2.8) is entirely explained by today's batch of 12 fresh consciousness-cluster notes, which are still in the early-linking phase. Existing notes from prior sessions retain their density. This will self-correct as reading continues and cross-links accumulate.

The new consciousness cluster (12 notes from today's reading of Pollan's *A World Appears*) has integrated cleanly with the existing intelligence-as-collective and Bayesian-epistemology clusters, suggesting the vault is now in the synthesis phase rather than the foundation phase.

## Findings

### Critical (Act Now)
**None.** Zero orphans, zero duplicates, clean inbox, all sources well-extracted.

### Advisory (Act Soon)

**1. One note with only a single outbound link**
- *"Attention heads apply no nonlinearity to value vectors — softmax governs routing but content movement is a linear weighted sum"*
- Currently links only to the residual-stream note.
- Suggested additions: link to the representation-engineering note (the OV circuit's linearity is what makes RepE feasible) and to the mechanistic-interpretability vs. RepE note (linearity enables direct weight inspection).

**2. Today's 12 new consciousness notes are at the low end of link density**
- Average 2.8 outbound links each (target is 3–6). Two have 2 links, eight have 3, two have 4.
- Expected for fresh extractions. No action needed — links will accumulate naturally as reading continues.

**3. One structure note approaching the split threshold**
- *"Evaluating claims through causal evidence, not correlation"* has 11 members; the boundary advisory is 12.
- Not yet problematic. Worth monitoring at the next audit. If it grows past 12, the Emergence Agent should be asked to propose a split.

### Informational

**1. New cluster successfully integrated**
The 12 Pollan-derived notes form a recognizable consciousness-and-felt-experience cluster that cross-links to the existing rationality cluster (inside view, operational criteria), the intelligence-as-collective structure note, and the cellular function note. The convergence is genuine, not coincidental — the same epistemic pattern (phenomenology vs. structure) is being applied across both domains.

**2. Source distribution is now diverse**
10 sources spanning consciousness philosophy, epistemology, mechanistic interpretability, organizational science, and LLM emotion research. Average extraction ratio is 5.7 evergreens per source, well within the healthy 3–8 range. No source is under-extracted.

**3. Structure-note coverage has emerged organically**
The 6 structure notes now created cover the major thematic clusters: intelligence-as-social-property, multi-agent conversation problems, behavioral steering through representation, causal vs. correlational evidence, statistical priors over inside-view detail, and transformer representation through linear feature directions. The next likely structure-note candidate (per Emergence Agent's upcoming scan) is a phenomenology-isn't-structure cluster spanning rationality and consciousness work.

## Proposed Actions

1. **Add 1–2 outbound links from the attention-heads note.** Specifically: link to *"Representation engineering amortizes cost into one-time calibration..."* (the OV circuit's linearity is what makes RepE feasible) and to *"Mechanistic interpretability and representation engineering answer different questions..."* (linearity enables direct weight inspection).

2. **Monitor *"Evaluating claims through causal evidence, not correlation"* at the next audit.** If it reaches 12+ members, ask the Emergence Agent to propose a split (likely candidates: a core-causal-epistemology cluster and a mechanistic-intervention-instantiation cluster).

3. **No action required for the new Pollan notes' linking density.** Track in the next report — should self-correct to ≥3 outbound links per note as reading continues.

## Reading Recommendations

**For deepening the consciousness cluster:**
- Lisa Feldman Barrett's *How Emotions Are Made* — the constructed-emotion framework is a strong empirical anchor for the valence-as-engine claim.
- Karl Friston's primary FEP papers — currently you have Pollan's exposition, not Friston's own argumentation. The original papers would test whether Pollan's reading is faithful.
- Paul Bach-y-Rita and successors on sensory substitution — the empirical bedrock for the "different sensory configurations produce different kinds of consciousness" claim.

**For gap-filling:**
- The vault is strong on individual cognition and on social/collective coordination, but weak on **adaptation and learning** — how systems update their behaviors when their priors fail. Worth a reading session targeted at predictive-processing-style learning or Bayesian belief updating in agents.
- The vault has nothing yet on **the boundary problem in life/consciousness frameworks** — what makes something "one system" rather than two? Friston's Markov blanket formalism is the obvious next step here.

## Comparison to Last Report (2026-04-03)

**What improved:**
- Note count nearly quadrupled (15 → 57, +280% growth in 21 days).
- Source diversity tripled (3 → 10), adding mechanistic interpretability, Bayesian epistemology, LLM emotion research, and consciousness philosophy.
- Structure-note infrastructure built out from scratch (0 → 6) — directly addressing the only advisory issue from the previous report.
- Title quality flags from the previous report (institutional-templates and llm-agents-need-separate-modules) appear to have been retained as-is; user evidently judged the rewrites unnecessary, which is a defensible call.

**What needs monitoring:**
- Outbound link density for new notes (will track over the next 1–2 audits).
- Structure-note size ceiling (one note approaching 12-member threshold).

**What was lost:**
- Nothing.

---

## Live Dashboards (Dataview)

The following Dataview blocks update automatically when this report is viewed in Obsidian. They require the Dataview community plugin.

### Evergreen Notes Missing Outbound Links

```dataview
TABLE length(file.outlinks) AS "Outbound Links", created
FROM "evergreen"
WHERE type = "evergreen" AND length(file.outlinks) < 3
SORT length(file.outlinks) ASC
```

### Under-Extracted Sources (< 3 Evergreen Notes)

```dataview
TABLE length(file.inlinks) AS "Notes Linking Here", date_read
FROM "sources"
WHERE type = "source-note" AND length(file.inlinks) < 3
SORT length(file.inlinks) ASC
```

### Stale Inbox Items (> 7 Days Old)

```dataview
TABLE file.cday AS "Captured", (date(today) - file.cday).days AS "Age (days)"
FROM "inbox"
WHERE (date(today) - file.cday).days > 7
SORT file.cday ASC
```

### Recently Created Evergreen Notes

```dataview
TABLE created, source, length(file.outlinks) AS "Links"
FROM "evergreen"
WHERE type = "evergreen"
SORT created DESC
LIMIT 10
```

### Vault Growth Over Time

```dataview
TABLE length(rows) AS "Notes Created"
FROM "evergreen"
WHERE type = "evergreen"
GROUP BY created
SORT rows.created DESC
LIMIT 30
```

---

*Report generated by Health Agent — 2026-04-24*
*Previous report: 2026-04-03 (21 days elapsed)*
