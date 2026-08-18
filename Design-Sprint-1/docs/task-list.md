# Sprint 1 Task List

Every task in Sprint 1, station by station. Task IDs carry the track letter: **C** Craft, **R** Research and Evidence, **P** Product and Business, **S** Systems and Technical.

Each task states the deliverable and the commit path. `UX{n}` is your own code. Milestone stations are marked `[MILESTONE]` and the whole cohort clears them together.

Weekly extracts of this file live in `students/UX{n}/week{n}/problem_statement.md`.

---

## Week 1: Frame

### P1. Reframe the brief `[MILESTONE]`

**P1.1** The department's brief is "make it so people stop coming to the counter". Write the three questions that brief does not answer. For each, state who could answer it and how long that would take.
Commit: `students/UX{n}/week1/P1-1-brief-questions.md`

**P1.2** Rewrite the brief as a problem statement in this shape: [user] cannot [job] because [obstacle], which costs [cost to user] and [cost to department]. One paragraph maximum. No solution words in it.
Commit: `students/UX{n}/week1/P1-2-problem-statement.md`

**P1.3** List every constraint from the brief plus three you found by using the live service. Mark each as fixed policy, technical, or assumed. The assumed ones are the ones worth attacking later.
Commit: `students/UX{n}/week1/P1-3-constraints.md`

**P1.4** Name the primary metric, two input metrics, and one guardrail metric. For the guardrail, write one sentence on what bad design would look like if only the primary metric mattered.
Commit: `students/UX{n}/week1/P1-4-metrics.md`

### R1. Audit what exists

**R1.1** Walk the live flow at `myaadhaar.uidai.gov.in` on a phone. Screenshot every screen including every error you can trigger. Do not use anyone else's Aadhaar number.
Commit: `students/UX{n}/week1/R1-1-current-flow-screens/` plus a `README.md` listing each screen in order

**R1.2** Heuristic evaluation of the live flow against Nielsen's 10 heuristics. Table format: screen, heuristic violated, what the user experiences, severity 1 to 4. Minimum 12 findings. "Looks outdated" is not a finding.
Commit: `students/UX{n}/week1/R1-2-heuristic-audit.md`

**R1.3** Accessibility audit of the live flow. Keyboard only pass, contrast check on 5 elements, focus visibility, form label check. State the WCAG 2.2 criterion for each failure.
Commit: `students/UX{n}/week1/R1-3-accessibility-audit.md`

**R1.4** Pick the three worst findings from R1.2 and R1.3. For each, write the user cost in one sentence a department official would understand. No design jargon.
Commit: `students/UX{n}/week1/R1-4-worst-three.md`

**R1.5** Watch one real person attempt the live flow. Anyone, a family member is fine. Do not help them. Note where they hesitate, what they say out loud, where they stop. Twenty minutes maximum.
Commit: `students/UX{n}/week1/R1-5-observation.md`

### C1. Type and spacing

**C1.1** Build a type scale. State the base size, the ratio, and every step with its intended use. Test it with Devanagari text at every step and note where it breaks.
Commit: `students/UX{n}/week1/C1-1-type-scale.md` plus a Figma link

**C1.2** Build a spacing scale. State the base unit and every step. For three steps, name a specific place in this flow where that step is the right one.
Commit: `students/UX{n}/week1/C1-2-spacing-scale.md`

**C1.3** Set one long paragraph of body text at three different measures. Screenshot all three, state which is right and why, in terms of line length and reading, not preference.
Commit: `students/UX{n}/week1/C1-3-measure-test.md`

**C1.4** Take one screen from the live flow. Rebuild it with no colour, only type, weight, and spacing. Hierarchy must be readable in greyscale.
Commit: `students/UX{n}/week1/C1-4-greyscale-hierarchy.md` plus a Figma link

### C2. Colour

**C2.1** Build a colour system: one neutral ramp of 10 steps, one primary ramp, and semantic colours for success, warning, error, and information. Use Leonardo or an equivalent so the ramps stay perceptually even. Every step must state its contrast ratio against white and against your darkest neutral.
Commit: `students/UX{n}/week1/C2-1-colour-system.md`

**C2.2** Map colours to semantic roles: page background, surface, border, text primary, text secondary, text disabled, interactive default, interactive hover, interactive pressed, focus ring, error text, error surface. This is the mapping that becomes tokens.
Commit: `students/UX{n}/week1/C2-2-semantic-roles.md`

