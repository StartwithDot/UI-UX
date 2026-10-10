# 08 — Prototyping And Responsive Design

Junior portfolios are judged on two things the main sprints touch but never isolate: **can this person make something that behaves**, and **does their work survive a different screen size, language and platform**.

This file adds four labs that make both explicit. They sit on the week's Day 6 (cohort day).

| ID | Week | Time | Name | You prove |
|---|---|---|---|---|
| **L-PR1** | 3 | 2 h | Responsive behaviour and platform conventions | Your layout is a set of rules, not a set of frames |
| **L-PR2** | 10 | 2 h | A prototype with logic | A stranger can use your prototype without you explaining it |
| **L-PR3** | 13 | 90 min | Components that survive stress | Your components hold at 200% zoom and in three scripts |
| **L-PR4** | 18 | 90 min | Choose the fidelity | You can say what a prototype needs to be, and no more |

---

## L-PR1 — Responsive behaviour and platform conventions (week 3)

**Learn first:** Figma Learn on Auto Layout (min/max width, hug, fill, wrap), and Refactoring UI ch. 3, "Relative sizing doesn't scale".

**Method**
1. Take three screens from your Sprint 1 flow. For each, write down how it behaves at 360, 390, 768, 1024 and 1440 px: what reflows, what stays fixed, what truncates, what wraps, what moves behind a control.
2. Name breakpoints by the content that breaks, not by device names. ("Below 600 px the two columns stack because the summary no longer fits beside the form.")
3. Build each screen with Auto Layout so that the rules in step 1 are enforced by the layout, not by redrawing. Resize the frame by dragging and screenshot every failure. Then open one screen as real HTML and CSS (a plain page is enough) and compare: where would a **container query** let a component respond to the space it is given rather than to the screen? Name two components in your flow that should.
4. Write a list of ten ways your layout broke when you resized it, and the fix for each.
5. **Platform conventions.** Choose one pattern in your flow (navigation back, confirmation dialog, or date entry). Show how the **current** Apple HIG and Material 3 each handle it. Both platforms changed their visual language in 2025, so do not use screenshots from old tutorials. State which you followed, and why that is right for your users' phones.

**Done when**
- [ ] Behaviour table for three screens at five widths
- [ ] Breakpoints named by content
- [ ] Ten resize failures documented with fixes
- [ ] Two components identified that should respond to their container
- [ ] A one-page platform comparison with your choice justified

→ `students/UX{n}/week3/L-PR1-responsive.md`

---

## L-PR2 — A prototype with logic (week 10)

**Learn first:** Figma Learn on prototyping with variables and conditionals; your I1.1 state machine.

**Method**
1. Build a prototype of the subscription flow in which the **state is real**: a variable holds whether the subscription is active, paused or past due, and the screens change with it. A paused user cannot pause again; a past-due user sees the update-card path.
2. Include the transitions from your motion spec (I2.4), with the reduced-motion version reachable.
3. Give it to one person who has never seen it, with only the instruction *"cancel the plan but keep your data"*. Do not speak. Record the screen.
4. Log every hesitation over three seconds and every wrong tap.
5. Fix the two worst problems and test again with a second person.

**Done when**
- [ ] The prototype's logic matches the state machine
- [ ] Two recorded sessions, hesitations logged
- [ ] Two fixes traced to logged moments
- [ ] A 20-second screen recording for your portfolio

→ `students/UX{n}/week10/L-PR2-logic-prototype.md`

---

## L-PR3 — Components that survive stress (week 13)

**Learn first:** WCAG 1.4.4 Resize Text and 1.4.10 Reflow; your T1.3 theming work.

**Method**
1. Take one component you contributed to the system (a text input or a button works).
2. Stress it four ways and screenshot each: browser zoom at 200%, a label three times longer than expected, the Devanagari and one other script you can read or find sample strings for, and the longest word in the cohort's content.
3. List what broke. Fix the component and its documentation so the behaviour is specified: wrap, truncate, grow, or reflow.
4. Add a "stress states" section to the component's file in `system/components/`.

**Done when**
- [ ] Four screenshots of stress cases
- [ ] A fix or a written decision for each break
- [ ] The component documentation updated and merged

→ `students/UX{n}/week13/L-PR3-stress.md`

---

## L-PR4 — Choose the fidelity (week 18)

**Learn first:** your K3.1 test plan draft, and Rocket Surgery Made Easy on what to test and what to fake.

**Method**
1. List your three riskiest assumptions in the design.
2. For each, write the cheapest prototype that could prove it wrong: paper, clickable low fidelity, high fidelity with logic, or a coded fragment. Justify the fidelity.
3. Apply the **"would a participant know it is fake"** test. Name the three moments in your prototype where a participant would see the seam, and how you will handle each (a script line, a fake, a fix).
4. Build only the prototype you need for week 19. Cut everything else.

**Done when**
- [ ] Three assumptions, three fidelity choices, three reasons
- [ ] Three seams identified and handled
- [ ] A test-readiness checklist the admin can run in five minutes

→ `students/UX{n}/week18/L-PR4-fidelity.md`

---

Next: back to `00-START-HERE.md`, or on to your sprint folder.
