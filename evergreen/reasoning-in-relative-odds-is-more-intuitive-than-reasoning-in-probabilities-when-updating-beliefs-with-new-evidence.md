---
type: evergreen
created: 2026-04-03
source: "A First Look at Bayes (Arbital)"
tags: [bayesian-reasoning, odds-ratio, cognitive-interface, calibration, mental-models]
aliases:
  - "Reasoning in relative odds is more intuitive than reasoning in probabilities when updating beliefs with new evidence"
---

# Reasoning in relative odds is more intuitive than reasoning in probabilities when updating beliefs with new evidence

Source: [[a-first-look-at-bayes|A First Look at Bayes]]

When you have estimated priors and encounter new evidence, thinking in relative odds — how much more likely is this under one hypothesis versus another — is cognitively easier than manipulating raw probabilities. Probabilities require you to track numbers between 0 and 1 and perform division to normalize. Relative odds let you simply multiply: prior odds times likelihood ratio gives you posterior odds directly.

This is not just a mathematical convenience. I learned Bayes' theorem in undergraduate studies but could never use it practically because thinking in probabilities felt unnatural for real-time reasoning. The shift to relative odds changes the cognitive interface without changing the underlying math — it makes the same theory usable inside your head rather than only on paper.

The practical value shows up in contexts like forecasting, where you start with a base rate (prior odds from historical data) and adjust as new information arrives. Relative odds give you a natural language for that adjustment: "this evidence makes one hypothesis three times more likely relative to the other" is easier to reason with than "this evidence changes the probability from 0.2 to 0.43."

## Links

- Extends: [[bayesian-reasoning-in-practice-requires-estimating-inputs-that-the-theory-assumes-are-given|Bayesian reasoning in practice requires estimating inputs that the theory assumes are given]]
- Context: [[the-strength-of-evidence-depends-on-how-unlikely-it-would-be-to-observe-that-evidence-if-the-claim-were-false|The strength of evidence depends on how unlikely it would be to observe that evidence if the claim were false]]
- Context: [[extraordinary-claims-require-extraordinary-evidence-because-extreme-prior-odds-demand-equally-extreme-likelihood-ratios|Extraordinary claims require extraordinary evidence because extreme prior odds demand equally extreme likelihood ratios]]
