# Week 4 — Ship and Defend

**Sprint 1 · Week 4 of 4 · Theme: accessibility, high fidelity, handoff, and the defense**

---

## By the end of this week you can

- Run a WCAG AA accessibility gate on your own work with evidence on every line
- Use a screen reader on your own design and fix what you hear
- Write a handoff spec an engineer can build from without asking you a question
- Defend every decision you made for four weeks, out loud, without your files

## The week at a glance

| Step | LEARN | DO |
|---|---|---|
| **1** | WCAG 2.2 AA, the 12 criteria that matter here | C7.1 C7.2 — keyboard and focus, contrast pass |
| **2** | web.dev Learn Accessibility · Deque screen reader module | C7.3 C7.4 — screen reader run, target sizes and motion |
| **3** | Refactoring UI on finishing touches | C8.1 C8.2 — high fidelity, desktop |
| **4** | Norman ch. 1–4 · your own decision records | S4.1 P4.1 — handoff spec, decision record · **critique** |
| **5** | — | **Defense, 55 min each** · P4.2 reflection |
| **6** | — | S5 system handover · F4 sprint retro |

---

# the start of the week

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **WCAG 2.2 Quick Reference** | Filter to AA. Read these 12 in full: 1.3.1 Info and Relationships · 1.4.1 Use of Color · 1.4.3 Contrast · 1.4.11 Non-text Contrast · 1.4.12 Text Spacing · 2.1.1 Keyboard · 2.4.3 Focus Order · 2.4.7 Focus Visible · 2.5.8 Target Size · 3.3.1 Error Identification · 3.3.2 Labels or Instructions · 4.1.2 Name, Role, Value | 50 min |
| **web.dev Learn Accessibility** | The "Focus" and "Keyboard" modules | 25 min |
| **The A11y Project** | The checklist page, skimmed so you know it exists | 15 min |

**What to take:** these 12 criteria cover almost everything a form-based flow can get wrong. You are not memorising WCAG. You are learning to look up the right criterion and cite it by number, because "this is inaccessible" loses an argument and "this fails 1.4.3, measured at 2.85:1" wins it.

→ **Commit** `students/UX{n}/week4/session1-learning.md`

## DO — 2 hours

### C7.1 — Keyboard and focus

**Learn first:** WCAG 2.1.1, 2.4.3, 2.4.7 from this study time.

**Method**
1. Make your prototype keyboard operable, in the design: define the tab order for every screen.
2. Draw the focus order on every screen as numbered annotations. It must follow reading order. If it does not, either the layout or the order is wrong.
3. Design the focus indicator. It must pass 3:1 contrast against both the component and the background behind it (1.4.11). A 1px light grey outline fails.
4. Define keyboard behaviour for every interactive thing: what Enter does, what Space does, what Escape does, whether focus is trapped in any modal and how it gets out.
5. Define where focus goes after every action: after submit, after an error appears, after a modal closes, after a step transition.

**Point 5 is the one everyone forgets.** If an error summary appears and focus stays where it was, a screen reader user never learns the error exists.

**Worked example**

> **Screen:** Address entry, after a failed submit.
> Focus moves to the error summary heading at the top of the form. The summary is `role="alert"` so it is announced immediately. Each error in the summary is a link to its field. Tab order from there: first error link → second error link → back into the form at the first failed field.
> **Why:** the user needs to know a) that something failed, b) how many things failed, c) how to reach each one. Leaving focus on the submit button gives them none of that.

**Done when**
- [ ] Focus order annotated on every screen, matching reading order
- [ ] Focus indicator designed and measured against 1.4.11 at 3:1
- [ ] Enter, Space, Escape defined for every interactive element
- [ ] Focus destination defined after submit, after error, after modal close
- [ ] Any modal has documented focus trapping and a documented escape

→ `students/UX{n}/week4/C7-1-keyboard-focus.md`

### C7.2 — Contrast pass

**Learn first:** WCAG 1.4.3 and 1.4.11.

