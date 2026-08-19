# Week 1 — Frame

**Sprint 1 · Week 1 of 4 · Theme: understand the problem and build your visual foundations**

Read this whole file on Monday morning before you start. Then work one day at a time.

---

## By Friday you can

- Turn a vague client request into a problem statement with a metric attached
- Audit a live service and name what is wrong using named heuristics, not opinions
- Build a type scale, a spacing scale, and a colour ramp, and explain why each step exists
- Make hierarchy work in greyscale, with no colour at all

## You do not design any screens this week

That is deliberate. This week is understanding plus foundations. Screens start in week 2.

---

## The week at a glance

| Day | LEARN (morning) | DO (afternoon) |
|---|---|---|
| **Mon** | Refactoring UI ch. 1–2 · Figma Learn: Auto Layout | P1.1 P1.2 — reframe the brief |
| **Tue** | Nielsen's 10 heuristics · WCAG 2.2 AA skim | R1.1 R1.2 R1.3 — audit the live service |
| **Wed** | Practical Typography · Refactoring UI ch. 3 (type) | C1.1 C1.2 C1.3 — type and spacing scales |
| **Thu** | Refactoring UI ch. 4 (colour) · Leonardo docs | C2.1 C2.2 — colour system · **critique 90 min** |
| **Fri** | Refactoring UI ch. 5–6 (hierarchy, depth) | C1.4 P1.3 P1.4 — greyscale hierarchy, constraints, metrics |
| **Sat** | — | S1 cohort session · F1 why session and teardown |

---

# Monday

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **Refactoring UI** | Ch. 1 "Starting from Scratch", Ch. 2 "Hierarchy is Everything" | 45 min |
| **Figma Learn** | "Auto layout" lesson | 20 min |
| **Figma Learn** | "Components and instances" lesson | 15 min |
| **The live service** | Use `myaadhaar.uidai.gov.in` on your own phone, with your own Aadhaar | 10 min |

**What to take from Refactoring UI ch. 1–2:** start with too much white space and remove it, not the other way round. Hierarchy is created by size, weight, and colour together, and using all three at once is usually wrong. De-emphasising is as powerful as emphasising.

→ **Commit** `students/UX{n}/week1/day1-learning.md` using the summary template in root `02-Learning-Path.md`.

## DO — 90 minutes

### P1.1 — Find what the brief does not answer

**Learn first:** nothing from Refactoring UI. This one comes from reading the brief carefully.

The department's brief is: *"make it so people stop coming to the counter."*

**Method**
1. Read `01-project-brief.md` sections 1 to 4 again.
2. For each of these, ask yourself whether the brief tells you: who exactly comes to the counter, why they come, what proportion could have finished online, what the department will accept as success.
3. Pick the three gaps that would most change your design if answered.
4. For each: write the question, who could answer it, and how long getting that answer would take.

**Worked example** — for a different brief, *"make our returns process better"*:

> **Question:** What percentage of returns are because the item was wrong versus because the customer changed their mind?
> **Who could answer:** Support team lead, from the returns reason field in the admin tool.
> **How long:** One afternoon, if the field is mandatory. Two weeks if it is free text and has to be coded.
> **Why it changes the design:** If most returns are "wrong item", the fix is in the product page, not the returns flow.

**Done when**
- [ ] Three questions, each one the brief genuinely does not answer
- [ ] Each has a named person or source who could answer it
- [ ] Each has a realistic time estimate
- [ ] Each has one line on why the answer would change your design

→ `students/UX{n}/week1/P1-1-brief-questions.md`

### P1.2 — Rewrite the brief as a problem statement

**Learn first:** the users in `01-project-brief.md` section 4.

**Method**
1. Use exactly this shape:
   `[user] cannot [job] because [obstacle], which costs [cost to user] and [cost to department].`
2. Write it for the user whose failure is most common, not the most dramatic.
3. Remove every solution word. If your statement contains "redesign", "simplify", "add", "app", or a screen name, it is a solution, not a problem.
4. One paragraph maximum.

