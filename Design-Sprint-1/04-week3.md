# Week 3 — Test and Fix

**Sprint 1 · Week 3 of 4 · Theme: every state a screen can be in, and what real users do to your design**

This is the week something breaks. A constraint will change mid-week. You do not know which one yet.

---

## By the end of this week you can

- Produce a complete states matrix and design the states nobody remembers
- Run a moderated usability test on three people without leading them
- Trace every design change back to a specific finding
- Write a post mortem on a change you did not choose

## The week at a glance

| Step | LEARN | DO |
|---|---|---|
| **1** | Refactoring UI ch. 8 (empty states) · Material 3 + Polaris state guidance | C5.1 C5.2 — states matrix, empty and loading |
| **2** | Rocket Surgery Made Easy ch. 1–4 | R2.1 R2.2 — test script, recruit and run session 1 |
| **3** | Krug on observing without leading | R2.3 R2.4 — sessions 2 and 3, severity rating |
| **4** | Your own findings, re-read cold | C5.3 C6.1 — offline and error states, fixes · **critique** · **whiteboard why** |
| **5** | (failure injection lands) | X1 P3.1 — post mortem, revised decisions |
| **6** | — | S3 system update · F3 why session and teardown · **L-PR1** |

---

# Day 1

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **Refactoring UI** | Ch. 8, "Don't overlook empty states", and the "Supercharge the defaults" section | 25 min |
| **Material Design 3** | The "Loading" and "Progress indicators" guidance | 20 min |
| **Shopify Polaris** | The "Empty states" pattern page and the "Skeleton" component page | 25 min |
| **NNGroup** | "Progress Indicators" and "Response Times: The 3 Important Limits" | 20 min |

**What to take:** the three response-time limits are 0.1s (feels instant), 1s (thought stays uninterrupted), 10s (attention is lost). Which loading treatment you use is determined by which side of those numbers you are on, not by taste.

→ **Commit** `students/UX{n}/week3/session1-learning.md`

## DO — 2 hours

### C5.1 — States matrix

**Method**
1. Rows: every screen in your flow.
2. Columns: default · empty · loading · partial · error · success · offline · permission denied · zero results · first run · destructive confirm.
3. For every cell write one of: **N/A** with a reason · **exists** with a link to where you designed it · **missing**.
4. "N/A" needs a reason. "This screen cannot be empty" is only true if you can say why.
5. Count your missing cells. That number is the honest state of your design.

**Worked example** — two rows:

| Screen | default | empty | loading | offline | error |
|---|---|---|---|---|---|
| Address entry | ✅ C3.3 | N/A — form is always empty at first, which *is* the default | ❌ missing — PIN lookup takes 800ms | ❌ missing | ✅ C4.2 |
| Document upload | ✅ C3.4 | ✅ C3.4 state 1 | ✅ C3.4 progress | ❌ missing — what happens if the connection dies at 60% is designed, but not the state before that | ✅ C3.4 states 2, 3 |

**Done when**
- [ ] Every screen × every column filled
- [ ] Every N/A has a stated reason
- [ ] Missing cells counted, and the number written at the top of the file
- [ ] Every "exists" links to the file where it lives

→ `students/UX{n}/week3/C5-1-states-matrix.md`

### C5.2 — Empty and loading states

**Method**
1. Pick the two most consequential empty states and the two most consequential loading states from your matrix.
2. For empty states: an empty state must say what would be here, why it is not here, and what to do. "No data" is a failure.
3. For loading states: choose the treatment based on the expected duration, then state the duration and the source of that estimate.

| Expected duration | Treatment |
|---|---|
| Under 1s | Nothing. Do not flash a spinner. |
| 1–3s | Inline spinner or skeleton, keeping layout stable |
| 3–10s | Progress with a message about what is happening |
| Over 10s | Do not make them wait. Confirm receipt and notify later. |

**Worked example** — an empty state for a different service:

> **Screen:** Saved applications, when there are none.
> ❌ "No applications found."
> ✅ Heading: "You have no saved applications." Body: "Applications you start but do not submit are saved here for 30 days. You can come back and finish them." Action: "Start a new address update".
>
> It says what belongs here, why it is empty, how long things persist, and gives the next step.

**Done when**
- [ ] Two empty states, each saying what belongs there, why it is empty, and what to do
- [ ] Two loading states, each with a stated expected duration and where that estimate came from
- [ ] The treatment matches the duration band
- [ ] Layout does not shift when content arrives

→ `students/UX{n}/week3/C5-2-empty-loading.md`

---

# Day 2

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **Rocket Surgery Made Easy**, Krug | Ch. 1–4. It is short and directly operational. | 50 min |
| **Don't Make Me Think** | The usability testing chapter | 20 min |
| **NNGroup** | "Thinking Aloud: The #1 Usability Tool" | 20 min |

**What to take:** three users find most of what five find. Your job in the session is to shut up. The most useful thing you can say is "what are you trying to do?" and the most damaging is "did you see the button up there?"

→ **Commit** `session2-learning.md`

## DO — 2 hours

