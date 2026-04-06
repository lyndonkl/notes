---
type: evergreen
created: 2026-04-06
source: "Map-Territory Rationality"
tags: [planning, estimation, conjunction-fallacy, inside-view, forecasting]
aliases:
  - "Detail in a plan increases perceived accuracy but decreases actual accuracy"
---

# Detail in a plan increases perceived accuracy but decreases actual accuracy

Source: [[map-territory-rationality|Map-Territory Rationality]]

When you build a project plan, each added layer of detail feels like you're being more rigorous, more realistic, more professional. You break the problem into smaller tasks, attach timelines to each one, account for contingencies. The plan grows thicker, more specific, more concrete. And the more concrete it becomes, the more confident you feel—this is the plan that will work, because you've thought through all the pieces.

This feeling is a systematic trap. Each specific component you add to your forecast introduces its own uncertainty. You estimated three days for the database schema; you added two days for integration testing; you allocated one day for the design review. Each estimate individually might have a 50% chance of being right. But the probability that *all of them* are correct—that they'll all land within their predicted ranges—drops exponentially. This is the conjunction fallacy at work: the plan's granularity breeds confidence while its accuracy erodes.

Empirical research on project estimation confirms this dark pattern. Detailed, inside-view forecasts are consistently more optimistic than base-rate references—teams that built elaborately reasoned plans systematically underestimated timelines compared to teams that simply asked, "How long did similar projects take?" The specificity didn't increase accuracy; it increased the *appearance* of confidence, which made the inevitable disappointment worse when reality refused to match the detailed map.

The paradox resolves when you recognize that accuracy and confidence are not the same thing. Your detailed plan is more honest in some ways—it acknowledges that you've thought through the problem. But it has sacrificed accuracy on the altar of detail. Until you ground it in reference class data, you're mostly building an intricate false map.

## Links

- Confirms: [[the-inside-view-feels-more-credible-than-the-outside-view-because-it-contains-specific-details-not-because-it-is-more-reliable|The inside view feels more credible than the outside view because it contains specific details, not because it is more reliable]]
- Extends: [[reference-class-forecasting-outperforms-inside-view-estimation-for-project-timelines|Reference class forecasting outperforms inside-view estimation for project timelines]]
