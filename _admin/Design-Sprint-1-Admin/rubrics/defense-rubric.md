# Rubrics

Three rubrics: defense, gate, and review quality. All three score 1 to 4 on the same meaning.

| Score | Meaning |
|---|---|
| 1 | Cannot do this yet |
| 2 | Can do it with support |
| 3 | Can do it alone |
| 4 | Can teach it |

---

## 1. Defense rubric

### Numbers
| Score | Looks like |
|---|---|
| 1 | 3 or fewer of 6. Does not know their own token values. |
| 2 | 4 of 6. Knows own system or the spec, not both. |
| 3 | 5 of 6. One gap, and knows it is a gap. |
| 4 | 6 of 6, and corrects a question that was imprecisely asked. |

### Reasoning
| Score | Looks like |
|---|---|
| 1 | "It looked better." No alternative considered. |
| 2 | Names an alternative but not the tradeoff. Reason is a convention with no source. |
| 3 | Names the tradeoff on both sides, cites a source, states the consequence accepted. |
| 4 | Names the tradeoff, cites evidence, states the consequence, and names the condition that would reverse the decision. |

### Live critique
| Score | Looks like |
|---|---|
| 1 | Describes what is on screen. Comments on taste. |
| 2 | Finds real flaws, names the principle inconsistently, does not state user cost. |
| 3 | Three flaws, principle named for each, user cost stated for each. |
| 4 | The above, plus names a good decision and what would break if it changed, plus identifies one flaw that is likely a deliberate business decision. |

### Adversarial
| Score | Looks like |
|---|---|
| 1 | Agrees with everything, or gets personally defensive. |
| 2 | Holds the position by repeating it louder. No new evidence. |
| 3 | Holds the position with evidence, calmly, under two pushes. |
| 4 | Holds where right, concedes where wrong, and states the fix for the part that was wrong. |

### Handoff
| Score | Looks like |
|---|---|
| 1 | Cannot answer three or more engineer questions. Spec is a screenshot. |
| 2 | Answers most, but the network failure and focus return questions are unanswered. |
| 3 | Answers everything asked. Spec covers states, tokens, focus, and copy. |
| 4 | The above, plus had already documented the question the engineer asked, plus knows which values are tokens and which are hardcoded and why. |

### Reflection
| Score | Looks like |
|---|---|
| 1 | Nothing to name, or "I would manage my time better". |
| 2 | Names something real but general. "My states were weak." |
| 3 | Names something specific, with the cost. "I sequenced states after fidelity, which cost two days of rework." |
| 4 | The above, plus names the process change, plus names something they still cannot do without hedging it. |

### Sprint 1 expected distribution
Mostly 2s. One or two 1s. One 3, usually in reflection or numbers. A designer scoring 3 or above across all six rounds in Sprint 1 arrived experienced, and the ledger should say so rather than treating it as growth.

---

## 2. Gate rubric

Applied to a claimed done deliverable. Not scored 1 to 4, it either holds or it does not, per line.

| Result | Meaning |
|---|---|
| Pass | Every line answered with checkable evidence |
| Pass with note | Every line answered, one or two lines weak, named and dated for fixing |
| Fail | Any line answered with a tick and no evidence, or any keyboard or screen reader failure |

**Automatic fail conditions**, no discussion:
- The flow cannot be completed with the keyboard
- Any interactive element has no visible focus indicator
- Body text below 4.5:1
- An error message that says "something went wrong" as its primary text
- A claim about users with no source
- A states matrix with an unexplained gap

**Do not negotiate an automatic fail.** The one time a gate is waived, the gate stops functioning for the rest of the program.

---

## 3. Review quality rubric

Scored per designer, weekly, from their pull request comments. This is the rubric most programs skip and it is the one that predicts whether a cohort improves each other or just coexists.

| Score | Looks like |
|---|---|
| 1 | "Looks good." Approves with no comment. |
| 2 | Points at something real but frames it as preference. "I would use more spacing here." |
| 3 | Names the principle and the user cost. Catches at least one thing per week the author had not seen. |
| 4 | The above, plus catches a system level consequence. "This works on your screen but the component has no disabled state, so the payment screen will fork it." |

### Weekly log

```
Week 2 review quality
UX1: 3  caught the missing focus state on the upload dropzone
UX2: 2  three comments, all spacing preferences
UX3: 4  caught that the select variant will break at 320px for every consumer
UX4: 1  two approvals, no comments. Flagged, spoken to.
UX5: 3  asked for the evidence behind a copy change, correctly
```

**Intervention for a 1.** Not a warning. Assign them to review the strongest designer's work next week and require three comments. Reviewing strong work teaches faster than reviewing weak work, because the flaws are subtle and they have to look properly.

---

## 4. What the scores are for

The ledger, and nothing else. No public leaderboard, no ranking read out to the cohort.

Two reasons. A public ranking makes the cohort compete instead of review each other honestly, which destroys the highest value part of the program. And a Sprint 1 score is a measure of what someone walked in with, not of what they are going to be. The number that matters is the delta by Sprint 6, and telling someone their week 4 rank in a 24 week program is just noise that changes how they behave for the wrong reasons.

Each designer is told their own scores, directly, with the coaching action. Nobody is told anyone else's.
