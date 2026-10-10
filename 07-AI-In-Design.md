# 07 — AI In Design

Two different skills, both asked about in interviews now:

1. **Using AI as part of how you work.** Faster exploration, faster prototypes, without handing over judgement.
2. **Designing interfaces that contain AI.** Confidence, explanation, failure, and trust.

The program already allows AI tools with disclosure (`03-Books-And-Resources.md`, section 8). This file turns that into practice. Five short labs, one per sprint, each ending with something you can talk about in an interview.

---

## 1. The stance

**AI generates options. You decide.** An AI tool is useful for the first draft of anything you can check, and dangerous for anything you cannot. The labs are built around finding out, with your own evidence, where that line is for each task.

**Treat as unvalidated** any claim that an AI tool can moderate an interview or replace participants. At most it can help you screen or rehearse. The evidence must come from people.

**Never** use AI for: inventing a research finding, writing a quote a participant did not say, choosing between design options, or producing something you cannot explain in a defense.

**Always** carry the one-line footer on anything AI touched:

> *AI note: used {tool} to {what}. Verified by {how}.*

---

## 2. The AI log

Keep one file per sprint: `students/UX{n}/ai-log.md` in the current sprint folder. Append one row every time you use an AI tool on program work.

| Date | Task ID | Tool | What I asked for | What came back | What I kept, changed, rejected | How I verified |
|---|---|---|---|---|---|---|

It costs 30 seconds per entry and it is the evidence base for the interview question *"how do you use AI in your process?"*. The honest answer has three specific examples, including one where the tool was wrong.

---

## 3. The labs

Each lab is done on the week's Day 6 (cohort day). Commit the output to `students/UX{n}/week{n}/` in the current sprint folder.

| ID | Week | Time | Name | You prove |
|---|---|---|---|---|
| **L-AI1** | 2 | 90 min | Options to react against | You can use AI to widen options without lowering the standard |
| **L-AI2** | 6 | 90 min | Catch the invention | You can find where AI summarisation invents or flattens evidence |
| **L-AI3** | 9 | 90 min | From spec to throwaway prototype | You know what AI-built prototypes get wrong |
| **L-AI4** | 14 | 90 min | Reading code you did not write | You can use AI to read a component and verify what it says |
| **L-AI5** | 17 | 3 h | Design an AI feature | You can design confidence, explanation and failure so the user neither over-trusts nor ignores |

### L-AI1 — Options to react against (week 2)

**Learn first:** the three jobs of an error message (C4.1 reading) and your error inventory from C4.1.

**Method**
1. Pick three of your errors. For each, ask an AI tool for ten alternative messages. Use the same prompt for each, and write the prompt down.
2. Score every one of the 30 against your three-jobs rubric: says what happened, says what to do, names the field. Mark each pass or fail on each job.
3. Keep the best two per error and rewrite them in your own words. Reject the rest and write the reason for the three most common ways they failed.
4. Test your final three messages with one person who has not seen them. Record whether they know what to do.

**Done when**
- [ ] The prompt, the 30 outputs and the scoring table are committed
- [ ] A hit rate is stated ("7 of 30 passed all three jobs")
- [ ] The three most common failure patterns are named
- [ ] AI footer and AI log entries exist

→ `students/UX{n}/week2/L-AI1-options.md`

### L-AI2 — Catch the invention (week 6)

**Learn first:** your own R4.2 self-critique of an interview transcript.

**Method**
1. Take the transcript of one interview you ran and read yourself. Anonymised. Remove anything identifying before you paste it anywhere, and check the participant's consent covered this. If it did not, use a practice transcript supplied by the admin.
2. Ask an AI tool for the main themes and three supporting quotes.
3. Check every quote against the transcript. Mark each as: exact, paraphrased, or invented.
4. Compare the themes to your own notes. List what it missed, what it overstated, and any contradiction it smoothed away.
5. Write a verification checklist of at least five steps that you will apply to any AI summary of research.