### R2.1 — Write the test script

**Learn first:** Krug ch. 2–3 on writing tasks.

**Method**
1. Write three tasks. A task states a goal, never a route.
   - ❌ "Click on Update Address, then upload your electricity bill."
   - ✅ "You have moved to a new house. Update the address on your Aadhaar using this phone."
2. Write your probe questions. Allowed: "what are you trying to do?", "what do you expect to happen?", "what does that mean to you?". Not allowed: anything containing the name of a button.
3. Write the consent script: what you are recording, what you will do with it, that they can stop at any time, and that you are testing the design and not them.
4. Write your own rules for the session: do not help for the first 60 seconds of any struggle, do not explain, do not defend.

**Done when**
- [ ] Three tasks, each stating a goal with no route
- [ ] Probe questions written down, and none names a UI element
- [ ] Consent script written
- [ ] Your own no-help rule written down before you start

→ `students/UX{n}/week3/R2-1-test-script.md`

### R2.2 — Session 1

**Method**
1. Recruit three people who are **not designers**. A neighbour, a shopkeeper, a relative over 50. The closer to the brief's users, the more you learn.
2. Run the session. Screen recording plus audio, with consent.
3. Take notes in this format only: **what they did · what they said · where they hesitated · what they expected**.
4. Do not write your interpretation in the session notes. Interpretation comes in R2.4, deliberately separated.

**Done when**
- [ ] One session run and recorded
- [ ] Notes in the four-column format
- [ ] Zero interpretation in the notes
- [ ] Every point where you broke your own no-help rule is recorded honestly

→ `students/UX{n}/week3/R2-2-session1.md`

---

# Day 3

## LEARN — 60 minutes

| Source | What exactly | Time |
|---|---|---|
| **Rocket Surgery Made Easy** | Ch. 5–7, on what to do with what you found | 30 min |
| **NNGroup** | "Severity Ratings for Usability Problems" | 20 min |
| **Your own R2.2 notes** | Re-read them cold, before running session 2 | 10 min |

→ **Commit** `session3-learning.md`

## DO — 2 hours

### R2.3 — Sessions 2 and 3
Same protocol as R2.2. Do not change your prototype between sessions. Changing mid-study means you tested two different things and can compare neither.

If something is obviously catastrophic, note it and keep going. You fix it late in the week.

→ `students/UX{n}/week3/R2-3-sessions-2-3.md`

### R2.4 — Findings and severity

**Learn first:** the NNGroup severity ratings article from today's LEARN block.

**Method**
1. Now you interpret. One row per issue.
2. Columns: what happened · how many of the 3 hit it · severity 1–4 · your interpretation of why · what you will change.
3. Separate what you **observed** from what you **think it means**. Keep them in different columns so a reader can disagree with your interpretation while accepting your observation.
4. If all three participants did the same unexpected thing, that is not three data points, it is one strong signal about your design.

**Worked example**

| Observed | n | Sev | Why I think it happened | Change |
|---|---|---|---|---|
| All 3 tapped the PIN field first, before house number | 3/3 | 2 | PIN is the field people know by heart, so it is the lowest-effort starting point. My field order assumes top-to-bottom entry. | Reorder so PIN is first, then auto-fill state and district from it. This also removes two fields. |
| 2 of 3 uploaded a photo and did not notice it was blurred until rejection | 2/3 | 3 | No feedback on legibility at upload time. The system knows, the user does not. | Add a legibility check at upload with a preview and a "retake" option. |

**Done when**
- [ ] Every issue from all three sessions is listed
- [ ] Observation and interpretation are in separate columns
- [ ] Severity assigned with the consequence implied
- [ ] Every severity 3 or 4 has a stated change

→ `students/UX{n}/week3/R2-4-findings.md`

---

# Day 4

## LEARN — 45 minutes

Re-read your own R1.2 heuristic audit from week 1 next to your R2.4 findings from this week.

Answer in writing, three lines: which of your week 1 heuristic findings did real users actually hit? Which did they never notice? What does that tell you about the limits of heuristic evaluation?

→ **Commit** `session4-learning.md` — this one is short and it matters. Heuristic evaluation finds things testing misses, and testing finds things heuristics miss. Knowing which is which is a real skill.

## DO — 2 hours (plus critique and whiteboard why)

### C5.3 — Offline and interruption states

Ramesh's connection drops. This is not an edge case in this brief; it is the normal case.

**Method**
Design these five, all of them:
1. **Offline before starting** — no connection at all
2. **Connection lost mid-form**, with data typed — what happens to what he typed
3. **Connection lost mid-upload** — what happens to the partial file
4. **Connection lost after submit, before confirmation** — the worst one. Did it go through or not? He paid ₹50.
5. **Reconnected** — how he gets back to where he was

For state 4, you must state what the system does: is submission idempotent, is there a request ID, does he risk paying twice? If you do not know, write the question you would ask an engineer. That is a valid answer. Guessing is not.

