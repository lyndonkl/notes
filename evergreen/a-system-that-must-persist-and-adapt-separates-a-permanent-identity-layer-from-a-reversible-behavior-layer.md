---
type: evergreen
created: 2026-06-22
source: "MIT 7.016 Introductory Biology — Reading Thread (Video 2: Chemical Bonding; Lipids and Membranes)"
tags: [systems-thinking, architecture, identity, dynamics, biology, multi-agent-systems, mit-7016]
aliases:
  - "A system that must both persist and adapt separates a strong, permanent layer that holds identity and information from a weak, reversible layer that enacts behavior"
---

# A system that must both persist and adapt separates a strong, permanent layer that holds identity and information from a weak, reversible layer that enacts behavior

Source: [[mit-7016-introductory-biology-thread|MIT 7.016 Introductory Biology (lecture series)]]

Living matter is held together by two kinds of bonds with sharply different strengths, and the difference is the point. Strong covalent bonds (on the order of 90–100 kcal/mol) form the permanent backbone — the fixed sequence of a DNA strand, the amino-acid order of a protein. That backbone is where identity and information live: it is the thing that must be preserved and copied faithfully. Weak non-covalent bonds (roughly 1–10 kcal/mol) are reversible; they break and re-form continuously, and they are where behavior happens — folding, binding, catalysis, the shape changes that do the actual work. One layer is for being; the other is for doing.

The general claim is that any system that must both persist and adapt needs this division of labor. A purely rigid system can store information but cannot act on it. A purely fluid system can change endlessly but has no stable identity for the changes to refer to. The dynamic layer depends on the permanent layer as a reference frame: variability with nothing fixed underneath is not flexibility, it is noise. The strength asymmetry — strong-and-permanent for structure, weak-and-reversible for behavior — is a design feature, not an accident.

(My framing, not the lecture's.) In engineered systems this is the split between a stable schema, contract, or identity and a fluid runtime that reconfigures on top of it. For multi-agent systems it suggests a concrete prescription: agents need fixed identities and protocols that must *not* drift, paired with loose, reconfigurable coordination that *should*. Collapsing the two — making everything rigid, or everything fluid — costs you either the adaptability or the continuity.

## Links

- Context: [[self-organization-is-relocated-design-into-local-rules-and-an-environment-that-makes-the-target-structure-stable|Self-organization is not the absence of design but its relocation into local rules and an environment that makes the target structure the stable configuration]]
- Context: [[institutional-templates-for-ai-agents-should-constrain-response-space-not-prescribe-responses|Institutional templates for AI agents should constrain response space not prescribe responses]]
