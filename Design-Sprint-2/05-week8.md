# Week 8 — Synthesise

**Sprint 2 · Week 8 of 8 · Theme: turning evidence into decisions, and defending a sample of five**

---

## By Friday you can

- Present findings with confidence levels that match their evidence
- Hold a contradiction open instead of resolving it by preference
- Trace every design change to a specific finding
- Defend a five-person study against someone who wants to dismiss it

## The week at a glance

| Day | LEARN | DO |
|---|---|---|
| **Mon** | Just Enough Research on reporting · NNGroup on personas | R6.1 R6.2 — findings report, confidence audit |
| **Tue** | Journey mapping · service blueprints | R6.3 P8.1 — journey map, finding-to-decision map |
| **Wed** | Your own Sprint 1 craft notes | C9.1 — redesign the two worst steps |
| **Thu** | Norman on human error | C9.2 S9.1 — full flow, evidence-linked spec · **critique** |
| **Fri** | — | **Defense, 55 min** · P8.2 reflection |
| **Sat** | — | S10 system release · F8 sprint retro |

---

# Monday

## LEARN — 75 minutes

| Source | What exactly | Time |
|---|---|---|
| **Just Enough Research** | The chapter on reporting and communicating findings | 30 min |
| **NNGroup** | "Personas Make Users Memorable" and "Why Personas Fail" | 25 min |
| **Your own R5.5** | Read your findings and mark the ones you *want* to be true | 20 min |

**Read both persona articles.** Personas are useful when they are built from research and treated as a summary of evidence. They are harmful when they become a fictional person whose preferences get invoked to win arguments. You will build one this week, from your five, and you will label what it is grounded in.

→ **Commit** `students/UX{n}/week8/day1-learning.md`

## DO — 2 hours

### R6.1 — Findings report

**Method**
Write the report. Six sections.

1. **What you set out to learn.** Your three questions from R3.3.
2. **What you did.** Method, sample, dates, and the recruitment channel. The channel matters, because it is the main source of your bias.
3. **What you found.** Each finding with its denominator, its evidence, and its confidence.
4. **What contradicts.** At least one place where two participants wanted opposite things, or where the interviews and the testing disagreed. **Do not resolve it by choosing the one you prefer.** State both, state what would settle it.
5. **What you still do not know.** With how you would find out and roughly what it would cost.
6. **What you recommend**, ranked, each traced to a finding.

**Worked example** — section 4:

> **Contradiction.** P2 and P4 both wanted the form to remember their details between sessions, and described re-entering everything as the worst part. P5 explicitly did not want anything saved, because the application is filled on a shared phone at a neighbour's shop and she did not want her income details visible to whoever used it next.
>
> These are both correct. The device context is different, and I do not know which context is more common. What would settle it: one question in the mission's existing SMS survey asking whether the application was filled on a personal or a shared device. Until then, any save feature has to be explicit and clearable, which is more work than either participant asked for.

Note that the contradiction produced a better design constraint than either individual preference would have.

**Done when**
- [ ] All six sections
- [ ] Recruitment channel named as a bias source
- [ ] Every finding has a denominator and a confidence level
- [ ] At least one contradiction stated and left unresolved, with what would settle it
- [ ] Recommendations ranked and each traced to a finding

→ `students/UX{n}/week8/R6-1-findings-report.md`

### R6.2 — Confidence audit

**Method**
1. Go through every finding and ask: what exactly is this based on? Something they *did*, or something they *said*?
2. Re-grade. What people do is stronger evidence than what people say, and what they say about the past is stronger than what they say they would do in future.
3. Find the findings where your confidence exceeds your evidence. There will be some, and they will be the ones that support your favourite idea.
4. Downgrade them in writing.

**Done when**
- [ ] Every finding marked as said-based or did-based
- [ ] Any hypothetical-based finding downgraded
- [ ] At least one finding you downgraded, named, with why
- [ ] Nothing rated high confidence on n=1 or n=2

→ `students/UX{n}/week8/R6-2-confidence-audit.md`