**C2.3** Take your error state colour and prove it works for a user with deuteranopia and for a user in bright sunlight at low screen brightness. Show what carries the meaning when colour does not.
Commit: `students/UX{n}/week1/C2-3-colour-independence.md`

### S1. System foundation `[MILESTONE]`

**S1.1** Cohort session, not individual. Agree one token naming convention for the shared system. Write the convention with three examples of a correct name and three of an incorrect name with the reason.
Commit: `system/docs/token-naming.md` by the week 1 system owner, referenced by everyone

**S1.2** The five type scales, five spacing scales, and five colour systems from C1 and C2 are now five different answers. Cohort session: pick one of each, or synthesise. Record what was rejected and why. This decision cannot be reopened after week 2 without a decision record.
Commit: `system/docs/foundations-decision.md`

**S1.3** Write the agreed foundations as token JSON. Three layers: primitive, semantic, component. Only the layers you actually need.
Commit: `system/tokens/primitive.json`, `system/tokens/semantic.json`

**S1.4** Set up the shared Figma library with the agreed variables and modes. Light mode only this week. Post the link in `system/docs/README.md`.
Commit: `system/docs/README.md`

### Spine, week 1

**F1.1** Why session. One designer presents Gestalt principles using screens from the live Aadhaar flow as the examples. Every principle needs an example from the real service, not a textbook diagram.
Commit: `fundamentals/why-sessions/week01-gestalt.md`

**F1.2** Teardown. Assigned subject: the IRCTC ticket booking flow. Format: the flaw, the principle it violates, the user cost, the fix, and what the fix costs to build.
Commit: `fundamentals/teardowns/01-irctc.md`

**F1.3** Drill, daily. Rebuild one component from any real Indian product, from memory, then compare. Ten minutes. One line log per day.
Commit: `fundamentals/drills/UX{n}-log.md`

---

## Week 2: Build

### P2. Flow and structure

**P2.1** Draw the full flow as a Mermaid diagram: every screen, every decision point, every exit. Include the three failure paths from the brief's user section.
Commit: `students/UX{n}/week2/P2-1-flow.md`

**P2.2** Lakshmi cannot receive the OTP because the registered mobile is not hers. Design the path. It cannot end in "visit a centre" without first exhausting what the interface can do.
Commit: `students/UX{n}/week2/P2-2-no-otp-path.md`

**P2.3** Decide whether address entry is one page or multiple steps. Write both options, the tradeoff, and your decision with the reason. Cite something: a documented convention, a heuristic, or your R1.5 observation.
Commit: `students/UX{n}/week2/P2-3-form-structure-decision.md`

### C3. Mid fidelity screens

**C3.1** Build the happy path at mid fidelity, 390px. Grey boxes are not mid fidelity. Real content, real labels, real button text, no lorem ipsum, no placeholder names.
Commit: `students/UX{n}/week2/C3-1-happy-path-mobile.md` plus a Figma link

**C3.2** Document guidance screen. Ramesh does not know that the document must be in his name. Design the moment where he learns that, before he uploads. State how you decided where that moment goes.
Commit: `students/UX{n}/week2/C3-2-document-guidance.md`

**C3.3** Address entry screen. Every field needs a label, an example or hint where the format is not obvious, and a validation rule you can state. List the fields with their rules before you design the screen.
Commit: `students/UX{n}/week2/C3-3-address-entry.md`

**C3.4** Upload screen. Design for: file too large, wrong format, unreadable photo, upload interrupted at 60 percent on a bad connection, and success. Five states, not one screen with an error variant.
Commit: `students/UX{n}/week2/C3-4-upload-states.md`

### C4. Microcopy

**C4.1** List every error this service can produce. Minimum 15. Source them from the live flow, the constraint list, and the upload rules.
Commit: `students/UX{n}/week2/C4-1-error-inventory.md`

**C4.2** Write every error message from C4.1. Each must say what happened, why, and what to do next. No error codes as the primary message. No "something went wrong" anywhere.
Commit: `students/UX{n}/week2/C4-2-error-messages.md`

**C4.3** Write the confirmation screen copy. The citizen has paid ₹50 and will wait up to 30 days. State what happens next, when, how they will know, and what to do if nothing happens. Include how the URN is preserved.
Commit: `students/UX{n}/week2/C4-3-confirmation-copy.md`