**Worked example** — for a different service, a driving licence renewal:

> A licence holder who has moved cities cannot renew online because the system requires the renewal to be filed at the office that issued the original licence, which costs them a day of travel and costs the department a counter appointment that produces no new information.

Note what it does: names the user, names the job, names the obstacle as a rule not a screen, and states both costs. No solution.

**Done when**
- [ ] Follows the shape exactly
- [ ] Zero solution words
- [ ] Both costs stated, one for the user and one for the department
- [ ] A department official would agree it is accurate

→ `students/UX{n}/week1/P1-2-problem-statement.md`

---

# Tuesday

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **NNGroup** | "10 Usability Heuristics for User Interface Design" — the main article plus the definition of each heuristic | 30 min |
| **WCAG 2.2 Quick Reference** | Filter to **Level AA only**. Read the criteria under Perceivable and Operable. Do not try to memorise. | 30 min |
| **axe DevTools** | Install it, run it once on any website, read the output | 15 min |
| **Refactoring UI** | Ch. 2 again, the section on de-emphasising | 15 min |

**What you need out of the heuristics:** the name, and one sentence on what it costs a user when it is violated. "Visibility of system status" is not a phrase to recite, it is the reason a person taps a button four times when nothing appears to happen.

→ **Commit** `day2-learning.md`

## DO — 2 hours

### R1.1 — Screenshot the live flow

**Method**
1. On your phone, walk the live address update flow at `myaadhaar.uidai.gov.in`. Use only your own Aadhaar.
2. Screenshot every screen in order.
3. Now trigger errors on purpose: upload a file that is too large, upload a `.txt`, enter a wrong OTP, leave a required field empty, wait long enough for a session to expire.
4. Screenshot every error too.
5. Name files in order: `01-login.png`, `02-otp.png`, `03-error-wrong-otp.png`.

**Done when**
- [ ] Every screen you reached is captured, in order
- [ ] At least 4 error states captured
- [ ] A `README.md` listing each file with one line on what the screen is for
- [ ] No screenshot contains anyone's Aadhaar number, including yours — redact it

→ `students/UX{n}/week1/R1-1-current-flow-screens/`

### R1.2 — Heuristic evaluation

**Learn first:** the 10 heuristics you read this morning.

**Method**
1. Go through your screenshots one at a time.
2. For each problem: name the screen, name the heuristic violated, describe what the *user experiences*, then rate severity.
3. Severity scale: 1 cosmetic · 2 minor, they work around it · 3 major, they fail the task · 4 catastrophic, they lose data or money.
4. Minimum 12 findings. Table format.

**Worked example** — from a different government portal:

| Screen | Heuristic violated | What the user experiences | Severity |
|---|---|---|---|
| Payment confirmation | Visibility of system status | After tapping Pay, nothing changes for 9 seconds. No spinner, no disabled button. The user taps Pay a second time and is charged twice. | 4 |
| Document upload | Help users recognise, diagnose and recover from errors | Error reads "ERR_UPLOAD_422". No mention of file size, and the actual limit is never stated anywhere on the page. | 3 |

Note what makes these valid: the user's experience is described in concrete behaviour, and the severity is justified by the consequence.

**Not a finding:** "looks outdated", "the colours are ugly", "not modern". Those have no user cost attached.

**Done when**
- [ ] 12 or more findings
- [ ] Every finding names one of the 10 heuristics
- [ ] Every "what the user experiences" describes behaviour, not aesthetics
- [ ] Every severity 3 or 4 has the consequence spelled out

→ `students/UX{n}/week1/R1-2-heuristic-audit.md`

### R1.3 — Accessibility audit

**Learn first:** the WCAG AA criteria you skimmed this morning. You do not need all of them, you need the six below.