**Method**
1. Every text element in your flow: measure it. Body needs 4.5:1, large text (24px+, or 19px+ bold) needs 3:1.
2. Every non-text element that conveys meaning: borders, icons, focus rings, chart elements. 3:1 (1.4.11).
3. **Disabled elements too.** People assume disabled is exempt. It is not exempt from being findable, and a disabled button nobody can see is a support call.
4. Every failure: record the measured ratio, the required ratio, and what you changed.

**Done when**
- [ ] Every text element measured, with its ratio recorded
- [ ] Every meaningful non-text element measured
- [ ] Disabled states included
- [ ] Zero remaining failures, or each one justified with why it cannot be fixed and what mitigates it

→ `students/UX{n}/week4/C7-2-contrast-pass.md`

---

# early in the week

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **Deque University** | The free screen reader module. Learn to navigate by heading and by form control. | 35 min |
| **web.dev Learn Accessibility** | The "Forms" and "ARIA and HTML" modules | 30 min |
| **WCAG** | 4.1.2 Name, Role, Value and 3.3.2 Labels or Instructions, in full | 25 min |

**What to take:** every interactive element must announce its name, its role, and its current value. An icon button with no accessible name announces as "button", which tells a blind user nothing. That is a defect, not a nicety.

→ **Commit** `session2-learning.md`

## DO — 2 hours

### C7.3 — Screen reader run

**Method**
1. Turn on VoiceOver (`Cmd+F5`) or NVDA.
2. Run your prototype, or a coded version of one screen if your prototype cannot be read.
3. **Write down what it actually says.** Verbatim. Not what you hoped it would say.
4. Where a coded prototype is not possible, write the intended announcement for every element and mark it as specified rather than verified. Be honest about which is which.
5. Fix what you hear.

**Worked example**

| Element | What was announced | Problem | Fix |
|---|---|---|---|
| The ⓘ help icon next to PIN | "button" | No accessible name at all. 4.1.2 fail. | `aria-label="What is a PIN code?"`, spec'd in the handoff |
| PIN field with an error | "PIN code, edit text" | The error is visible but never announced. 3.3.1 fail. | Link the error text with `aria-describedby`; announce as "PIN code, edit text, PIN code must be 6 digits" |
| Progress "Step 2 of 4" | not announced at all | Decorative markup. The user has no idea where they are. | Make it a real heading, and announce step changes via a live region |

**Done when**
- [ ] Every interactive element's announcement recorded verbatim, or specified and clearly marked as unverified
- [ ] Every icon button has an accessible name
- [ ] Every error is programmatically linked to its field
- [ ] Step or progress information is announced
- [ ] Every problem has a fix, specified precisely enough for an engineer

→ `students/UX{n}/week4/C7-3-screen-reader-run.md`

### C7.4 — Target sizes and motion

**Learn first:** WCAG 2.5.8 Target Size and 2.3.3 Animation from Interactions.

**Method**
1. Measure every tappable target. Minimum 24 × 24 px (2.5.8 AA). 44 × 44 is the practical recommendation for a service used on cheap phones in a hurry.
2. Check spacing between adjacent targets. Two 24px targets touching each other is a mis-tap generator.
3. For every animation or transition over 200ms, define the reduced-motion alternative. `prefers-reduced-motion` is not optional for a government service.
4. State what each animation is *for*. Animation that does not communicate a state change or a spatial relationship should be removed, not reduced.

**Done when**
- [ ] Every target measured, minimum met, smallest one named
- [ ] Adjacent target spacing checked
- [ ] Every animation over 200ms has a reduced-motion alternative
- [ ] Every animation has a stated purpose, or has been deleted

→ `students/UX{n}/week4/C7-4-targets-motion.md`

---

# mid week

## LEARN — 60 minutes

| Source | What exactly | Time |
|---|---|---|
| **Refactoring UI** | The chapters on finishing touches, shadows and depth, and working with images | 40 min |
| **Your own week 1 tokens** | Re-read C1.1, C1.2, C2.1. You are about to use them at full fidelity. | 20 min |

