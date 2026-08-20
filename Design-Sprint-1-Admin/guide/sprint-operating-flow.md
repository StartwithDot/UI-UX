# Sprint 1 Operating Flow

Week by week, what the admin does. Times are the actual load, not the ideal.

---

## Before week 1

| Task | Detail |
|---|---|
| Repos created | `Design-Sprint-1` public, `Design-Sprint-1-Admin` private |
| Branch protection | main requires one approval, no force push, **squash merge disabled** |
| Figma team created | Three files, library published, everyone invited as editor |
| Designer codes assigned | UX1 to UX5, fixed for 24 weeks, recorded in the ledger |
| Rotation filled | `docs/rotation-log.md`, all four weeks assigned before week 1 |
| Injection sealed | `failure-injections/sprint1.md`, not opened |
| Guest critic booked | For week 4 defense day |

Squash merge being disabled is not a preference. Squashing erases individual authorship in the shared zones, which is exactly what the program uses to show contribution.

## Week 1: Frame

**the start of the week kickoff, 15 minutes.** Say only this:

> "Nobody designs anything this week. You audit what exists and you build the foundations. On late in the week we choose one type scale, one spacing scale, and one colour system out of the five each of you will bring, and four of you will lose that argument. That is the exercise."

Telling them in advance that four will lose changes how they present. It also prevents the late in the week session becoming personal.

**mid week.** Read the heuristic audits. The tell for a weak audit is findings phrased as taste. Comment on the two weakest with the same question: "what does this cost the user".

**late in the week.** Critique, then the foundations session. Run the foundations session yourself, do not delegate it in week 1.

How to run it: each designer presents their scale in 3 minutes. No discussion during presentations. Then one question to the room: "which of these survives Devanagari at every step". That question usually decides it, because most will not have tested it, and the one who did wins on evidence rather than taste. Record what was rejected and why in `system/docs/foundations-decision.md`.

**the end of the week.** Approve the token JSON. Check one thing specifically: does any semantic token reference a hex value directly instead of a primitive. If yes, send it back. That single check teaches the layering better than a lecture.

**The week 1 failure to expect.** Designers who open Figma at the start of the week and start drawing screens. Catch it early in the week, not late in the week. The response is not "stop", it is "show me your problem statement first".

## Week 2: Build

**the start of the week.** Assign components. Give the hardest one, file upload, to whoever produced the strongest week 1 audit, because they will find the real states. Assign select to whoever is weakest technically, because the native versus custom question forces them into accessibility.

**mid week.** Read the error inventories. Anyone with fewer than 15 has not looked at the service. Anyone whose messages start with "Oops" or "Something went wrong" gets one comment: "what does this tell Ramesh to do".

**the week's critique.** Watch for the cohort agreeing with each other. Week 2 is when politeness sets in. If two sessions pass with no disagreement, name it: "nobody has disagreed with anybody in ninety minutes, which means either you all made the same choices or nobody is saying what they think".

**the end of the week.** Run the states gate on one designer's upload screen, chosen at random, in front of everyone. Not to embarrass, to calibrate. The first time the gate is applied publicly is what makes it real for the rest of the sprint.

**The week 2 failure to expect.** Happy path only, states deferred. This is the most common failure in the entire program. Every designer does it once. The injection in week 3 punishes it, which is why the injection is where it is.

## Week 3: Test, fix, and the injection

**the start of the week, 10:00.** Deliver the injection. Verbatim from `failure-injections/sprint1.md`. Then go quiet.

**the start of the week to mid week.** Answer only what a department would answer. Track two things: who asks about the refund, and what each person cuts.

**mid week.** Whiteboard why, 15 minutes each. No file open, no notes. They draw their flow from memory and answer three questions drawn at random.

The value is not the drawing. It is watching whether they can reconstruct their own reasoning without their artefacts. A designer who cannot draw their own flow from memory has been decorating, not deciding.

**the week's critique.** Test results, not screens. Require every claim to name a participant. The phrase to stop is "users found", every time, without exception: "which user, what did they do".

**the end of the week.** Injection debrief, script in the injection file. Then read the cohort's cut list out loud. Do not attribute cuts to individuals in the room, aggregate them. Individual notes go in the ledger.

**The week 3 failure to expect.** Testing with friends who want them to succeed, and recording opinions instead of behaviour. The catch: ask for the hesitation timings. A designer who recorded "she said it was clear" and cannot say how long she paused was watching for approval, not for data.

## Week 4: Ship and defend

**the start of the week.** One line: "the gate is early in the week, not the end of the week. Fixes take longer than checks."

**early in the week to mid week.** Read every gate result. The tell for a faked gate is uniform "pass" with no measured numbers. Send those back with one instruction: "give me the ratio".

**late in the week.** Handoff reviews. Read the three questions each designer wrote about their peer's spec. Those questions are the most honest measure of spec quality in the sprint and they cost you nothing to collect.

**the end of the week.** Merge freeze at 18:00. Everything not merged does not exist for the defense.

**the cohort review.** Defenses. 55 minutes each, five designers, plus breaks. That is a 6 hour day and it cannot be compressed. Run two in the study time, three after lunch. Guest critic sits in at least one.

**before the week opens.** Ledger update, sprint retro, and one honest message to each designer with their weakest round and the coaching action for Sprint 2.

## Load, actual

| Week | Admin hours |
|---|---|
| 1 | 9, the foundations session runs long |
| 2 | 7 |
| 3 | 8, the injection needs monitoring |
| 4 | 13, defense day is 6 of them |

Average 9 hours a week at 5 designers. At 8 designers, defense day alone becomes 9 hours and the reviewer role must be split off.

## Sprint 1 retro, questions to answer honestly

Committed to `guide/decision-log.md` at the end of the sprint.

1. Which task produced the least learning for the time it took. Cut it in the next cohort.
2. Which gate line did nobody pass. Either the teaching is missing or the line is wrong.
3. Did the injection land, or did it just cause damage. If nobody's reasoning changed, the injection was badly chosen.
4. Which designer surprised you, in either direction.
5. What did you fix for them that you should have made them fix. Every admin does this at least once in Sprint 1.