**Method**
1. **Keyboard only.** Unplug your mouse or do not touch the trackpad. Try to complete the flow with Tab, Shift+Tab, Enter, and Space. Note where you get stuck.
2. **Focus visible.** Tab through and note every element where you cannot see what is focused. (WCAG 2.4.7)
3. **Contrast.** Pick 5 text elements. Use axe DevTools or the WebAIM contrast checker. Body text needs 4.5:1, large text 3:1. (WCAG 1.4.3)
4. **Form labels.** For each field, check there is a real `<label>`, not just placeholder text. Turn on your screen reader and listen to what one field announces. (WCAG 1.3.1, 4.1.2)
5. **Target size.** Measure the smallest tappable thing. Under 24 × 24 px fails. (WCAG 2.5.8)
6. **Colour alone.** Find anything where colour is the only signal — a red border with no text, for example. (WCAG 1.4.1)

**Worked example**

| Check | Result | WCAG criterion | Evidence |
|---|---|---|---|
| Keyboard only | Fail. The date picker cannot be opened with Enter or Space, only a click. | 2.1.1 Keyboard | Tabbed to the field, pressed Enter and Space, nothing opened |
| Contrast, hint text | Fail. #9A9A9A on #FFFFFF = 2.85:1, needs 4.5:1 | 1.4.3 Contrast (Minimum) | WebAIM checker screenshot |

**Done when**
- [ ] All six checks done, each with pass or fail
- [ ] Every failure names its WCAG criterion number
- [ ] Every failure has evidence: a measurement, a screenshot, or what the screen reader said
- [ ] The keyboard-only attempt is described, including where you gave up

→ `students/UX{n}/week1/R1-3-accessibility-audit.md`

---

# Wednesday

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **Practical Typography** | "Summary of key rules" then the "Type composition" section: point size, line spacing, line length | 40 min |
| **Refactoring UI** | Ch. 3, the typography chapter: establish a type scale, limit your font weights, don't use grey text on coloured backgrounds | 30 min |
| **typescale.com** | Open it and try three different ratios on the same base size. Look at what happens to the top end. | 20 min |

**What you need out of this:** a scale is a small fixed set of sizes chosen on purpose, so you never again pick a font size by eye. The reason is consistency and speed of decision, not mathematical beauty.

→ **Commit** `day3-learning.md`

## DO — 2 hours

### C1.1 — Build a type scale

**Learn first:** Refactoring UI ch. 3, the "establish a type scale" section. Practical Typography on point size and line spacing.

**Method**
1. Pick your base body size. For a government service on cheap Android phones, 16px is the floor, 17–18px is safer.
2. Pick a ratio. 1.2 (minor third) is calm and useful for dense UI. 1.25 (major third) is a good default. 1.333 gets dramatic fast.
3. Generate the steps at typescale.com. Round every value to a whole pixel. Do not ship 17.36px.
4. Give every step a name and a use. A step with no use gets deleted.
5. Set line height per step: tight for large text (1.1–1.2), looser for body (1.5–1.6).
6. **Devanagari test.** Type a Hindi string at every step: `पते का प्रमाण अपलोड करें`. Devanagari has taller ascenders and descenders than Latin. Note every step where your line height clips or crowds it.

**Worked example**

> Base 17px, ratio 1.25, rounded.
>
> | Step | Size | Line height | Use |
> |---|---|---|---|
> | body-sm | 14px | 1.5 (21px) | Hint text, field help |
> | body | 17px | 1.55 (26px) | All form labels and paragraph text |
> | h3 | 21px | 1.4 (29px) | Section headings inside a form |
> | h2 | 27px | 1.3 (35px) | Screen title |
> | h1 | 33px | 1.2 (40px) | Not used in this flow. Kept for the landing page. |
>
> **Devanagari test.** At body-sm 14px/21px the matras clip against the line above. Raised body-sm line height to 1.65 (23px) for Devanagari. Documented as a mode, not a global change.