---

# Tuesday

## LEARN — 75 minutes

| Source | What exactly | Time |
|---|---|---|
| **NNGroup** | "Journey Mapping 101" and "Service Blueprints: Definition" | 35 min |
| **Just Enough Research** | The section on turning research into design direction | 25 min |
| **Your R4.7 affinity map** | Re-read the group names | 15 min |

→ **Commit** `day2-learning.md`

## DO — 2 hours

### R6.3 — Journey map

**Method**
1. Map the whole journey, not just the part that happens on a screen. It starts when someone hears the scholarship exists and ends when money arrives or does not.
2. Rows: what they do · what they think · what they feel · where the pain is · what is happening behind the scenes that they cannot see.
3. **Every point must be traceable to a participant.** Mark each with P1 to P5. Anything you cannot attribute is your invention and must be labelled as an assumption.
4. Mark the offline steps. Getting a certificate, visiting an office, asking a teacher. Most of the journey is not on your screen, and the biggest failures usually happen off it.

**Done when**
- [ ] The journey extends before and after the digital flow
- [ ] Five rows including the behind-the-scenes row
- [ ] Every point attributed to a participant or labelled as an assumption
- [ ] Offline steps included
- [ ] The worst moment is identified, with the evidence for it

→ `students/UX{n}/week8/R6-3-journey-map.md`

### P8.1 — Finding-to-decision map

**Method**
1. A table with one row per design decision.
2. Columns: the decision · the finding it comes from · the finding's confidence · what you would change if that finding turned out to be wrong.
3. **Any decision with no finding behind it goes in a separate list**, labelled "designer's judgement". That list is allowed to exist. It is not allowed to be disguised.

**Worked example**

| Decision | Finding | Confidence | If the finding is wrong |
|---|---|---|---|
| Ask which income certificate they have before showing the upload field | R5.5-03, 4 of 5 could not identify the valid certificate | High | If applicants actually know which one is valid, this question adds a step for no benefit and should be removed. |
| Show the full document list up front rather than progressively | R6-1-02, 3 of 5 wanted to know everything needed before starting | Medium | If most applicants prefer to start immediately, this becomes an intimidating wall of requirements and should be collapsible. |

**Judgement list:** button placement, exact wording of the confirmation heading, icon choices. No research supports these. They are craft decisions and I am naming them as such.

**Done when**
- [ ] Every design decision in the table
- [ ] Every one traced to a finding, or moved to the judgement list
- [ ] Confidence carried across from R6.2
- [ ] Every row has an "if wrong" answer
- [ ] The judgement list exists and is honest

→ `students/UX{n}/week8/P8-1-finding-to-decision.md`

---

# Wednesday

## LEARN — 45 minutes

Re-read your own Sprint 1 week 1 type and colour work, and the Sprint 1 accessibility gate. You are about to design again after three weeks of research, and the craft standard has not dropped.

→ **Commit** `day3-learning.md`

## DO — 2.5 hours

### C9.1 — Redesign the two worst steps

**Method**
1. Take the two steps your evidence says are worst.
2. Redesign both. Full states, using the shared system.
3. For each, state the finding, what you changed, and what you predict will happen.
4. State how you would test whether the prediction was right.
5. Sprint 1 standards still apply: contrast measured, focus order defined, real content, no placeholder text.

**Done when**
- [ ] Two steps redesigned, all relevant states
- [ ] System components used
- [ ] Each change linked to a finding by its ID
- [ ] A stated prediction per change, and how you would test it
- [ ] Contrast and focus order done, not deferred

→ `students/UX{n}/week8/C9-1-redesign.md`

---

# Thursday

## LEARN — 60 minutes

| Source | What exactly | Time |
|---|---|---|
| **The Design of Everyday Things** | The chapter on human error: slips versus mistakes | 40 min |
| **Your R5.5** | Classify each of your findings as a slip or a mistake | 20 min |