**C4.4** Take three of your messages and rewrite them for a reader who is slow in English. Shorter words, shorter sentences, same information. Note what you could not simplify and why.
Commit: `students/UX{n}/week2/C4-4-plain-language.md`

### S2. First components

**S2.1** Contribute one component to the shared system: button, text input, select, or file upload. Assigned by the system owner so all four get built. Include every state, every variant, accessibility notes, and usage guidance with one do and one do not.
Commit: `system/components/{component}.md` plus the Figma component in the shared library

**S2.2** Review one peer's component contribution. Your review must name one thing that will break when someone else uses it. "Looks good" is not a review.
Commit: as a pull request comment, logged in `system/docs/review-log.md`

**S2.3** Write the focus and keyboard behaviour for your component. Where does focus go, what does Tab do, what does Escape do, what does a screen reader announce.
Commit: inside `system/components/{component}.md` under a Keyboard and screen reader section

**S2.4** Semantic HTML for your component. Which element, and one sentence on why that element and not a div with a click handler.
Commit: inside `system/components/{component}.md` under a Markup section

### Spine, week 2

**F2.1** Why session: visual hierarchy and whitespace. Presenter shows one screen from the cohort's own week 2 work and rebuilds its hierarchy live.
Commit: `fundamentals/why-sessions/week02-hierarchy.md`

**F2.2** Teardown: a state electricity board bill payment flow.
Commit: `fundamentals/teardowns/02-electricity-payment.md`

**F2.3** Drill continues. Same log file.

---

## Week 3: Test and fix

### R2. Test your own flow `[MILESTONE]`

**R2.1** Write a test plan: three tasks, success criteria for each, and what you expect to go wrong. Writing the prediction first is the point.
Commit: `students/UX{n}/week3/R2-1-test-plan.md`

**R2.2** Write the moderator script. Every question must be non leading. Include the two questions you almost wrote in a leading form, and the corrected version of each.
Commit: `students/UX{n}/week3/R2-2-script.md`

**R2.3** Run the test with three participants on your own prototype. At least one participant must be over 50 or slow in English. Record task success, time, and where they hesitated.
Commit: `students/UX{n}/week3/R2-3-test-results.md`

**R2.4** Severity rate every issue found: 1 cosmetic, 2 minor, 3 major, 4 catastrophic. Justify every 3 and 4 with the user cost.
Commit: `students/UX{n}/week3/R2-4-severity.md`

**R2.5** Write what surprised you. Something must have. If nothing did, either the prototype was too simple or the tasks were too easy, and say which.
Commit: `students/UX{n}/week3/R2-5-surprises.md`

### C5. All states

**C5.1** Every screen, every state. Default, empty, loading, partial, error, success, offline, permission denied, zero results, first run, destructive confirm where relevant. Use the checklist in `accessibility-gate.md` section 2.
Commit: `students/UX{n}/week3/C5-1-states-matrix.md` plus a Figma link

**C5.2** The loading state for document upload on 3G. Show what the user sees at 0, 3, 15, and 45 seconds. State which of those needs a different design and why.
Commit: `students/UX{n}/week3/C5-2-loading-timeline.md`

**C5.3** Session expiry. Priya's rental agreement takes 8 minutes to find. Design what happens to her typed data. State where it is stored and what you promise the user.
Commit: `students/UX{n}/week3/C5-3-session-expiry.md`

**C5.4** Rejection state. The request came back rejected 12 days later with a reason code. Design the screen that turns that code into an action, including whether the ₹50 has to be paid again and how you say so.
Commit: `students/UX{n}/week3/C5-4-rejection.md`

### S3. Fix from evidence

**S3.1** Fix the top three severity issues from R2.4. For each, commit a before and after with the test finding quoted as the reason for the change.
Commit: `students/UX{n}/week3/S3-1-fixes.md`

**S3.2** One issue you are not fixing. State why: out of scope, low severity, or the fix costs more than the problem. Defend it in writing.
Commit: `students/UX{n}/week3/S3-2-wont-fix.md`

**S3.3** If a fix required a system change, open it as a system pull request rather than a local override. If you overrode locally instead, write one line on why the system could not absorb it.
Commit: `system/components/{component}.md` update or `students/UX{n}/week3/S3-3-override-note.md`

### The injected failure

Delivered by the core admin on the Monday of week 3. Sealed until then. See the post mortem task.

**X1.1** Post mortem. What changed, what it broke in your work, what you did, how much time it cost, and what earlier decision would have made it cheaper.
Commit: `students/UX{n}/week3/X1-1-postmortem.md`

