# Sprint 1, Week 3: Test and fix

**UX2 | Position this week: builder | Theme: your opinion stops mattering this week**

Three people use your flow. What they do replaces what you assumed. Something will surprise you, and the surprise is the deliverable.

The core admin delivers an injected change on Monday. Handle it.

---

## Research and Evidence `[MILESTONE]`

**R2.1** Test plan: three tasks, success criteria for each, and what you expect to go wrong. Write the prediction before you test. That is the point.
→ `R2-1-test-plan.md`

**R2.2** Moderator script. Every question non leading. Include the two questions you almost wrote in a leading form and the corrected version of each.
→ `R2-2-script.md`

**R2.3** Run the test with three participants on your own prototype. At least one must be over 50 or slow in English. Record task success, time, and hesitation points.
→ `R2-3-test-results.md`

**R2.4** Severity rate every issue: 1 cosmetic, 2 minor, 3 major, 4 catastrophic. Justify every 3 and 4 with the user cost.
→ `R2-4-severity.md`

**R2.5** What surprised you. Something must have. If nothing did, say whether the prototype was too simple or the tasks were too easy.
→ `R2-5-surprises.md`

## Craft and Interface

**C5.1** Every screen, every state. Use the states table in `../../../docs/accessibility-gate.md` section 2. Commit as a matrix: rows are screens, columns are states, cells link to the frame or say not applicable with the reason.
→ `C5-1-states-matrix.md` plus Figma link

**C5.2** Loading state for document upload on 3G. What the user sees at 0, 3, 15, and 45 seconds. State which of those needs a different design and why.
→ `C5-2-loading-timeline.md`

**C5.3** Session expiry. Priya's rental agreement takes 8 minutes to find. Design what happens to her typed data. State where it is stored and what you promise the user.
→ `C5-3-session-expiry.md`

**C5.4** Rejection state. Rejected 12 days later with a reason code. Design the screen that turns that code into an action, including whether the ₹50 must be paid again and how you say so.
→ `C5-4-rejection.md`

## Systems and Technical

**S3.1** Fix your top three severity issues from R2.4. Before and after for each, with the test finding quoted as the reason.
→ `S3-1-fixes.md`

**S3.2** One issue you are not fixing. Why: out of scope, low severity, or the fix costs more than the problem. Defend it in writing.
→ `S3-2-wont-fix.md`

**S3.3** If a fix required a system change, open a system pull request rather than overriding locally. If you overrode locally, write one line on why the system could not absorb it.
→ `system/components/{component}.md` update, or `S3-3-override-note.md`

## The injected change

Delivered Monday by the core admin. It will be inconvenient. That is the point.

**X1.1** Post mortem. What changed, what it broke, what you did, how much time it cost, and what earlier decision would have made it cheaper.
→ `X1-1-postmortem.md`

## Spine

**F3.1** Why session, Saturday. This week's presenter: **UX3**. Cognitive load and progressive disclosure, using the cohort's own address entry screens as material.
→ `fundamentals/why-sessions/week03-cognitive-load.md`

**F3.2** Teardown: any insurance claim submission flow.
→ `fundamentals/teardowns/03-insurance-claim.md`

**F3.3** Whiteboard why, Wednesday. 15 minutes, no notes, no file open. Draw your flow from memory, answer three questions drawn at random. Admin logs the result.

## Done when

- Three participants tested, results recorded with quotes not paraphrase
- Every issue severity rated, every 3 and 4 justified with the user cost
- States matrix complete with no unexplained gaps
- Top three fixes committed with the finding quoted
- Post mortem committed
- Whiteboard why attempted, pass or re-run scheduled

## Watch for

Three ways week 3 goes wrong:

1. **Testing with people who want you to succeed.** A friend who says "that was clear" while hesitating for nine seconds has given you data you are ignoring. Record hesitation, not opinions.
2. **Leading the participant.** "Was that easy to find?" contaminates the answer. "Tell me what you were looking for" does not. R2.2 exists because this is the hardest research skill.
3. **Fixing everything.** Three fixes and one documented refusal is the assignment. A designer who fixes all nine findings has not prioritised, they have just complied.

## Reading this week

- Rocket Surgery Made Easy, the whole thing, it is short
- Interviewing Users, the chapters on question framing
- NNGroup on severity ratings for usability problems