**Done when**
- [ ] All five designed
- [ ] State 2 says explicitly whether typed data survives, and how
- [ ] State 4 answers the double-payment risk, or states the exact question you would ask
- [ ] Nothing in these states is a generic "connection error"

→ `students/UX{n}/week3/C5-3-offline-states.md`

### C6.1 — Fix what testing found

**Method**
1. Take every severity 3 and 4 finding from R2.4.
2. Redesign for each one.
3. For each change, write: which finding it addresses, what changed, and what got worse. **Something always gets worse.** If nothing did, you have not changed anything meaningful.
4. If you chose not to fix a severity 3, say why. "Fixed cheaply enough elsewhere" and "the cost outweighs the benefit at this frequency" are valid. "Ran out of time" is also valid, if honest.

**Done when**
- [ ] Every sev 3 and 4 either fixed or explicitly deferred with a reason
- [ ] Each change traces to a specific finding by its row
- [ ] Each change names what got worse
- [ ] Before and after screens

→ `students/UX{n}/week3/C6-1-fixes.md`

### Critique — 90 minutes
Present your findings and your fixes. The strongest thing you can present is a finding that contradicted something you were confident about in week 2.

### Whiteboard why — 15 minutes, with the admin
No notes. No files open. Draw your flow from memory and answer three questions drawn from the sprint question bank. "Needs work" is a normal outcome and schedules a re-run next week.

---

# Day 5

## The failure injection lands

The admin delivers a constraint change during this morning's LEARN block. You do not know in advance which one. It is real, it is not negotiable, and it invalidates part of what you built.

## DO — 2 hours

### X1 — Post mortem

**Method**
1. **What changed.** State it in one sentence, factually.
2. **What it broke.** Name every screen, decision, and file affected. Be specific.
3. **What it cost.** Hours to fix, and what you now cannot finish because of it.
4. **What would have made this cheaper.** The real question. Which earlier decision, if made differently, would have absorbed this change instead of being broken by it?
5. **What you are changing in how you work.** One concrete thing, not a resolution to "be more flexible".

**Worked example** — the shape of point 4, for a different injection:

> If I had built the address entry as a component with the field list driven by a config array instead of nine hard-placed fields, adding the two new mandatory fields would have been a 10-minute change instead of redrawing four screens. I hard-placed them because it was faster on early in the week. It cost me four hours on the end of the week.

That is the answer the defense is looking for: a named earlier decision, the reason it was made, and the price it charged.

**Done when**
- [ ] What changed, in one factual sentence
- [ ] Everything it broke, named specifically
- [ ] A real cost in hours and in dropped scope
- [ ] Point 4 names a specific earlier decision, not a general lesson
- [ ] Point 5 is one concrete change to how you work

→ `students/UX{n}/week3/X1-post-mortem.md`

### P3.1 — Revised decisions

**Method**
1. List every decision from weeks 1 and 2 that the injection has invalidated.
2. For each: what it was, why it no longer holds, and what replaces it.
3. Update the affected screens.
4. Do not quietly change things. The record of what you decided and why has to stay readable.

**Done when**
- [ ] Every invalidated decision listed
- [ ] Each has its replacement and the reason
- [ ] Affected screens updated
- [ ] Old decisions marked superseded, not deleted

→ `students/UX{n}/week3/P3-1-revised-decisions.md`

---

# Day 6 — Cohort day

## S3 — System update, 90 minutes

### S3.1 — Add the states to the components
Every component in `system/` needs the states you learned about this week: loading, disabled, error, and focus if it is missing. Same component you own from week 2.
→ update `system/components/{component}.md`

### S3.2 — Write the component contribution rule
The system owner writes what a contribution must include before it can be merged. It has to be specific enough to reject something with.
→ `system/docs/contribution-rules.md`

### S3.3 — Handle the injection at system level
If the injection affected the shared system, the cohort decides together how to absorb it. Record the decision.
→ `system/docs/decisions/{nn}-{topic}.md`

## F3 — Fundamentals

**F3.1 — Why session: cognitive load and progressive disclosure.** The presenter must use one screen from the cohort's own work that has too much on it, and reduce it live.
→ `fundamentals/why-sessions/week03-cognitive-load.md`

**F3.2 — Teardown:** a hospital appointment booking flow.
→ `fundamentals/teardowns/03-hospital-booking.md`

**F3.3 — Drill continues.**

## Lab L-PR1 — Responsive behaviour and platform conventions, 2 hours

Full method and done-when checklist: `08-Prototyping-And-Responsive.md` (repository root), section L-PR1.

→ `students/UX{n}/week3/L-PR1-responsive.md`

---

## End of week checklist

- [ ] 5 learning summaries
- [ ] C5.1, C5.2, C5.3
- [ ] R2.1, R2.2, R2.3, R2.4
- [ ] C6.1
- [ ] X1 post mortem, P3.1 revised decisions
- [ ] Whiteboard why attempted
- [ ] Critique attended
- [ ] L-PR1 done (2 hours)

**Do not cut R2.2, R2.3, or R2.4.** Three real users is the entire evidence base for your defense next week. Without it you have opinions.

Next: `05-week4.md`