→ **Commit** `session3-learning.md`

## DO — 2 hours

### C8.1 — High fidelity, mobile

**Method**
1. Take every screen and bring it to full fidelity at 390px.
2. Full fidelity means: final type, final colour, final spacing, final icons, real content, all states present, and nothing left undecided.
3. **Every value must come from a token.** If you type a hex code or a pixel value directly, either it belongs in the system or you are taking a shortcut. Log it either way.
4. Shadows and depth are the last thing you add, and only where they communicate elevation. Not for decoration.

**Done when**
- [ ] Every screen at full fidelity, 390px
- [ ] Zero hardcoded values, or each one logged with a reason
- [ ] Every state from your C5.1 matrix is present or explicitly deferred
- [ ] Real content throughout
- [ ] All of C7.1 to C7.4 reflected in the final screens
- [ ] Figma link plus exported PNGs

→ `students/UX{n}/week4/C8-1-high-fidelity-mobile.md`

### C8.2 — Desktop at 1440px

**Method**
1. Adapt, do not stretch. A 1440px form with a 1200px-wide input is worse than the mobile version.
2. Apply your measure limit from C1.3. Line length rules do not change because the viewport got wider.
3. State what you changed and why for each screen: a two-column layout, a sidebar for guidance, a persistent summary. Each needs a reason.
4. Name at least one thing that is genuinely better on desktop and one thing that is worse.

**Done when**
- [ ] Every screen at 1440px
- [ ] Measure limit respected
- [ ] Every layout change has a stated reason
- [ ] One thing better and one thing worse, both named
- [ ] Figma link

→ `students/UX{n}/week4/C8-2-desktop.md`

---

# late in the week

## LEARN — 60 minutes

| Source | What exactly | Time |
|---|---|---|
| **The Design of Everyday Things**, Norman | Ch. 1–4: affordances, signifiers, mapping, feedback, conceptual models | 45 min |
| **Your own decision files** | Read P1.2, P2.3, P3.1 and X1 in order, as one story | 15 min |

**Why Norman now, in week 4:** you have spent four weeks making concrete decisions. Reading Norman before that would have been abstract. Reading it now, you will recognise your own week 2 mistakes described in a book from 1988, which is a more useful experience than reading it first.

→ **Commit** `session4-learning.md`

## DO — 2 hours (plus critique)

### S4.1 — Handoff spec

**Method**
For every screen, document:
1. Layout: grid, breakpoints, max widths — as tokens, not screenshots
2. Every component used, and whether it is from `system/` or new
3. Every interaction: trigger, result, duration
4. Every state and what triggers the change into it
5. Validation rules per field, exactly as in C3.3
6. Every error message, exactly as in C4.2, with its position
7. Accessibility: focus order, ARIA where needed, announcements
8. Anything you know is unresolved

**The test:** an engineer who has never spoken to you should be able to build it without asking you a single question. Any question they would need to ask is a gap in your spec.

Point 8 matters. "Unknown: whether submit is idempotent, needs a backend answer" is a professional spec. Silence on that point is not.

**Done when**
- [ ] All 8 sections for every screen
- [ ] Values given as tokens
- [ ] Every unresolved item listed as a question with who can answer it
- [ ] No screenshot used as a substitute for a specification

→ `students/UX{n}/week4/S4-1-handoff-spec.md`

### P4.1 — Decision record

**Method**
1. Pick the one decision a department official would most likely challenge.
2. Write: the context · the options considered · the decision · the reason with evidence · the consequences, good and bad · what would change your mind.
3. One page. If it takes more, you have not decided anything.

**Done when**
- [ ] The genuinely contentious decision, not a safe one
- [ ] At least two real alternatives, described fairly
- [ ] Evidence cited from your own R2.4 or from a named convention
- [ ] Negative consequences stated
- [ ] What would change your mind, stated concretely
- [ ] One page

