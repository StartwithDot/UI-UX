# Sprint 5 Task List

Weeks 17 to 20. **C** Craft, **R** Research, **P** Product, **S** Systems, **F** Spine, **X** Injection.

---

## Week 17: Learn the domain and the density

**R17.1** Domain study. What underwriting actually is, what the 38 fields mean, and which six of them decide most cases. You cannot design this screen without knowing what a DSCR is.
→ `students/UX{n}/week17/R17-1-domain-study.md`

**R17.2** Interview or shadow one person who assesses risk for a living. Bank, insurance, lending, credit. If nobody is reachable, study three published underwriting guidelines and mark the confidence as low.
→ `R17-2-expert-study.md`

**C17.1** Information hierarchy for 38 fields plus 6 documents plus a bank analysis. What is on screen at rest, what is one interaction away, what is two. Justify the boundary.
→ `C17-1-hierarchy.md`

**C17.2** Density strategy. 38 fields scannable in 40 seconds. State your row height, your type size, your grouping logic, and the target size you are using given that AA asks for 24px minimum.
→ `C17-2-density-strategy.md`

**C17.3** The keyboard model. Every action, its key, the tab order, and the shortcut set. 45 applications a day means the mouse is a failure.
→ `C17-3-keyboard-model.md`

**S17.1** Which existing components survive at this density and which need a dense variant. Propose the variant properly, do not fork.
→ `S17-1-dense-variants.md`

**F17.1** Why session: designing for expertise. Why professional tools look wrong to novices and why simplifying them is usually a mistake.
→ `fundamentals/why-sessions/week17-expertise.md`

**F17.2** Teardown: a professional tool you do not use. Trading terminal, radiology viewer, airline crew scheduling.
→ `fundamentals/teardowns/17-professional-tool.md`

## Week 18: The AI surface

**C18.1** Score presentation. Your design, plus the two alternatives you rejected, plus why. One of the three alternatives must be "do not show the score at all".
→ `C18-1-score-presentation.md`

**C18.2** Confidence. Design it for a person who does not think in probability, and write down what your representation loses.
→ `C18-2-confidence.md`

**C18.3** The factors. Four contributing factors, presented without implying causation. Write the exact label text.
→ `C18-3-factors.md`

**C18.4** The wait. 2 to 8 seconds of model latency. What is on screen, what the underwriter can do meanwhile, and what happens at 8 seconds.
→ `C18-4-latency.md`

**C18.5** The anchoring problem. If the score is visible before the underwriter reads the file, it anchors them. State whether you sequence it, and what the sequencing costs in time per application.
→ `C18-5-anchoring.md`

**P18.1** Map your design against all 18 Microsoft Human AI guidelines. Every one: met, not met, or not applicable with a reason.
→ `P18-1-guidelines-audit.md`

**F18.1** Why session: human AI interaction, trust calibration, automation bias.
→ `fundamentals/why-sessions/week18-ai-trust.md`

**F18.2** Teardown: an AI feature in a product you use. What it claims, what it actually knows, and how it handles being wrong.
→ `fundamentals/teardowns/18-ai-feature.md`

## Week 19: When it breaks

**C19.1** Model unavailable. The underwriter has 45 applications and no score. Design it as a first class state, not an error.
→ `C19-1-model-unavailable.md`

**C19.2** Model wrong. Design the path where the underwriter disagrees: the override, the reason capture, and what the audit trail records.
→ `C19-2-override-flow.md`

**C19.3** Low confidence. Below your threshold, the score is close to useless. State the threshold, and what changes on screen below it.
→ `C19-3-low-confidence.md`

**C19.4** The applicant's reason. Write the actual decline sentence the applicant receives. It must be true, legally sufficient, and comprehensible to someone whose loan was just refused.
→ `C19-4-decline-explanation.md`

**C19.5** Feedback loop. The underwriter knows something the model does not. Design the path for that information to reach the model's owners.
→ `C19-5-feedback-loop.md`

**R19.1** Test with 5 participants, using an anchoring condition: some see the score first, some see it after forming a view. Report the difference in what they did, not what they said.
→ `R19-1-anchoring-test.md`

**F19.1** Why session: uncertainty, probability, and how people misread both.
→ `fundamentals/why-sessions/week19-uncertainty.md`

**F19.2** Teardown: a credit score product shown to consumers.
→ `fundamentals/teardowns/19-credit-score.md`

**F19.3** Whiteboard why. Draw the AI surface from memory and defend the score sequencing decision.

## Week 20: Finish and defend

**C20.1** Full console, high fidelity, keyboard complete, all states.
→ `C20-1-final-console.md`

**C20.2** Screen reader pass. Two colleagues at this company use one. Write out the announced text for the score, the confidence, the factors, and the override.
→ `C20-2-screen-reader-pass.md`

**C20.3** Gate, full, evidence on every line, at this density where target size is under pressure.
→ `C20-3-gate-result.md`

**P20.1** Decision record for the score presentation. The most consequential ADR of the program so far.
→ `fundamentals/adr/ADR-{n}-score-presentation.md`

**P20.2** The over trust measurement. How would you detect over trust in production, from behaviour, before the default rate tells you six months later.
→ `P20-2-overtrust-detection.md`

**S20.1** Dense variants contributed to the system with the constraint that justified them.
→ `../Design-Sprint-1/system/components/`

**S20.2** Handoff spec including the model contract: what the interface expects, what it does when it does not get it.
→ `S20-2-handoff-spec.md`

**F20.1** Explainer, Sprint 5.
→ `fundamentals/explainers/UX{n}-sprint5.md`

**X5.1** Post mortem on the injection.
→ `X5-1-postmortem.md`

**F20.2** Defense, six rounds. The adversarial round: "an underwriter approved a loan in 11 seconds because your interface showed a green score, and it defaulted. Explain your design to the audit committee."

---

## What fails review in this sprint

| Answer | Why it fails |
|---|---|
| The score shown as a verdict | You have built the over trust failure into the interface |
| "71 percent confidence" shown raw with no translation | Meaningless for a single case, and you have not thought about it |
| A factor labelled as a cause | Misrepresents what the model can support, and it is a regulatory problem |
| Model unavailable handled as an error toast | It is a normal condition at these latencies |
| A decline explanation citing the model | The applicant is entitled to a reason a person can act on |
| A wizard for 38 fields | 12 steps at 45 applications a day is 540 screen loads. You have designed for yourself. |
