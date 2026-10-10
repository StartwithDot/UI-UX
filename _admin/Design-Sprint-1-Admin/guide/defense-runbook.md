# Defense Runbook

How to run a defense. 55 minutes per designer, end of every sprint. Six rounds.

The defense is the only mechanism in the program that cannot be gamed, so it is the only one that matters at the end. Everything else can be produced with enough hours and enough help.

---

## Before the day

- Read the designer's committed work. All of it. You cannot run the adversarial round without knowing their weakest decision.
- Pick their weakest decision. Not their most obvious flaw, their weakest reasoning.
- Choose the critique surface. Something they have not seen and cannot have prepared. A live product, opened in front of them.
- Draw the numbers questions from `../question-bank/numbers.md`. Six questions, at random, in front of them so they see it is random.
- Book a guest critic for at least one defense per sprint. An external voice removes the suspicion that the score is about the relationship.

## The six rounds

### 1. Numbers, 8 minutes

Six questions. Rapid fire. No file open, no notes.

Sample, Sprint 1:
- What is the contrast ratio of your body text against its background
- What is your smallest interactive target and what is the WCAG minimum
- What is your base type size and your ratio
- Which WCAG criterion covers focus not being obscured
- What is your primary metric and its current baseline
- Name your guardrail metric and what it protects against

**Scoring.** Right or wrong. 6 of 6 is expected of someone who built their own tokens. 4 of 6 passes. Below 4 means they are working inside a system they do not know, which is the most common Sprint 1 failure and worth naming plainly.

### 2. Reasoning, 12 minutes

Pick three decisions from their work. For each: why this, and what did you reject.

What you are listening for:
- A tradeoff named on both sides
- A source cited, even a weak one, labelled as weak
- The consequence they accepted

Failing answers: "it looked better", "that is standard", "the client wanted it", "I saw it on Dribbble".

A strong answer sounds like: "one page loses the sense of progress, four steps costs four network round trips on 3G. I went with three steps because the observation in R1.5 showed the participant losing their place after the sixth field, and three steps keeps each screen under six fields. The cost is one extra tap for a fast user like Priya."

### 3. Live critique, 10 minutes

Open a surface they have not seen. Give them 2 minutes to look, then 8 to talk.

Require: three flaws, each with the principle named and the user cost stated. One thing that works and why it works.

**Scoring.** Naming a flaw is 1 point. Naming the principle is 2. Naming the user cost is 3. Naming a good decision and what would break if changed is 4. Most designers plateau at 2 for the first two sprints, which is normal and worth telling them.

### 4. Adversarial, 10 minutes

Attack their weakest decision. Hold the position even when they answer well. Then attack a second time from a different angle.

Script pattern:
> "Your document guidance screen adds a step before upload. The department's brief was to reduce counter visits, and you have added friction to the online flow. Defend that."

What you are watching for, in order of what it predicts:

| Behaviour | What it means |
|---|---|
| Concedes the point that is actually wrong, states the fix | Best outcome. Rare in Sprint 1. |
| Holds the position with evidence, calmly | Strong. |
| Holds the position with no evidence, louder | Common. Coach it. |
| Collapses and agrees with everything | Worse than arguing. A designer who folds under one push will fold in front of a stakeholder. |
| Gets personally defensive | Note it, address it privately, not in the room. |

**The line to use when they fold too fast:** "I was wrong to push there, your original answer was right. Say it again and hold it." Then see if they can.

### 5. Handoff, 8 minutes

You play the engineer. Take their handoff spec and ask only what an engineer would actually ask.

- What happens if the upload succeeds but the network drops before the response
- What is the maximum file size and what happens at exactly that size
- Which of these values is a token and which did you hardcode
- What is the focus target after this modal closes
- Is this string translated, and what happens when it is 30 percent longer

**Scoring.** Count how many questions they cannot answer. Every one is a gap a real engineer would have had to interrupt them for.

### 6. Reflection, 7 minutes

Three questions:
1. What did you get wrong this sprint
2. What would you do differently with the same four weeks
3. What is the thing you still cannot do

**The strongest possible answer** names something specific, states the cost, and does not perform humility. "I designed the happy path first and treated states as cleanup in week 3. That cost me two days of rework and my upload states are still the weakest screens in the flow."

**The weakest answer** is "I would manage my time better", which is what someone says when they have not looked.

A designer with nothing to name here has not looked, and that is worth saying out loud. This round predicts trajectory better than any other.

---

## Scoring

Per round, 1 to 4.

| Score | Meaning |
|---|---|
| 1 | Cannot do this yet |
| 2 | Can do it with support |
| 3 | Can do it alone |
| 4 | Can teach it |

**Sprint 1 expectation:** mostly 2s, some 1s, a 3 somewhere. Anyone with 3s across the board in Sprint 1 either came in experienced or is being scored generously.

**Progression that matters:** the number that predicts placement is not the Sprint 6 score, it is the delta from Sprint 1 to Sprint 6 on the reasoning and adversarial rounds. Craft scores rise for everyone. Reasoning scores only rise for people who are actually learning.

### Recording

```markdown
## Sprint 1 defense, UX3
Date: | Admin: | Guest critic:

| Round | Score | Note |
|---|---|---|
| Numbers | 4/6 correct, 2 | Did not know focus obscured criterion. Knew all own token values. |
| Reasoning | 3 | Strong on form structure, cited own observation. Weak on colour, no reason given. |
| Critique | 2 | Found flaws, named principles on 2 of 3, no user cost stated |
| Adversarial | 2 | Held on the first push, folded on the second when I repeated it louder |
| Handoff | 2 | Could not answer network drop or focus return |
| Reflection | 3 | Named the states sequencing mistake specifically, without prompting |

Weakest: adversarial. Folds under repetition rather than argument.
Strongest: reflection. Sees own process clearly.
Coach next sprint: hold a position when the pressure is only volume. Assign critique lead in Sprint 2 week 1.
Told them: yes, all of the above, directly.
```

The last line matters. A score not delivered to the designer is administration, not teaching.

---

## Failure and repeat

A round scored 1 is repeated within a week, once. The repeat is recorded separately from the original. Nothing is retroactively upgraded.

A designer who scores 1 on numbers twice in a row is not working inside their own system, and the intervention is not more practice, it is making them rebuild their tokens by hand.

No one is removed from the cohort for a low defense score. Removal is only for silence or dishonesty, per the student guide.
