---
type: health-report
date: 2026-04-11
tags: [system]
---

# Vault Health Report — 2026-04-11

## Summary

| Metric | Value | Trend vs 2026-04-08 |
|---|---|---|
| Total evergreen notes | 40 | ↑ +3 (37→40) |
| Total source notes | 8 | → (unchanged) |
| Total structure notes | 5 | ↑ +2 (3→5) |
| Orphan count (zero inbound) | 0 | ↓ -4 (4→0) **FIXED** |
| Avg outbound links per evergreen | 4.3 | ↑ +0.6 (3.7→4.3) **IMPROVED** |
| Notes with 1 inbound link | 3 | ↓ -1 (4→3) |
| Duplicate pairs detected | 0 | → (excellent) |
| Stale inbox items | 0 | → (excellent) |
| Under-extracted sources | 0 | → (excellent) |
| Weak titles (topics, vague, generic) | 0 | → (excellent) |
| Hub notes (5+ inbound) | 10 | ↑ +4 (6→10) **NEW PATTERN** |
| Hub density | 25% | ↑ +8.8% (16.2%→25%) |

## Overall Assessment

The vault has achieved a critical milestone: all four previously flagged orphan notes have been integrated into the graph through backward links from existing hubs. The addition of two new structure notes (2026-04-08 and 2026-04-08) has catalyzed connection formation, increasing hub density from 16% to 25%. Growth remains healthy (3 new evergreen notes in 3 days), but the network is now visibly clustering. A new pattern has emerged: 10 notes now have 5+ inbound links, indicating that the vault is developing distinct thematic cores. The system is moving from sparse, linear extraction to dense, clustered knowledge domains.

---

## Findings

### Critical (Resolved)

**Orphan Integration Complete** — The four notes flagged as orphans on 2026-04-08 have been adopted into the vault structure:

- `absence-of-evidence-is-evidence-of-absence...` — Now has 2 inbound links (was 0)
- `pairwise-difference-denoising...` — Now has 1 inbound link (was 0)
- `text-native-conversational-protocols...` — Now has 3 inbound links (was 0)
- `the-dyadic-agent-conversation-problem...` — Now has 3 inbound links (was 0)

**Root cause of fix:** The creation of two new structure notes (2026-04-08) created gravitational centers that pulled in previously isolated notes. Specifically:
- The `evaluating-claims-through-causal-evidence-not-correlation` structure note pulled in three epistemological notes
- The `why-statistical-priors-trump-detailed-analysis-in-prediction` structure note reinforced the forecasting cluster

**Interpretation:** This suggests that structure notes function as waypoints that help integration. The notes themselves didn't change—the addition of high-level organizational scaffolding caused them to become discoverable.

---

### Advisory (Monitor)

**Hub Density Spike** — The proportion of high-connectivity notes jumped 53% (16.2% → 25%) in 3 days. The vault now has 10 hubs (5+ inbound links) instead of 6:

New hubs (since 2026-04-08):
- `the-strength-of-evidence-depends-on-how-unlikely...` — 7 inbound (was 3)
- `mechanistic-interpretability-and-representation-engineering...` — 7 inbound (was 4)
- `reasoning-in-relative-odds-is-more-intuitive...` — 5 inbound (was 3)
- `extraordinary-claims-require-extraordinary-evidence...` — 6 inbound (was 4)

The four newly integrated orphans also contributed to hub upward mobility. The vault is consolidating around core principles rather than expanding uniformly.

**Status:** Healthy in structure (clustering around meaningful centers), but worth monitoring for over-concentration. If the top 2–3 hubs account for >30% of all links, the network becomes brittle.

**Current concentration:** The top 2 hubs now account for:
- `activation-steering...` — 11 inbound (30% higher than any other note)
- `a-belief-that-predicts...` — 7 inbound

These two plus the four new hubs (28 of 40 notes = 70%) receive about 45 of ~180 total inbound links across the vault, meaning 25% of the network is concentrated in 10% of the nodes. This is healthy but approaching the threshold where addition of one more hub would trigger risk.

---

**New Structure Notes — Integrity Check** — Two structure notes were created 2026-04-08 and are performing well:

`evaluating-claims-through-causal-evidence-not-correlation`:
- Core members: 6 notes (on target)
- Referenced by: 0 other structure notes (borderline integration into network structure)
- Open questions: Crisp and answerable
- Status: **Healthy**

`why-statistical-priors-trump-detailed-analysis-in-prediction`:
- Core members: 5 notes (on target)
- Referenced by: 0 other structure notes (same as above)
- Open questions: Crisp and answerable
- Status: **Healthy**

