# Design Sprint 1, Admin

Private. Never shared with the cohort. If a designer can read this, the defense is worthless.

---

## What is here

| Path | Contents |
|---|---|
| `guide/program-flow.md` | How the 24 weeks run, what the admin does when |
| `guide/sprint-operating-flow.md` | The week by week operating manual for this sprint |
| `guide/defense-runbook.md` | How to run a defense, what to ask, how to score |
| `guide/review-process.md` | How to review design work in git and in Figma |
| `guide/troubleshooting.md` | Every failure mode seen and what to do about it |
| `answers/week1.md` to `week4.md` | Model answers and the range of acceptable ones |
| `question-bank/` | Numbers, reasoning, adversarial, and critique questions per sprint |
| `failure-injections/` | Sealed scope changes, one per sprint, with the delivery script |
| `rubrics/` | Defense scoring, gate scoring, review quality scoring |
| `ledger/` | Per designer record across 24 weeks |

## Admin roles

| Role | Who | Load |
|---|---|---|
| Core admin | 1 person | 6 to 8 hours a week. Runs kickoff, approves system merges, runs defense, keeps the ledger. |
| Reviewer | Can be the same person at 5 designers | 3 to 4 hours a week. Reviews pull requests against the gates. |
| Guest critic | Rotating, external | 90 minutes per sprint. Sits in one critique and one defense. Value is that they do not know the cohort. |

At 5 designers one person can hold core admin and reviewer. Above 8 designers, split them.

## The weekly rhythm

| Day | Admin action | Time |
|---|---|---|
| Mon | Post the week goal, assign positions from the rotation log, assign the teardown subject | 30 min |
| Tue | Nothing. Let them work. | 0 |
| Wed | Read open pull requests, comment on the two weakest | 60 min |
| Thu | Sit in critique. Do not lead it. Note what the critique lead misses. | 90 min |
| Fri | Approve system merges, run the gate on one deliverable at random, close the rotation log | 90 min |
| Sat | Sit in the spine session. Ask one question the presenter did not prepare for. | 60 min |
| Sun | Update the ledger, write next week's goal | 45 min |

## The non negotiables

1. **Never design for them.** The instinct to open Figma and fix it is the single most damaging admin behaviour. Ask the question that makes them see it.
2. **Never approve a gate you have not checked.** One unchecked gate teaches the whole cohort that the gate is theatre.
3. **Never soften a defense score.** The score is the honest signal. A generous score removes the only reliable feedback in the program.
4. **Deliver the injected failure on schedule, even when the week is going badly.** Especially then. A cohort that only handles change when convenient has not learned anything.
5. **Read the reviews, not just the work.** Rubber stamp approvals are the earliest sign a cohort is drifting into politeness.

## Sprint 1 specifics

| Item | Detail |
|---|---|
| Project | Aadhaar address update flow |
| Designers | 5, UX1 to UX5 |
| Injected failure | Week 3, Monday. Sealed in `failure-injections/sprint1.md`. |
| Milestone stations | P1 reframe, S1 foundations, R2 test, S4 gate and handoff |
| Defense | Week 4 Saturday, 55 minutes per designer |
| The failure to expect | Designers who make it look good and cannot say why. The numbers round catches this in eight minutes. |

## The ledger

One file per designer, updated weekly. The 24 week record is what makes a reference letter or a placement recommendation defensible.

```
ledger/UX1.md
```

Contents: weekly commit count, review quality, gate results, defense scores per round, whiteboard why results, injected failure handling, and the honest one line assessment that you would not say to their face in week 2 but will need in week 20.
