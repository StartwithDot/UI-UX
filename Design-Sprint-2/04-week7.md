# Week 7 — Test

**Sprint 2 · Week 7 of 8 · Theme: usability testing with no budget, and the mid-sprint failure**

---

## By the end of this week you can

- Run a moderated usability study on five people
- Write tasks that test the design rather than your instructions
- Rate findings by severity and defend the rating
- Absorb a constraint change without abandoning your evidence

## The week at a glance

| Step | LEARN | DO |
|---|---|---|
| **1** | Rocket Surgery ch. 1–4 · Don't Make Me Think, testing chapter | R5.1 R5.2 — test plan, prototype to test |
| **2** | Rocket Surgery ch. 5–6 | R5.3 — sessions 1 and 2 |
| **3** | NNGroup severity ratings · Krug on fixing | R5.4 — sessions 3, 4, 5 |
| **4** | Your own findings, read cold | R5.5 R5.6 — findings, severity, fix list · **critique** · **whiteboard why** |
| **5** | (failure injection lands) | X2 P7.1 — post mortem, revised plan |
| **6** | — | S8 system · F7 why session and teardown |

---

# the start of the week

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **Rocket Surgery Made Easy**, Krug | Ch. 1–4 | 45 min |
| **Don't Make Me Think** | The usability testing chapter | 25 min |
| **NNGroup** | "Why You Only Need to Test with 5 Users" and then "Why You Only Need to Test with 5 Users: Revisited" | 20 min |

**Read both NNGroup articles.** The second one qualifies the first, and knowing the qualification is what lets you survive the sample-size question in the defense. Five users find most problems *in one flow, for one user group, in formative testing*. Five users cannot give you a completion rate.

→ **Commit** `students/UX{n}/week7/session1-learning.md`

## DO — 2 hours

### R5.1 — Test plan

**Method**
1. **What are you testing?** One sentence. If it is "the design", you are not testing anything specific.
2. **Three tasks.** Goals with no route. Ordered so an early failure does not block a later task.
3. **Success criteria per task.** Define, before you run it, what counts as completing it. Otherwise you will decide afterwards, in your own favour.
4. **What you will measure.** Completion, where they hesitate, what they say, how long. Note that with five participants, time is directional and not a statistic.
5. **What you will say and not say.** Your no-help rule, written down, with the number of seconds.
6. **Consent**, same standard as week 5.

**Worked example** — task plus success criterion:

> **Task 2:** "Your family's income certificate is at home with your father. You want to finish as much of this application as you can now. Do that."
> **Success:** The participant either saves and exits with a stated understanding of how to return, or finds and uses a partial-save mechanism, without asking me what to do.
> **Why this task:** 4 of 5 interview participants stalled at exactly this point. This task tests whether the design solves the thing I actually found, rather than the thing the brief assumed.

**Done when**
- [ ] What you are testing, in one specific sentence
- [ ] Three tasks, goals not routes, sensibly ordered
- [ ] Success criteria written before running anything
- [ ] Measures stated, with their limits acknowledged
- [ ] No-help rule written with a number of seconds
- [ ] At least one task traces directly to a week 6 finding

→ `students/UX{n}/week7/R5-1-test-plan.md`

### R5.2 — Build what you will test

**Method**
1. You need something testable. A clickable Figma prototype of the current service's flow, or your own redesign of the two or three screens your findings point at.
2. Make the paths in your three tasks actually work, including the failure paths. A prototype where only the happy path clicks tests nothing about recovery.
3. Keep fidelity low enough that people comment on the flow and not on the colours. Mid fidelity, using your system.
4. Test the prototype yourself first, on a phone, following your own tasks. Every dead end you find now is a wasted session you did not have.

**Done when**
- [ ] All three tasks completable in the prototype
- [ ] Failure paths clickable
- [ ] You have run it yourself on a phone and fixed the dead ends
- [ ] Mid fidelity, using system components
- [ ] Figma link

→ `students/UX{n}/week7/R5-2-test-prototype.md`

---

# early in the week

## LEARN — 45 minutes

| Source | What exactly | Time |
|---|---|---|
| **Rocket Surgery Made Easy** | Ch. 5–6, on running the session and taking notes | 30 min |
| **Your R4.2** | Your own interview self-critique. The same mistakes appear in usability testing. | 15 min |

→ **Commit** `session2-learning.md`

## DO — 3 hours

### R5.3 — Sessions 1 and 2

**Method**
1. Consent, then run.
2. Notes in four columns: what they did · what they said · where they hesitated · where they failed.
3. **Do not help for the number of seconds you wrote down.** When you do help, log it as a help event, because a task completed with help is not a completed task.
4. No interpretation in session notes.
5. Do not change the prototype between sessions.

**Done when**
- [ ] Two sessions, consented, recorded
- [ ] Four-column notes
- [ ] Every help event logged with when and what you said
- [ ] Zero interpretation
- [ ] Prototype unchanged

→ `students/UX{n}/week7/R5-3-sessions-1-2.md`

---

# mid week

## LEARN — 45 minutes

| Source | What exactly | Time |
|---|---|---|
| **NNGroup** | "Severity Ratings for Usability Problems" | 20 min |
| **Rocket Surgery** | Ch. 7, on deciding what to fix | 25 min |

