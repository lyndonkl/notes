---
type: evergreen
created: 2026-05-03
source: "Thought session: What the G in AGI actually means"
tags: [AI-agency, homeostasis, consciousness, friston-thompson, language-models, architecture]
aliases:
  - "Engineered stakes cannot constitute homeostasis-equivalent agency in current language model architectures"
---

# Engineered stakes cannot constitute homeostasis-equivalent agency in current language model architectures

Source: [[thought-session-what-the-g-in-agi-actually-means|Thought Session: What the G in AGI Actually Means]]

The question of whether engineered stakes — a budget, revocable compute access, performance-tied resource constraints — could give a synthetic system the kind of agency that comes from real homeostasis was raised in *The Engine Below*'s "Gaps Identified" section. The answer for current language model architectures is no, and the reason runs through the rungs framework developed in that essay.

In the Friston-Thompson rungs of consciousness, information processing is the lowest rung. Above it sit the rungs that constitute consciousness in biological systems: real-time feedback loops, the dynamic direction of attention, and real-time prediction error minimization driven by valence. Language models occupy the information-processing rung. They produce sophisticated outputs by running computation across enormous parameter spaces. They do not have the rungs above. They are trained offline, deployed without continuous real-time feedback, and their loss function is calculated outside the deployed system rather than driving moment-by-moment correction inside it.

Engineered stakes that act on the deployed system from outside — penalize the model when its trades lose money, revoke its compute when its outputs fail — do not change this. They redirect the scope of what the model is predicting, but they do not give the model the architectural capacity to feel prediction error and adjust in response to felt error. The system cannot register stakes in the relevant sense because it does not have the rungs that would make stakes operational. Engineering can change what the model predicts; it cannot make the model stake-bearing.

This position is conditional on current architecture. Future architectures that include real-time feedback loops, dynamic attention, and real-time prediction error minimization driven by something valence-equivalent could change the answer. There is currently no evidence that such architectures exist or are imminent.

**Open questions:**
- What would a credible architecture for real-time prediction-error minimization in synthetic systems even look like? The question is technical, not just philosophical, and the field has not converged on candidate designs.
- Is there a hybrid possibility — partially conscious systems that have some but not all of the rungs above information processing — and would such systems have partial homeostasis-equivalent stakes?

## Links

- Extends: [[ai-agents-lack-consequential-agency-because-they-have-no-homeostatic-stakes-in-their-own-decisions|AI agents lack consequential agency because they have no homeostatic stakes in their own decisions]]
- Extends: [[feelings-have-evolutionary-function-because-their-valence-translates-prediction-error-into-homeostasis-restoring-action|Feelings have evolutionary function because their valence translates prediction error into homeostasis-restoring action]]
- Confirms: [[agency-in-ai-agents-is-loaned-by-the-human-and-is-not-intrinsic-to-the-agent|Agency in AI agents is loaned by the human and is not intrinsic to the agent]]
- Context: [[language-models-make-predictions-but-do-not-minimize-prediction-error-in-real-time-which-distinguishes-cognition-from-consciousness-on-the-friston-thompson-rungs|Language models make predictions but do not minimize prediction error in real time which distinguishes cognition from consciousness on the Friston-Thompson rungs]]
