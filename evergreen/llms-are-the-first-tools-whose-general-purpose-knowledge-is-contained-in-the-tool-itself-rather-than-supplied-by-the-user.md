---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [AGI, LLMs, tool-history, knowledge-representation, generality]
aliases:
  - "LLMs are the first tools whose general-purpose knowledge is contained in the tool itself rather than supplied by the user"
---

# LLMs are the first tools whose general-purpose knowledge is contained in the tool itself rather than supplied by the user

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

Every prior general-purpose tool — the computer, the spreadsheet, the printing press, the programming language — became useful across domains only when a human supplied the domain knowledge necessary to operate it. A spreadsheet does nothing for a financial analyst until the analyst encodes their financial model into it. A programming language does nothing for an ML engineer until the engineer encodes their training procedure. The tool was a substrate; the user supplied the content.

The LLM inverts this. Broad domain knowledge across financial analysis, biology, sports forecasting, software engineering, nutrition, and dozens of other fields is already present in the model's weights before any user shows up. The user no longer supplies domain knowledge to the tool — the user supplies context that selects, scopes, and shapes the knowledge the tool already has.

This is what makes Sutskever's offhand remark — that we have "in some ways surpassed AGI" — defensible rather than hyperbolic. The "general" in AGI was always ambiguous: does it mean "as capable as a human across all domains" or "applicable across all domains"? The first reading sets a bar we have not cleared. The second reading sets a bar that no tool in human history had cleared, but that a present-day language model now does.

**Open questions:**
- "Knowledge contained in the model" smuggles a strong claim. What the model actually has is patterns over text large enough to simulate domain knowledge. Whether the distinction matters depends on whether the historical-uniqueness argument needs the strong reading or survives the weaker one.
- This claim conflates breadth of knowledge present with reliability of access. The model's knowledge is broad but its reliability per query is uneven, which is the entry point for the exploration/exploitation bound.

## Links

- Confirms: [[intelligence-scales-through-social-organization-not-individual-cognitive-upgrades|Intelligence scales through social organization not individual cognitive upgrades]]
- Context: [[scalable-ai-alignment-requires-institutional-templates-not-individual-virtue|Scalable AI alignment requires institutional templates not individual virtue]]
