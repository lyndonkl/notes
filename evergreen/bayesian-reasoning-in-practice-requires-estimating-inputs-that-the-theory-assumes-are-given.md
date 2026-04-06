---
type: evergreen
created: 2026-04-03
source: "A First Look at Bayes (Arbital)"
tags: [bayesian-reasoning, calibration, estimation, forecasting, cricket]
aliases:
  - "Bayesian reasoning in practice requires estimating inputs that the theory assumes are given"
---

# Bayesian reasoning in practice requires estimating inputs that the theory assumes are given

Source: [[a-first-look-at-bayes|A First Look at Bayes]]

Textbook presentations of Bayes' theorem hand you clean numbers: 20% base rate, 90% true positive rate, 30% false positive rate. You multiply and get an answer. But real-world reasoning almost never works this way. You have to estimate your own priors and likelihood ratios, and that estimation step is where most of the actual difficulty lives.

In cricket forecasting, this gap is concrete. I start with a base rate from head-to-head records, then try to update based on recent form. But converting "Team A scored 280 in their last 3 games while Team B scored 230" into a specific likelihood ratio requires judgment. I break game phases into bullish, bearish, and neutral scenarios based on player trends, then use heuristics to convert those into point adjustments. The framework is Bayesian in spirit — base rate plus updating evidence — but the conversion from qualitative assessment to quantitative ratio is where the art lives.

This is a genuine gap in the pedagogical literature on Bayes. The series I read teaches the mechanics of updating but not the skill of input estimation. Calibration training — learning to assign probabilities that match real-world frequencies — is a separate skill that Bayesian reasoning depends on but doesn't teach.

## Links

- Context: [[reasoning-in-relative-odds-is-more-intuitive-than-reasoning-in-probabilities-when-updating-beliefs-with-new-evidence|Reasoning in relative odds is more intuitive than reasoning in probabilities when updating beliefs with new evidence]]
- Context: [[the-strength-of-evidence-depends-on-how-unlikely-it-would-be-to-observe-that-evidence-if-the-claim-were-false|The strength of evidence depends on how unlikely it would be to observe that evidence if the claim were false]]