**Why:** a slip is when the user intended the right thing and did the wrong thing — usually a design problem you can fix with layout, size, or confirmation. A mistake is when they intended the wrong thing — usually a problem with the conceptual model, which layout cannot fix. Treating a mistake as a slip is why so many redesigns fail.

→ **Commit** `day4-learning.md`

## DO — 2 hours (plus critique)

### C9.2 — Full revised flow
Every screen, mid to high fidelity, incorporating everything. Using the system. Slips and mistakes handled differently and the difference stated.
→ `students/UX{n}/week8/C9-2-revised-flow.md`

### S9.1 — Evidence-linked spec
The handoff spec, to the Sprint 1 standard, with one addition: **every non-obvious decision carries the finding ID it came from.** An engineer who wants to change something should be able to see what evidence they would be arguing with.
→ `students/UX{n}/week8/S9-1-spec.md`

### Thursday critique — 90 minutes
Final critique. Present the flow and the finding-to-decision map together. The critique focus: **is every change earned by evidence, or has some craft preference been laundered through a quote?**

---

# Friday

## Defense — 55 minutes

| Part | Time | What you do |
|---|---|---|
| Research walk | 10 min | Your questions, your method, your sample. From memory. |
| Findings | 10 min | Three findings with confidence and evidence |
| Contradiction | 5 min | The one you did not resolve, and why that is the right answer |
| Sample size attack | 10 min | You will be told five is worthless. Answer it properly. |
| Failure story | 10 min | The week 7 injection |
| Alternative | 10 min | A constraint card is drawn |

**On the sample size attack.** The wrong answers: getting defensive, claiming five is statistically meaningful, or conceding that the research was worthless. The right answer states what formative qualitative research with five participants can support — the existence and nature of problems — and what it cannot — frequency, magnitude, or a completion rate. Then it names what you would run to get the second kind, and what that would cost.

**Sprint 2 constraint cards:** you get one participant instead of five · no recording allowed · participants are all from one school · the mission insists the form length is the problem and will not fund anything else · you must report to someone who does not believe in research.

## P8.2 — Reflection
- The finding you were most wrong about at the start
- Your worst interviewing habit and whether it improved between interview 1 and 5
- The question in the defense you answered worst
- One specific behaviour you will change in Sprint 3

→ `students/UX{n}/week8/P8-2-reflection.md`

---

# Saturday

## S10 — System release

**S10.1** — Sprint 2 release, changelog updated.
**S10.2** — Every component documented to the same standard. No exceptions carried forward.
**S10.3** — `debt.md` updated. Note which Sprint 1 debt items are now two sprints old, because Sprint 4 is going to inherit them.

## F8 — Sprint retro

**F8.1 — Why session: the psychology of decision-making.** Choice overload, defaults, loss aversion. Illustrated with the scholarship form and with what your participants actually did.
→ `fundamentals/why-sessions/week08-decision-making.md`

**F8.2 — Teardown:** a food delivery app's checkout, chosen because it is the opposite of everything in this sprint — high frequency, low stakes, heavily optimised.
→ `fundamentals/teardowns/08-delivery-checkout.md`

**F8.3 — Explainer.** One page on why five users is enough for some things and not others, written for someone who has never done research.
→ `fundamentals/explainers/sprint2-sample-size.md`

**F8.4 — Drill log review.** 40 entries now.

---

## Sprint 2 done when

- [ ] 20 learning summaries
- [ ] 5 interviews, consented, anonymised, transcribed in part
- [ ] Self-critique with counted mistakes
- [ ] 5 usability sessions with severity-rated findings
- [ ] Findings report with confidence levels and one unresolved contradiction
- [ ] Journey map with every point attributed
- [ ] Finding-to-decision map, with an honest judgement list
- [ ] Redesigned flow and evidence-linked spec
- [ ] Post mortem
- [ ] Defense passed
- [ ] Reflection
- [ ] System released, debt updated
- [ ] 4 teardowns, 1 explainer, 40 drill entries

Next: `../Design-Sprint-3/00-READ-FIRST.md`