→ **Commit** `session3-learning.md`

## DO — 3 hours

### R5.4 — Sessions 3, 4, 5
Same protocol. Prototype still unchanged.

By session 4 you will be able to predict what happens next. That prediction is a finding — write down what you expected before each remaining session, and whether you were right. Being consistently right is evidence that the pattern is real.

→ `students/UX{n}/week7/R5-4-sessions-3-4-5.md`

---

# late in the week

## LEARN — 45 minutes

Read all five sets of session notes cold, in one sitting, without your interpretation from during the sessions.

Write three lines: what all five did the same, what only one did, and which of your week 6 interview findings the testing contradicted.

→ **Commit** `session4-learning.md`

## DO — 2 hours (plus critique and whiteboard why)

### R5.5 — Findings with severity

**Method**
1. One row per issue: what happened · n out of 5 · severity 1–4 · what it cost the user · your interpretation · confidence.
2. Severity: 1 cosmetic · 2 minor, worked around · 3 major, task failed · 4 catastrophic, data or money lost.
3. Confidence: high if 4 or 5 of 5 and consistent with interviews · medium if 3 of 5 or if interviews and testing disagree · low if 1 or 2 of 5.
4. **Include the findings that disagree with your week 6 hypothesis.** Especially those.

**Done when**
- [ ] Every issue across all five sessions
- [ ] Denominators throughout
- [ ] Severity and confidence both assigned, with reasons
- [ ] Observation separated from interpretation
- [ ] At least one finding that contradicts your own earlier belief

→ `students/UX{n}/week7/R5-5-findings.md`

### R5.6 — Fix list

**Method**
1. Every severity 3 and 4 gets a proposed fix.
2. For each fix: what changes, what it costs to build (your estimate is fine), and what gets worse.
3. Rank by severity × confidence ÷ cost. Not by what you find interesting.
4. Say what you are **not** fixing, and why. A fix list with nothing deferred is not a prioritised list.

**Done when**
- [ ] Every sev 3 and 4 has a fix or a stated deferral
- [ ] Each fix names what gets worse
- [ ] Ranked, with the ranking method shown
- [ ] Deferrals justified

→ `students/UX{n}/week7/R5-6-fix-list.md`

### the week's critique — 90 minutes
Present three findings with their confidence levels. The critique focus: **is the confidence level honest, or is the finding you like most given more confidence than its denominator supports?**

### Whiteboard why — 15 minutes
No notes. Draw your research plan from memory, state your three questions, and answer what five participants can and cannot support.

---

# the end of the week

## The failure injection lands

The admin delivers the change this study time. In this sprint it is likely to be something that invalidates part of your research, not just your design. That is deliberate, and it is the most common thing that happens to real research.

## DO — 2 hours

### X2 — Post mortem

**Method**
1. What changed, in one factual sentence.
2. What it invalidated. Be specific: which findings, which participants' relevance, which tasks.
3. What survives. This is the important half. Findings about how people think usually survive a change in requirements; findings about a specific screen usually do not.
4. What would have made this cheaper. Which earlier decision, made differently, would have absorbed this?
5. One concrete change to how you work.

**Worked example** — point 3, for a different injection:

> **What survives:** the finding that applicants do not know which income certificate is valid survives completely, because it is about their knowledge and not about the form's structure. The finding that they abandon at step 4 does not survive, because step 4 no longer exists in the same position. I can re-map the first finding onto the new flow in about 30 minutes. The second one has to be re-tested.

Being able to separate these two is the skill being tested.

**Done when**
- [ ] What changed, factually
- [ ] What was invalidated, named specifically
- [ ] What survives, with the reason it survives
- [ ] A named earlier decision that would have made this cheaper
- [ ] One concrete change to how you work

→ `students/UX{n}/week7/X2-post-mortem.md`

### P7.1 — Revised research position

**Method**
1. Restate your findings under the new constraint.
2. Mark each: still valid · needs re-testing · invalid.
3. Update your fix list.
4. State what you would do with two more days, and what you are giving up instead.

**Done when**
- [ ] Every finding classified into the three categories
- [ ] Fix list updated
- [ ] What you would do with more time, stated as a priority order
- [ ] What you are giving up, named

→ `students/UX{n}/week7/P7-1-revised-position.md`

---

# the cohort review

## S8 — System, 90 minutes

**S8.1** — Add the states your testing exposed. If participants got stuck somewhere the system has no component for, that is a system gap.
**S8.2** — Review one peer's contribution.
**S8.3** — Update `system/docs/debt.md` with anything this sprint has added to it.

## F7 — Fundamentals

**F7.1 — Why session: bias.** Confirmation bias, anchoring, the framing effect, and social desirability bias. Every one illustrated with something from the cohort's own interviews this fortnight.
→ `fundamentals/why-sessions/week07-bias.md`

**F7.2 — Teardown:** an insurance claim submission flow.
→ `fundamentals/teardowns/07-insurance-claim.md`

**F7.3 — Drill continues.**

---

## End of week checklist

- [ ] 5 learning summaries
- [ ] R5.1 through R5.6 — five sessions run
- [ ] X2 post mortem, P7.1 revised position
- [ ] Whiteboard why attempted
- [ ] Critique attended
- [ ] Everything anonymised

Next: `05-week8.md`