**Done when**
- [ ] Every quote is checked and classified
- [ ] At least three specific errors are documented, or you state honestly that you found none and how thoroughly you looked
- [ ] The checklist exists
- [ ] The rule is restated in your words: why synthesis stays human

→ `students/UX{n}/week6/L-AI2-catch-the-invention.md`

### L-AI3 — From spec to throwaway prototype (week 9)

**Learn first:** your I1.1 state machine.

**Method**
1. Take one flow from your state machine (for example Active → PastDue → Active). Write a prompt for an AI prototyping tool (v0, Figma Make, or similar) that describes it.
2. Run the output. Walk it with your state machine beside you. List every state and transition it missed or invented.
3. Test it with keyboard only and with a screen reader for two minutes. Record what failed.
4. Decide what you would keep (layout idea, copy, structure) and what you must rebuild. Never ship it.

**Done when**
- [ ] The prompt and a screenshot of the output are committed
- [ ] A table of missed and invented states
- [ ] Two accessibility failures found
- [ ] One sentence: what the spec had that the prompt could not carry

→ `students/UX{n}/week9/L-AI3-prototype.md`

### L-AI4 — Reading code you did not write (week 14)

**Learn first:** the ARIA APG pattern for the component type you chose in T2.1.

**Method**
1. Open the source of one real component (a Polaris, Carbon or GOV.UK modal, select, or tabs). Ask an AI tool to explain its API, its keyboard behaviour and its focus management.
2. Check each claim three ways: the system's documentation, the ARIA APG pattern, and by using the live component with a keyboard.
3. Produce a corrected explanation: five facts you verified and two things the AI got wrong or could not know.
4. Say what you learned that changes your own component's documentation.

**Done when**
- [ ] Each AI claim is marked verified, wrong, or unverifiable
- [ ] Five verified facts, two corrections
- [ ] One change made to your own component docs

→ `students/UX{n}/week14/L-AI4-reading-code.md`

### L-AI5 — Design an AI feature (week 17)

**The case:** an underwriting tool where a model scores a loan application and a human decides. Full detail is in `Design-Sprint-5/01-project-options.md`, Option D. Everyone does this lab, whichever capstone option they chose. Option D designers extend it into their capstone.

**Learn first:** Google People + AI Guidebook (chapters on mental models, explainability and confidence, errors and graceful failure). Microsoft HAX guidelines, all 18.

**Method**
1. Write the two ways this goes wrong: over-trust and under-trust. For each, name a specific behaviour a real underwriter would show.
2. Design the score display. Decide what is shown (band, number, factors), what is not, and why. Say how your design avoids implying the model made the decision.
3. Design three failure states as first-class screens: model slow (2 to 8 seconds), confidence unavailable, and model clearly wrong (the underwriter overrides). Each must say what the user can do next.
4. Write the explanation text for one applicant decline. It must not claim the factors *caused* the decline.
5. Name one measure that would tell you in production that trust is calibrated, and one that would warn you it is not.
6. **Autonomy.** The business now asks whether the green band could be approved automatically. Without designing it, write the conditions you would require before agreeing: the autonomy level (suggest, approve-then-act, act-then-notify), the scope limit (which loans, up to what amount), the human approval step that remains, the audit trail, and how a wrong automatic decision is undone. If you cannot write the undo, say the feature should not ship.

**Done when**
- [ ] Over-trust and under-trust each have a named behaviour
- [ ] Score display decision is justified against HAX guideline numbers
- [ ] Three failure states designed, not described
- [ ] Decline explanation avoids causal language
- [ ] Two measures stated
- [ ] Autonomy conditions written: level, scope limit, approval, audit trail and undo

→ `students/UX{n}/week17/L-AI5-ai-feature.md`

---

## 4. In the interview

By week 23 you should be able to answer, with examples from your log:

- How do you use AI in your design process?
- Tell me about a time an AI tool was wrong and how you caught it.
- What would you never use AI for?
- How would you design the interface for a feature where the model is sometimes wrong?

The question bank (`Design-Sprint-6/07-interview-question-bank.md`) has these.

---

Next: `08-Prototyping-And-Responsive.md`.
