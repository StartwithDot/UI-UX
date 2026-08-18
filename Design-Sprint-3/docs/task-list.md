# Sprint 3 Task List

Weeks 9 to 12. **C** Craft, **R** Research, **P** Product, **S** Systems, **F** Spine, **X** Injection.

---

## Week 9: Define the problem in numbers

**P9.1** Define activation. State the event, the time window, and the retention evidence that supports it as the right definition. Then state the definition you rejected and why.
→ `students/UX{n}/week9/P9-1-activation-definition.md`

**P9.2** Map the funnel from first visit to day 30, with the numbers from the brief at every step you can, and marked as unknown where you cannot.
→ `P9-2-funnel.md`

**P9.3** HEART framework applied. Fill all five rows, with goals, signals, and metrics. Any row you cannot fill honestly, say so rather than inventing a metric.
→ `P9-3-heart.md`

**P9.4** Competitive teardown of three products **and WhatsApp plus a paper diary**. The diary is the incumbent and it wins on three specific things. Name them.
→ `P9-4-competitive.md`

**R9.1** Interview two fleet owners and one driver. If you cannot reach real ones, state that and use the closest analogue, and mark the confidence accordingly.
→ `R9-1-interviews.md`

**S9.1** IA proposal. Every label justified. Every label you chose over a synonym, with the reason.
→ `S9-1-ia-proposal.md`

**F9.1** Why session: information architecture and navigation models.
→ `fundamentals/why-sessions/week09-ia.md`

**F9.2** Teardown: a bank's business banking dashboard.
→ `fundamentals/teardowns/09-business-banking.md`

## Week 10: Scope and structure

**P10.1** Shape the feature, in Shape Up terms. The appetite is six weeks with four engineers. Breadboard it, name the rabbit holes, name the no gos.
→ `P10-1-shaped-feature.md`

**P10.2** The cut list. What you are not building, and the reason each item is below the line. Ranked.
→ `P10-2-cut-list.md`

**P10.3** The driver problem. The buyer is not the data entry user. State your approach and what it costs. If your answer is an app install, defend it against a 40MB budget and prepaid data.
→ `P10-3-driver-strategy.md`

**S10.1** Tree test your IA with 8 participants. Report success rate, first click accuracy, and every label that failed.
→ `S10-1-tree-test.md`

**C10.1** The end to end flow, mid fidelity. Entry, empty state, first success, repeat use, failure, recovery. Six conditions, no gaps.
→ `C10-1-end-to-end-flow.md`

**C10.2** The empty state that is not empty. A new account has no trips, no drivers, and no data. Design what it shows and what it asks for first, given that Suresh will not enter 14 trucks.
→ `C10-2-empty-state.md`

**C10.3** Data density. One screen where the fleet owner sees 30 trucks at once. Table or cards, decided with a reason, at 390px and 1440px.
→ `C10-3-density.md`

**F10.1** Why session: data visualisation and dashboard design, Few and Tufte.
→ `fundamentals/why-sessions/week10-dataviz.md`

**F10.2** Teardown: an e-commerce seller dashboard.
→ `fundamentals/teardowns/10-seller-dashboard.md`

## Week 11: Prototype, test, and the ethics decision

**C11.1** Prototype with real logic in ProtoPie or Figma. Real conditional behaviour, not a click through. Must handle at least one failure path.
→ `C11-1-prototype.md`

**R11.1** Test with 5 participants. Task success, time on task, where they hesitated, and what they expected to happen that did not.
→ `R11-1-prototype-test.md`

**R11.2** The finding that broke your design. There will be one. If there is not, your tasks were too easy or you led them.
→ `R11-2-the-break.md`

**P11.1** Persuasion audit of your own design against the dark pattern catalogue. Every persuasive element: what it is, who benefits, and whether the user would agree with it if it were explained to them plainly.
→ `P11-1-persuasion-audit.md`

**P11.2 `[THE ETHICS DECISION]`** The client's request arrives Monday. Answer in writing: what it does to the number, what it costs the user, where it sits against the catalogue and the DPDP Act, your decision, and your alternative.
→ `P11-2-ethics-decision.md`

**C11.2** Fix what the test broke. Document what you changed and what you chose not to change, with reasons for both.
→ `C11-2-revisions.md`

**F11.1** Why session: persuasion, ethics, and the point at which influence becomes manipulation.
→ `fundamentals/why-sessions/week11-persuasion.md`

**F11.2** Teardown: a food delivery app's upsell and tipping flow.
→ `fundamentals/teardowns/11-food-delivery.md`

**F11.3** Whiteboard why. Your funnel, your activation definition, and your cut list, from memory.

## Week 12: Prove it and defend it

**C12.1** Final flow, high fidelity, both widths, on the cohort's system.
→ `C12-1-final-flow.md`

**C12.2** Full states, gate run, evidence on every line.
→ `C12-2-gate-result.md`

**P12.1** Instrumentation plan. Every event, its properties, and the question it answers. An event that answers no question gets deleted.
→ `P12-1-instrumentation.md`

**P12.2** Experiment design. Hypothesis, variants, primary metric, guardrails, minimum detectable effect, sample size, duration, and the result that would make you roll back.
→ `P12-2-experiment.md`

**P12.3** The business case, one page. What it costs to build, what it is expected to return, how confident you are, and what happens to the company's runway if you are wrong.
→ `P12-3-business-case.md`

**P12.4** What you would measure at month 3 to know whether the activation you designed was real or hollow.
→ `P12-4-hollow-activation-check.md`

**S12.1** Component contributions with the finding or constraint that justified each.
→ `../Design-Sprint-1/system/components/{component}.md`

**S12.2** Handoff spec for the highest risk screen, with the engineering questions pre answered.
→ `S12-2-handoff-spec.md`

**F12.1** Why session: metrics, experimentation, and how a number gets gamed.
→ `fundamentals/why-sessions/week12-metrics.md`

**F12.2** Explainer, Sprint 3.
→ `fundamentals/explainers/UX{n}-sprint3.md`

**X3.1** Post mortem on the injection.
→ `X3-1-postmortem.md`

**F12.3** Defense, six rounds. The adversarial round this sprint is run by someone playing the founder with 14 months of runway, and the question is why your design is worth six of the eighteen engineering weeks they have left.

---

## What fails review in this sprint

| Answer | Why it fails |
|---|---|
| "It improves the user experience" | Not a business outcome and not measurable |
| An activation definition with no retention evidence | A guess dressed as a metric |
| A design requiring more than the six week appetite, with no cut list | Not a product decision, a wish |
| A persuasion audit that finds nothing in your own design | Everyone's design has at least one persuasive element. Not finding it means not looking. |
| An ethics decision that refuses with no alternative | The client still has the problem. You have only removed yourself from it. |
| An experiment with no minimum detectable effect | You cannot know if the result means anything |