**Done when**
- [ ] Base size stated with a reason tied to this specific audience
- [ ] Ratio stated with a reason
- [ ] Every step has a whole-pixel size, a line height, and a named use
- [ ] Any step with no use has been deleted
- [ ] Devanagari tested at every step, with what broke and what you changed
- [ ] Figma link included, with the scale built as text styles

→ `students/UX{n}/week1/C1-1-type-scale.md`

### C1.2 — Build a spacing scale

**Learn first:** Refactoring UI ch. 1, on starting with too much white space.

**Method**
1. Pick a base unit. 4px or 8px. 8px means fewer decisions; 4px gives finer control in dense UI.
2. Build the steps. Do not make them linear — `4, 8, 12, 16, 24, 32, 48, 64` is more useful than `4, 8, 12, 16, 20, 24, 28`, because adjacent steps need to be visibly different.
3. For three of the steps, name a specific place *in this flow* where that step is correct.

**Worked example**

> Base 4px. Steps: 4, 8, 12, 16, 24, 32, 48, 64.
>
> - **8px** — gap between a field label and its input. Small enough that they read as one unit (Gestalt proximity).
> - **24px** — gap between two form fields. Large enough that they do not read as one group, small enough to stay in one visual block.
> - **48px** — space above the primary action button. Separates "entering information" from "committing", which is a different kind of decision.

**Done when**
- [ ] Base unit stated with a reason
- [ ] Full step list, non-linear at the top end
- [ ] Three steps each mapped to a real place in this flow, with the reason

→ `students/UX{n}/week1/C1-2-spacing-scale.md`

### C1.3 — Measure test

**Learn first:** Practical Typography on line length. The rule of thumb is 45–90 characters per line, with 60–70 being comfortable.

**Method**
1. Take one real paragraph from the service — the document requirements text works well.
2. Set it three times at your `body` size, at three different widths: too narrow (about 30 characters), comfortable (about 65), too wide (about 110).
3. Screenshot all three.
4. Read each one out loud and note what your eye does. Narrow forces too many return sweeps. Wide makes you lose your place on the return.
5. State which is right, in terms of characters per line and reading behaviour. Not "it looks better".

**Done when**
- [ ] Three screenshots at three stated widths
- [ ] Character count per line stated for each
- [ ] Your choice justified by reading behaviour, with the source named
- [ ] The chosen max width recorded as a number you will use for the rest of the sprint

→ `students/UX{n}/week1/C1-3-measure-test.md`

---

# Thursday

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **Refactoring UI** | Ch. 4, the colour chapter: define your palette up front, don't let lightness kill saturation, greys don't have to be grey | 40 min |
| **Leonardo** | leonardocolor.io — read the intro, then build one ramp and watch the contrast numbers update | 25 min |
| **WCAG 1.4.1** | "Use of Color" — the criterion and the failure examples | 15 min |
| **Material 3** | The colour roles page. Look at how they name roles rather than colours. | 10 min |

**What you need out of this:** you need more greys than you think, roughly nine. You need fewer accent colours than you think. And a colour must be chosen for a role — "error text" — not for a hue.

→ **Commit** `day4-learning.md`

## DO — 2 hours (plus critique)

### C2.1 — Build the colour system

**Learn first:** Refactoring UI ch. 4. Leonardo for generating the ramps.

**Method**
1. **Neutral ramp, 10 steps.** From near-white to near-black. Use Leonardo so the steps are perceptually even rather than mathematically even. Give them numbers: 50, 100, 200 … 900.
2. **Primary ramp.** One brand colour, 10 steps, same method. A government service usually inherits this; if so, state the source.
3. **Semantic colours.** Success, warning, error, information. Each needs at least a text version and a surface version, because error text on white and an error background need different lightness.
4. **Contrast every step.** For every colour, record its ratio against white and against your darkest neutral. Mark which pass 4.5:1 and which pass 3:1.
5. **Do not skip step 4.** The whole point of doing this now is that in week 2 you can pick a colour without checking anything.

**Worked example** — three rows of a neutral ramp:

| Token | Hex | vs white | vs neutral-900 | Passes |
|---|---|---|---|---|
| neutral-500 | #6B7280 | 4.83:1 | 3.11:1 | AA body text on white ✓ |
| neutral-400 | #9CA3AF | 2.85:1 | 5.27:1 | ✗ body on white · ✓ large text only |
| neutral-200 | #E5E7EB | 1.22:1 | 12.3:1 | Borders and surfaces only. Never text. |

**Done when**
- [ ] 10-step neutral ramp, perceptually even, with a stated generation method
- [ ] Primary ramp, with its source stated if inherited
- [ ] Four semantic colours, each with a text and a surface value
- [ ] Every single step has both contrast ratios recorded
- [ ] Each step is marked with what it may be used for

→ `students/UX{n}/week1/C2-1-colour-system.md`

### C2.2 — Map colours to roles

**Learn first:** the Material 3 colour roles page from this morning.

**Method**
1. Fill in every role below with a token from C2.1, never a raw hex.
2. Roles: page background · surface · surface raised · border default · border strong · text primary · text secondary · text disabled · interactive default · interactive hover · interactive pressed · interactive disabled · focus ring · error text · error surface · error border · success text · success surface
3. For every text role, confirm the contrast against the background role it sits on.
4. If a role has no token that works, say so. That is a finding, not a failure.

**Why this matters:** this mapping is what becomes your token file in S1.3, and what makes dark mode possible in week 4 without redesigning anything.

**Done when**
- [ ] Every role has a token, not a hex
- [ ] Every text role has its contrast against its own background confirmed
- [ ] Focus ring is included and passes 3:1 against both the component and the background
- [ ] Any role you could not fill is named as a gap

→ `students/UX{n}/week1/C2-2-semantic-roles.md`

### Thursday critique — 90 minutes

Present for 12 minutes: your problem statement, your three worst audit findings, and your type and colour scales. Run against `07-critique-guide.md`.

The critique lead files the log the same day.

---

# Friday

## LEARN — 60 minutes

| Source | What exactly | Time |
|---|---|---|
| **Refactoring UI** | Ch. 5 "Layout and Spacing" and Ch. 6 "Designing Text" | 40 min |
| **Refactoring UI** | The greyscale section — designing without colour first | 20 min |

→ **Commit** `day5-learning.md`

## DO — 2 hours

### C1.4 — Greyscale hierarchy

**Learn first:** the greyscale section you just read.

**Method**
1. Pick the busiest screen from your screenshots. The address entry screen is the right choice.
2. Rebuild it in Figma using only your type scale, your spacing scale, and your neutral ramp. No primary colour. No semantic colour. Nothing.
3. Every difference in importance must come from size, weight, or grey value.
4. Now squint at it, or blur it in Figma. The three most important things should still be the three things you notice.
5. Compare with the live screen next to it.

**Why:** if hierarchy only works once colour arrives, the hierarchy is not real. Colour is the last 10 percent, not the structure.

**Done when**
- [ ] One screen fully rebuilt, greyscale only
- [ ] Uses only tokens from C1.1, C1.2, C2.1
- [ ] Blurred version included, and the three most prominent things are the intended three
- [ ] Side by side with the original
- [ ] Figma link

→ `students/UX{n}/week1/C1-4-greyscale-hierarchy.md`

### P1.3 — Constraint list

**Method**
1. List every constraint stated in `01-project-brief.md`.
2. Add at least three you found yourself while using the live service on Tuesday.
3. Mark each as: **fixed policy** (a rule you cannot change) · **technical** (current implementation, could change with effort) · **assumed** (nobody has actually verified it).
4. The assumed ones are the ones worth attacking in week 2.

**Worked example**

| Constraint | Type | Note |
|---|---|---|
| OTP goes only to the registered mobile | Fixed policy | Identity requirement. Cannot be designed away. Can be explained better. |
| Upload limit is 2MB | Technical | Changeable server-side. Worth asking, because phone photos are 4MB. |
| Address must be entered in 9 separate fields | **Assumed** | No policy requires 9 fields. This is how it was built. Attack this. |