→ `students/UX{n}/week4/P4-1-decision-record.md`

### The accessibility gate

Run the full checklist in `06-accessibility-gate.md`. Every line needs evidence: a measurement, a screenshot, or a quoted screen reader announcement.

**This is a gate, not a review.** Fail it and the sprint is not done, regardless of how the work looks.

→ `students/UX{n}/week4/accessibility-gate-signed.md`

### the week's critique — 90 minutes
Final critique. Present your full flow. The critique lead files the final log for the sprint.

---

# the end of the week

## Defense — 55 minutes each

No files. No notes. Your own diagram, drawn live.

| Part | Time | What you do |
|---|---|---|
| Flow walk | 10 min | Draw your flow from memory and walk it. Every branch. |
| Terminology and tradeoff | 10 min | Define terms you used, with the tradeoff attached |
| Failure story | 10 min | The week 3 injection: what it cost, what you would have done differently |
| Business framing | 5 min | What the department gets, in their terms |
| Evidence defense | 10 min | Defend your three-person study. Sample size, what you cannot claim. |
| Alternative design | 10 min | A constraint card is drawn. Redesign under it, out loud. |

**Sprint 1 constraint cards:** no colour available · screen reader only · 2G connection · feature phone, no smartphone · one hand, in sunlight, standing in a queue · the department will not allow document upload at all.

**To pass, all four:**
1. Correct vocabulary used correctly
2. One piece of evidence you can defend, including its limits
3. One coherent alternative design under the constraint drawn
4. One honest "I do not know yet, and here is how I would find out"

## P4.2 — Reflection

After your defense, written straight away while it is uncomfortable:
- The question you answered worst, and what you now know you do not understand
- The strongest thing in your work, with the reason it is strong
- The weakest, with the reason
- What you will do differently in Sprint 2, as one specific behaviour

→ `students/UX{n}/week4/P4-2-reflection.md`

---

# the cohort review

## S5 — System handover, 90 minutes

### S5.1 — Sprint 1 system release
Tokens final. Every component documented with all states. A changelog written.
→ `system/docs/CHANGELOG.md`, `system/docs/README.md`

### S5.2 — Dark mode test
Add a dark mode to your semantic tokens only. Zero changes to any component allowed. If a component breaks, your token layer was not doing its job, and that is the finding.
→ `system/docs/dark-mode-test.md`

### S5.3 — Debt list
Everything the system got wrong or left undone in Sprint 1, written for the next system owner. This is what Sprint 4 starts from.
→ `system/docs/debt.md`

## F4 — Sprint retro

**F4.1 — Why session: affordances, signifiers and mental models.** Every concept illustrated with something the cohort actually built or broke in the last four weeks.
→ `fundamentals/why-sessions/week04-affordances.md`

**F4.2 — Teardown:** a subscription cancellation flow. Assigned deliberately, because this is where dark patterns live and you are about to study them properly in Sprint 3.
→ `fundamentals/teardowns/04-cancellation-flow.md`

**F4.3 — Explainer.** Write a one-page explanation of one Sprint 1 concept for someone who has never designed anything. No jargon. If you cannot do it, you learned the words and not the idea.
→ `fundamentals/explainers/sprint1-{topic}.md`

**F4.4 — Drill log review.** 20 entries. Read them and note what you consistently get wrong from memory. That is your visual blind spot, and now you know it.

---

## Sprint 1 done when

- [ ] 20 learning summaries across 4 weeks
- [ ] Every week's tasks committed
- [ ] Accessibility gate signed with evidence on every line
- [ ] Handoff spec complete
- [ ] Decision record written
- [ ] Post mortem written
- [ ] Defense passed, or a re-run scheduled in the buffer week
- [ ] Reflection written
- [ ] System released with a changelog and a debt list
- [ ] 4 teardowns, 1 explainer, 20 drill entries

Next: `../Design-Sprint-2/00-READ-FIRST.md`