### Spine, week 3

**F3.1** Why session: cognitive load and progressive disclosure, using the cohort's own address entry screens as material.
Commit: `fundamentals/why-sessions/week03-cognitive-load.md`

**F3.2** Teardown: any insurance claim submission flow.
Commit: `fundamentals/teardowns/03-insurance-claim.md`

**F3.3** Whiteboard why, week 3. Fifteen minutes, no notes. Draw your flow from memory, answer three questions drawn at random. Admin records the result.
No commit. Admin logs it.

---

## Week 4: Ship and defend

### C6. High fidelity

**C6.1** Full flow at high fidelity, 390px and 1440px. The desktop version is not the mobile version stretched. State one layout decision that differs between the two and why.
Commit: `students/UX{n}/week4/C6-1-final-flow.md` plus a Figma link

**C6.2** Dark mode for three screens using your semantic tokens. If the tokens do not support it, that is a system finding, so log it.
Commit: `students/UX{n}/week4/C6-2-dark-mode.md`

**C6.3** One motion specification: what animates, duration, easing, what it explains to the user, and the reduced motion alternative.
Commit: `students/UX{n}/week4/C6-3-motion-spec.md`

**C6.4** Language expansion test. Take your three densest screens with Hindi text 30 percent longer than English. Show what breaks and how you fixed it.
Commit: `students/UX{n}/week4/C6-4-language-expansion.md`

### S4. Gate and handoff `[MILESTONE]`

**S4.1** Run the full accessibility gate on your primary flow. Every line answered with evidence, not a tick. Include a screen reader pass with the announced text written out.
Commit: `students/UX{n}/week4/S4-1-gate-result.md`

**S4.2** Handoff spec for the upload screen: component references from the shared system, spacing values, states, validation rules, error copy, focus order, and what the engineer needs from the backend.
Commit: `students/UX{n}/week4/S4-2-handoff-spec.md`

**S4.3** Read one peer's handoff spec as if you were the engineer. Write the three questions you would have to ask before you could build it. Those three questions are the gaps.
Commit: `students/UX{n}/week4/S4-3-handoff-review.md`

**S4.4** Cohort session. The shared system: does the documentation match what is actually in it. Fix the drift. Write the changelog.
Commit: `system/docs/CHANGELOG.md`

### P3. Decisions and delivery

**P3.1** Decision record for the choice a department official would most likely question. Format: context, two options considered, decision, consequences including the bad ones, and what would make you revisit it.
Commit: `fundamentals/adr/ADR-{n}-{title}.md`

**P3.2** Two minute version of your work. What the problem was, what you changed, what evidence you have. No screens shown until the problem is stated.
Commit: `students/UX{n}/week4/P3-2-two-minute-script.md`

**P3.3** Cohort session. One shared presentation to the department. Five designers, one narrative, not five portfolios. Assign sections.
Commit: `delivery/presentation/sprint1-deck.md`

**P3.4** Write what you would do with four more weeks, in priority order, with the reason each item is above the next.
Commit: `students/UX{n}/week4/P3-4-next-four-weeks.md`

### Spine, week 4

**F4.1** Why session: affordances, signifiers, and mental models, from Norman chapters 1 to 4, applied to your own upload component.
Commit: `fundamentals/why-sessions/week04-affordances.md`

**F4.2** Teardown: a subscription cancellation flow of your choice. Name every dark pattern and the regulation it may run into.
Commit: `fundamentals/teardowns/04-cancellation.md`

**F4.3** Explainer. Pick one concept from this sprint you can now explain properly. Format: plain definition, the problem it solves, an example from this project, what breaks if you get it wrong, and one thing still unclear to you.
Commit: `fundamentals/explainers/UX{n}-sprint1.md`

**F4.4** The defense. Six parts, 55 minutes. See `../../Program Structure.md` section 7.
No commit. Admin logs the result in the ledger.

---

## Task count

| Track | Tasks |
|---|---|
| Craft and Interface (C) | 18 |
| Research and Evidence (R) | 10 |
| Product and Business (P) | 11 |
| Systems and Technical (S) | 11 |
| Spine (F) and failure (X) | 13 |
| **Total** | **63** |

Roughly 15 to 16 tasks per week across a 12 to 15 hour week. If a week runs long, the C tasks compress and the R, S, and F tasks do not. Craft can be polished later. Evidence, systems, and understanding cannot be retrofitted.