**Done when**
- [ ] Every brief constraint listed
- [ ] At least three you found yourself
- [ ] Each classified as policy, technical, or assumed
- [ ] At least two marked assumed, with a note on how you would verify

→ `students/UX{n}/week1/P1-3-constraints.md`

### P1.4 — Metrics

**Method**
1. **Primary metric.** The one number the department would use to decide this worked. State how it is measured.
2. **Two input metrics.** Things that move before the primary metric does, so you find out sooner.
3. **One guardrail metric.** The thing that must not get worse while you improve the primary one.
4. For the guardrail, write one sentence describing the bad design you would produce if only the primary metric mattered.

**Worked example** — for a different service, appointment booking:

> **Primary:** online completion rate. Sessions that reach confirmation ÷ sessions that start. Measured weekly.
> **Input 1:** document upload success on first attempt.
> **Input 2:** median time on the address entry step.
> **Guardrail:** rejection rate of submitted requests.
> **If only the primary mattered:** I would remove all validation and all document guidance so that everyone reaches the confirmation screen. Completion would look excellent, and rejections two weeks later would rise, which moves the counter visit later instead of removing it.

**Done when**
- [ ] Primary metric with its measurement method
- [ ] Two input metrics that genuinely move earlier
- [ ] One guardrail
- [ ] The "if only the primary mattered" sentence describes a specific bad design, not a vague risk

→ `students/UX{n}/week1/P1-4-metrics.md`

---

# Saturday

## S1 — The shared system, cohort session, 90 minutes

Five designers have now built five type scales, five spacing scales, and five colour systems. The shared system needs one of each.

### S1.1 — Agree token naming
Write the convention with three correct examples and three incorrect ones, each with the reason.
→ `system/docs/token-naming.md`, written by this week's system owner

### S1.2 — Pick the foundations
Choose one type scale, one spacing scale, one colour system. Or synthesise. Record what was rejected and why.

**This decision cannot be reopened after week 2 without a written decision record.**
→ `system/docs/foundations-decision.md`

### S1.3 — Write the tokens
The agreed foundations as JSON, in two layers: primitive (raw values) and semantic (roles).
→ `system/tokens/primitive.json`, `system/tokens/semantic.json`

### S1.4 — Shared Figma library
Set up the library with the agreed variables. Light mode only this week. Post the link.
→ `system/docs/README.md`

## F1 — Fundamentals, 90 minutes

**F1.1 — Why session: Gestalt principles.** One designer presents. Every principle must be illustrated with a screenshot from the live Aadhaar flow, not a textbook diagram. Proximity, similarity, common region, continuity, closure, figure-ground.
→ `fundamentals/why-sessions/week01-gestalt.md`

**F1.2 — Teardown: IRCTC ticket booking.** Use the five-part format from root `02-Learning-Path.md`.
→ `fundamentals/teardowns/01-irctc.md`

**F1.3 — Drill, daily from today.** Ten minutes. Rebuild one component from any real Indian product from memory, then compare. One line in the log.
→ `fundamentals/drills/UX{n}-log.md`

---

## Friday checklist

- [ ] 5 learning summaries: `day1` to `day5`
- [ ] P1.1, P1.2, P1.3, P1.4
- [ ] R1.1, R1.2, R1.3
- [ ] C1.1, C1.2, C1.3, C1.4
- [ ] C2.1, C2.2
- [ ] Two peer reviews given, each with one substantive comment
- [ ] Critique attended, log filed if you were lead
- [ ] Saturday: S1 session done, teardown committed, drill log started

**If you are short on time, cut in this order:** C1.3, then C1.4. Never cut R1.2, R1.3, or the learning summaries. Craft can be polished later. Audit findings and understanding cannot be retrofitted.

Next: `03-week2.md`
