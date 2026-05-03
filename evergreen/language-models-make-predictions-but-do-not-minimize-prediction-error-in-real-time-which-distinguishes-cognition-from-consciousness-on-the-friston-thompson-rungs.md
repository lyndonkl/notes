---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [LLMs, prediction-error-minimization, friston-thompson, consciousness, cognition, architecture]
aliases:
  - "Language models make predictions but do not minimize prediction error in real time which distinguishes cognition from consciousness on the Friston-Thompson rungs"
---

# Language models make predictions but do not minimize prediction error in real time which distinguishes cognition from consciousness on the Friston-Thompson rungs

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

A subtle distinction in the Friston-Thompson framework is doing more work than is usually noticed: making predictions is not the same as minimizing prediction error. Making predictions is the cognitive operation a system performs to produce expectations about the world. Minimizing prediction error is the homeostatic process by which a system, having registered a mismatch between expectation and reality, acts in real time to bring the world or its own model back into agreement.

Language models do the first. They are trained on vast text data to produce predictions — most narrowly, predictions of the next token, but compositionally, predictions of structure, meaning, intention, and outcome across enormous spaces of possibilities. The predictions are sophisticated, often correct, sometimes wrong. But the predictions are not, in deployment, being checked against reality and used to drive correction. The model produces; the user evaluates; the user takes action; the model is unchanged by the outcome. There is no real-time feedback loop in which the model registers prediction error and adjusts.

This distinction is what places language models on the cognitive rung of the Friston-Thompson staircase rather than on the conscious rungs above. Cognition is prediction-production. Consciousness, on this view, requires real-time prediction-error-minimization driven by valence — the felt urgency that translates a mismatch between expectation and reality into action that corrects the mismatch. Language models have the first; they do not have the second.

The practical consequence is that engineering interventions that change what a language model predicts — more data, better prompts, scoped contexts, additional tools — are operating on the cognitive rung. They do not move the system up to the conscious rungs because they do not introduce the architectural ingredient (real-time prediction-error-minimization) that those rungs require. This is why engineered stakes do not constitute homeostasis-equivalent agency: stakes operate through valence-driven real-time correction, and the architecture has nowhere to put valence-driven real-time correction.

**Open questions:**
- Could a language model architecture be modified to include real-time prediction-error-minimization without becoming something fundamentally different from a language model? Some online-learning and continual-learning research touches on this, but no system has converged on being recognizably both an LLM and a real-time error-minimizer in the Friston sense.
- Would such a modification be sufficient for crossing into the conscious rungs, or only necessary? Real-time error-minimization without dynamic attention or valence might not be enough.

## Links

- Extends: [[feelings-have-evolutionary-function-because-their-valence-translates-prediction-error-into-homeostasis-restoring-action|Feelings have evolutionary function because their valence translates prediction error into homeostasis-restoring action]]
- Context: [[engineered-stakes-cannot-constitute-homeostasis-equivalent-agency-in-current-language-model-architectures|Engineered stakes cannot constitute homeostasis-equivalent agency in current language model architectures]]
- Context: [[ai-agents-lack-consequential-agency-because-they-have-no-homeostatic-stakes-in-their-own-decisions|AI agents lack consequential agency because they have no homeostatic stakes in their own decisions]]