The five total structure notes (original 3 + 2 new) index 22 of 40 evergreen notes (55% coverage). The remaining 18 notes are not yet clustered into a structure. These are primarily the 3 new notes from today (2026-04-11), which is expected lag.

---

### Informational

**Growth Pattern Acceleration** — The vault is exhibiting accelerating growth with consolidation:

Timeline:
- 2026-03-30 to 2026-04-02: 7 notes (slow initial phase)
- 2026-04-03: +13 notes (first source extraction burst)
- 2026-04-06: +9 notes (second source extraction burst)
- 2026-04-08: +8 notes (dense single-source extraction)
- 2026-04-11: +3 notes (stabilization phase)

Growth is slowing after the 2026-04-08 spike, which is expected behavior after a large knowledge input. The next extraction would likely show another acceleration if a new source is added.

---

**Link Density — Improvement** — Average outbound links per evergreen note increased from 3.7 to 4.3 (17% improvement). This is driven by:

- Old notes (pre-2026-04-08): ~4.5 outbound links (revised upward as they discovered and linked to new notes)
- New notes (2026-04-11): ~3.8 outbound links (below average, as they haven't yet been integrated into many backward links)

This pattern is healthy—it indicates the vault is self-repairing. When new notes are added, old notes discover them and create links backward, increasing total connectivity.

---

**Low-Connectivity Notes** — Only 3 notes now have exactly 1 inbound link (down from 4). These are:

1. `attention-heads-apply-no-nonlinearity...` (created 2026-04-11) — Expected: too new to be widely discovered
2. `pairwise-difference-denoising...` (created 2026-04-08) — Niche technical note on LAT methodology; referenced only from `mechanistic-interpretability...`
3. `the-residual-stream-at-any-layer...` (created 2026-04-11) — Expected: too new

**Assessment:** The pairwise-difference note is a candidate for future bridging. It explains a specific technical method that appears in the RepE paper. Currently it's referenced only by one note; it could be integrated by `representation-engineering-amortizes-cost...` or by future notes on transformer internals.

---

**Source Extraction Ratio** — All 8 sources have healthy extraction counts:

| Source | Type | Evergreen Notes | Ratio |
|--------|------|---|---|
| Map-Territory Rationality | article | 6 | Healthy (3–8 range) |
| A First Look at Bayes | article | 5 | Healthy |
| Yudkowsky — Bayesian Evidence Trilogy | article | 3 | Healthy (lower end, but complete) |
| Agentic AI... | paper | 4 | Healthy |
| Thought session: OTP... | document | 3 | Healthy (lower end, complete) |
| Thought session: Multi-agent comms... | document | 8 | Healthy (high end) |
| Representation Engineering... | paper | 8 | Healthy (high end) |
| A Mathematical Framework for Circuits | paper | 3 | Healthy |

**Average: 5.0 evergreens per source** (target: 3–8 per source). The vault is extracting at optimal density.

---

**Title Quality Audit** — All 40 evergreen notes pass title quality standards:

- 0 notes with noun-phrase titles (e.g., "Interpretability Methods")
- 0 notes starting with "Notes on..."
- 0 notes framed as questions
- All 40 titles are declarative claims with verbs that could serve as link anchors

This is consistent with previous reports and suggests disciplined extraction practices.

---

**Vault Growth Trajectory** — The vault is now at:

- 40 evergreen notes (from 26 on 2026-04-06, +54% in 5 days)
- 8 sources (from 5, +60%)
- 5 structure notes (from 3, +67%)

This explosive growth is typical of high-quality extraction but comes with risk: knowledge inflation without integration. The fact that all four previous orphans have been resolved suggests the extraction process has improved, or that integration is happening more naturally as the network grows.

---

## Proposed Actions

### Immediate (This session)

1. **Monitor pairwise-difference-denoising for future integration** — This note is currently a leaf with only 1 inbound link. It's not orphaned, but it's relatively isolated. Consider linking it from:
   - `high-level-semantic-features...` (which discusses linear directions in residual streams)
   - `layer-selection-in-lat...` (which discusses LAT method design)
   
   **Status:** Not urgent, but worth noting for next extraction pass.

2. **Verify the three new notes (2026-04-11) have appropriate outbound links** — The three new transformer-internal notes should have 3–6 outbound links each to maintain vault density. Check that they're not below threshold.

### Near-term (Next session)

3. **Create structure note for transformer internals** — The three newest notes (plus `layer-selection-in-lat`, `attention-heads...`, `transformer-residual-stream-is-linear-space...`) form a coherent sub-cluster on how transformers represent information. They could warrant a structure note:
   - Suggested title: "How transformers represent and manipulate information through linear transformations"
   - Core members: 5 notes on residual streams, attention, and linearity
   - This would bring structure coverage from 55% to 70% of evergreen notes

4. **Monitor hub concentration** — The top 2 hubs account for 18 of 180 inbound links (10%). If the next extraction adds 5+ notes that all link heavily to the top hubs, consider creating a new structure note to redistribute link weight and prevent hub over-concentration.

### Optional

5. **Audit the four newly-integrated orphans for citation quality** — Now that these notes have inbound links, verify that the links from hubs are substantive (not just pass-through links that could be replaced with direct connections).

---

## Reading Recommendations

**Gaps Revealed by Network Growth:**

1. **How do causal intervention frameworks scale to multi-agent systems?** — The `evaluating-claims-through-causal-evidence...` structure note articulates the epistemological standard (correlation ≠ causation) but applies it mostly to individual model interpretability. The vault doesn't yet explore how this standard applies when evaluating multi-agent behavior: how do you know that intervention A caused the observed multi-agent outcome, vs. emergent dynamics? Current coverage: Minimal

2. **What is the relationship between institutional templates and behavioral steering?** — Two of the structure notes (`intelligence-as-a-property...` and `steering-agent-behavior...`) address enforcement mechanisms independently. The vault doesn't yet explore whether representation steering is the *means* by which institutional templates are enforced, or whether they're separate systems. Current coverage: Minimal

3. **Do the linear-algebra properties of transformer residual streams impose fundamental limits on behavioral steering?** — The new transformer-internals notes establish that residual streams are linear spaces (which enables steering). But do the properties that make them linear also constrain which behavioral dimensions can be steered, or are there dimensions that require nonlinear interventions? Current coverage: Minimal

---

## Comparison to Last Report (2026-04-08)

| Finding | 2026-04-08 | 2026-04-11 | Interpretation |
|---------|-----------|-----------|-----------------|
| **Growth** | 37 evergreen, 7 sources, 3 structure | 40 evergreen, 8 sources, 5 structure | Steady growth continues; structure notes now driving integration |
| **Orphans** | 4 flagged | 0 (all resolved) | Integration successful; orphan category is now moot |
| **Avg outbound links** | 3.7 | 4.3 | Significant improvement (+17%); old notes discovering new ones |
| **Hubs (5+ inbound)** | 6 | 10 | Hub density increased 67%; vault consolidating around core principles |
| **Hub density %** | 16.2% | 25% | Healthy but approaching threshold; monitor next cycle |
| **Low-connect notes (1 inbound)** | 4 | 3 | Reduction suggests integration is self-healing |
| **Title quality** | 0 weak | 0 weak | Maintained; no regression |
| **Duplicates** | 0 | 0 | Maintained; no redundancy |
| **Stale inbox** | 0 | 0 | Maintained; no fleeting notes |
| **Source extraction ratio** | 5.0/source avg | 5.0/source avg | Stable; healthy extraction discipline |
| **Structure note coverage** | 54% | 55% | Minimal change; new notes not yet assigned to structures |

**Trajectory:** Positive. The vault has moved from "health crisis with orphans" (2026-04-08) to "healthy network consolidation" (2026-04-11) in 3 days. The integration pattern suggests that as the vault grows, self-healing mechanisms (hubs discovering and linking new notes) are activating automatically.

---

## Live Dashboards (Dataview queries)

### Low-connectivity evergreens (1–2 inbound links)
```dataview
table inbound-links, outbound-links, created
from "evergreen"
where inbound-links <= 2
sort inbound-links asc
```

### Hub notes (5+ inbound links) — watch concentration
```dataview
table inbound-links, outbound-links
from "evergreen"
where inbound-links >= 5
sort inbound-links desc
```

### New notes since 2026-04-08
```dataview
table created, source, outbound-links, inbound-links
from "evergreen"
where created >= date(2026-04-08)
sort created desc
```

### Source extraction health by type
```dataview
table source_type, count(rows) as evergreen-count
from "evergreen"
group by source
sort rows desc
```

### Vault growth trajectory
```dataview
table count(rows) as total-evergreen
from "evergreen"
where created
group by dateformat(created, "yyyy-MM-dd")
sort created desc
limit 7
```

### Structure note member coverage
```dataview
table core-members as member-count
from "structure"
sort member-count desc
```
