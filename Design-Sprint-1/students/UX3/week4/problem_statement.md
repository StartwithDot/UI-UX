# Sprint 1, Week 4: Ship and defend

**UX3 | Position this week: builder | Theme: it is not done until someone else can build it**

High fidelity, gate passed, handoff written, defense survived. The defense is Saturday and it is not a presentation.

---

## Craft and Interface

**C6.1** Full flow at high fidelity, 390px and 1440px. The desktop version is not the mobile version stretched. State one layout decision that differs between the two and why.
→ `C6-1-final-flow.md` plus Figma link

**C6.2** Dark mode for three screens using your semantic tokens. If the tokens do not support it, that is a system finding, so log it.
→ `C6-2-dark-mode.md`

**C6.3** One motion specification: what animates, duration, easing, what it explains to the user, and the reduced motion alternative.
→ `C6-3-motion-spec.md`

**C6.4** Language expansion. Your three densest screens with Hindi text 30 percent longer than English. What breaks and how you fixed it.
→ `C6-4-language-expansion.md`

## Systems and Technical `[MILESTONE]`

**S4.1** Full accessibility gate on your primary flow. Every line answered with evidence, not a tick. Include the screen reader pass with the announced text written out.
→ `S4-1-gate-result.md`

**S4.2** Handoff spec for the upload screen: component references, spacing values, states, validation rules, error copy, focus order, and what the engineer needs from the backend.
→ `S4-2-handoff-spec.md`

**S4.3** Read one peer's handoff spec as the engineer. Write the three questions you would have to ask before you could build it. Those three questions are the gaps.
→ `S4-3-handoff-review.md`

**S4.4** Cohort session. Does the system documentation match what is actually in it. Fix the drift, write the changelog.
→ `system/docs/CHANGELOG.md`

## Product and Business

**P3.1** Decision record for the choice a department official would most likely question. Context, two options considered, decision, consequences including the bad ones, and what would make you revisit it.
→ `fundamentals/adr/ADR-{n}-{title}.md`

**P3.2** Two minute version of your work. Problem, what you changed, what evidence you have. No screens until the problem is stated.
→ `P3-2-two-minute-script.md`

**P3.3** Cohort session. One shared presentation to the department. Five designers, one narrative, not five portfolios.
→ `delivery/presentation/sprint1-deck.md`

**P3.4** What you would do with four more weeks, in priority order, with the reason each item is above the next.
→ `P3-4-next-four-weeks.md`

## Spine

**F4.1** Why session, Saturday. This week's presenter: **UX4**. Affordances, signifiers, mental models from Norman chapters 1 to 4, applied to your own upload component.
→ `fundamentals/why-sessions/week04-affordances.md`

**F4.2** Teardown: a subscription cancellation flow of your choice. Name every dark pattern and the regulation it may run into.
→ `fundamentals/teardowns/04-cancellation.md`

**F4.3** Explainer. One concept from this sprint you can now explain properly: plain definition, the problem it solves, an example from this project, what breaks if you get it wrong, and one thing still unclear to you.
→ `fundamentals/explainers/UX3-sprint1.md`

## The defense, Saturday, 55 minutes

Six parts. Structure in `../../../../Program Structure.md` section 7.

| Part | Time | What is actually being checked |
|---|---|---|
| Numbers | 8 min | Contrast ratios, target sizes, type sizes, WCAG criterion numbers, from memory. This part is either right or it is not. |
| Reasoning | 12 min | Why this and not the alternative. "It looked better" fails. |
| Critique | 10 min | Critique a surface you have not seen, live. Three flaws with principle and user cost. |
| Adversarial | 10 min | Your weakest decision is attacked. Defending a bad decision scores worse than conceding it and stating the fix. |
| Handoff | 8 min | Explain your upload spec to someone playing the engineer. They will find the gap. |
| Reflection | 7 min | What you got wrong this sprint. A designer with nothing to name here has not looked. |

**How to prepare.** Numbers cannot be crammed, so check your own values against the tokens today. Reasoning cannot be scripted, so re-read your ADR and your wont-fix. Critique cannot be prepared at all, which is why the teardown drill exists. The reflection is the part people underprepare and it is the part that most predicts whether someone will be good in a year.

## Done when

- High fidelity flow at both widths, committed with the Figma link
- Accessibility gate filled with evidence on every line
- Handoff spec written and reviewed by a peer
- ADR committed
- Explainer committed
- Defense attempted

## Watch for

**The gate is not a formality.** A flow that fails the gate in week 4 does not ship, and the sprint result records it. Run the gate on Tuesday, not Friday night, because the fixes take longer than the check.

**The handoff review is the honest signal.** If your peer needs to ask you three basic questions to build your screen, the spec is incomplete regardless of how the screens look. Every question they had is something a real engineer would have interrupted you for.

## Reading this week

- WCAG 2.2 quick reference, one more full pass before the gate
- Articulating Design Decisions, the chapters on responding to feedback and stakeholder questions
- Your own week 1 heuristic audit. Read it against your final flow and count how many of your own findings you reproduced.
