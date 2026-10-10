# Week 5 — Plan

**Sprint 2 · Week 5 of 8 · Theme: what research is for, and how to plan something that can fail**

---

## By the end of this week you can

- List your assumptions and rank them by what it would cost to be wrong
- Choose a research method because it answers your question, not because it is familiar
- Write a research plan that states in advance what result would prove you wrong
- Recruit five real participants

## The week at a glance

| Step | LEARN | DO |
|---|---|---|
| **1** | Just Enough Research ch. 1–3 | R3.1 R3.2 — assumption list, risk ranking |
| **2** | Just Enough Research ch. 4–5 · NNGroup on method choice | R3.3 — research plan |
| **3** | `06-research-ethics.md` · consent and minors | R3.4 R3.5 — consent form, recruitment |
| **4** | Just Enough Research ch. 6 · Interviewing Users ch. 1 | R3.6 P5.1 — discussion guide, stakeholder map · **critique** |
| **5** | NNGroup on analytics as a research input | R3.7 P5.2 — desk research, reframed brief |
| **6** | — | S6 system contribution · F5 why session and teardown |

---

# Day 1

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **Just Enough Research**, Erika Hall | Ch. 1 "Enough is Enough", Ch. 2 "The Basics", Ch. 3 "The Process" | 60 min |
| **NNGroup** | "When to Use Which User-Experience Research Method" | 20 min |
| **The brief** | `01-project-brief.md`, read twice | 10 min |

**What to take from Hall:** research is not a phase, it is how you reduce the risk of building the wrong thing. The most common failure is not doing too little research, it is doing research that could not have changed anyone's mind.

→ **Commit** `students/UX{n}/week5/session1-learning.md`

## DO — 90 minutes

### R3.1 — Assumption list

**Method**
1. Read the brief and write down everything it treats as true without evidence.
2. Include the mission's central claim: that drop-off is caused by form length.
3. Include your own assumptions. You have them already, from Sprint 1 habits.
4. Aim for 15 or more. Fewer than 10 means you are still reading the brief as fact.
5. Mark each as: stated in the brief · implied by the brief · yours.

**Worked example** — a few rows, for a different brief:

| Assumption | Source | Why it might be false |
|---|---|---|
| Applicants drop off because the form is long | Stated | Length correlates with drop-off but does not cause it. They may drop off at one specific field. |
| Applicants have the documents ready when they start | Implied | The brief never says this. If they do not, drop-off happens at the upload step regardless of form length. |
| Parents fill the form, not students | Mine | I assumed this because of the age group. Never checked. |

**Done when**
- [ ] 15 or more assumptions
- [ ] The brief's central claim is on the list
- [ ] At least 4 are your own, not the brief's
- [ ] Each has a source label and a reason it might be false

→ `students/UX{n}/week5/R3-1-assumptions.md`

### R3.2 — Rank by risk

**Method**
1. For each assumption, score two things, 1 to 5.
   - **Uncertainty:** how sure are you it is true?
   - **Cost of being wrong:** what happens if you build on it and it is false?
2. Risk = uncertainty × cost.
3. Sort. The top three are what you research. Everything else waits.
4. For the top three, write what you would need to see to change your mind.

**Why this ordering matters:** research capacity is small. Five interviews cannot answer 15 questions. Ranking is how you decide which three questions the five interviews are for.

**Done when**
- [ ] Every assumption scored on both dimensions
- [ ] Sorted by risk
- [ ] Top three identified
- [ ] For each of the top three, a stated falsification condition

→ `students/UX{n}/week5/R3-2-risk-ranking.md`

---

# Day 2

## LEARN — 90 minutes

| Source | What exactly | Time |
|---|---|---|
| **Just Enough Research** | Ch. 4 "The Organisation", Ch. 5 "User Research" | 50 min |
| **NNGroup** | "Quantitative vs. Qualitative Research" and the method-choice article again, this time with your top three questions open | 25 min |
| **Your R3.2** | Re-read your top three | 15 min |

**What to take:** qualitative tells you *why* and *how*, in small numbers. Quantitative tells you *how many* and *how often*, in large numbers. Choosing the wrong one is the most expensive mistake in research planning, because you find out at the end.

→ **Commit** `session2-learning.md`

## DO — 2 hours

### R3.3 — The research plan

**Method**
Write the plan. It has eight sections and none are optional.

1. **The questions.** Your top three from R3.2, phrased as questions, not topics.
2. **The method for each**, with a reason. Interview, usability test, analytics, survey, diary study. Why this one answers this question.
3. **Who you need.** Specific: "parents of students in classes 9 to 12 who started an application in the last 6 months and did not finish". Not "users".
4. **How many, and why that number.** Five is a defensible answer if you state what five can and cannot support.
5. **What you will do.** The actual protocol.
6. **What would falsify each question.** State, in advance, the result that would prove your expectation wrong. This is the section people skip and it is the section that makes the plan real.
7. **What you cannot learn this way.** Every method has a blind spot. Name yours.
8. **Timeline.** Recruiting takes longer than running.

**Worked example** — section 6, for a different question:

> **Question:** Do applicants abandon because of form length, or because of a specific field?
> **What would falsify "length":** If abandonment is concentrated at one or two specific fields rather than spread across the form, length is not the cause. I will know this from the analytics drop-off by field, and from where in the task participants hesitate.
> **What would falsify "specific field":** If abandonment is roughly evenly distributed across the form and participants report fatigue rather than confusion, length is the better explanation.

Note that both directions are stated. A plan that can only confirm what you expect is not a plan.

**Done when**
- [ ] All eight sections
- [ ] Every method choice has a reason tied to its question
- [ ] The participant description is specific enough to recruit from
- [ ] The sample size is justified, not just stated
- [ ] Section 6 states falsification in both directions for each question
- [ ] Section 7 names a real blind spot

→ `students/UX{n}/week5/R3-3-research-plan.md`

---

# Day 3

## LEARN — 75 minutes

| Source | What exactly | Time |
|---|---|---|
| **`06-research-ethics.md`** | The whole file. Read it before you contact anybody. | 30 min |
| **Just Enough Research** | The section on ethics and consent | 20 min |
| **NNGroup** | "Ethical Maturity in User Research" | 25 min |

**Why this is a whole learning block:** this sprint involves students. Some participants may be under 18. Consent from a minor is not sufficient, recording a minor has different rules, and "it is only for a design project" is not an exemption.

→ **Commit** `session3-learning.md`

## DO — 2 hours

### R3.4 — Consent form and script

**Method**
1. Write the consent script. It must state, in plain language: who you are, what you are doing, what you will record, where it will be stored, how long you keep it, who sees it, that they can stop at any time with no consequence, and that you are testing the design and not them.
2. Write a second version for a participant under 18, plus the guardian consent it requires.
3. Write your anonymisation rule: what you strip before anything is committed to git.
4. **Nothing identifiable goes in the repository.** No names, no phone numbers, no school names, no faces. Participants are P1 to P5.

**Done when**
- [ ] Adult consent script, in plain language, all eight points
- [ ] Minor version plus guardian consent
- [ ] Anonymisation rule written and specific
- [ ] Storage location and retention period stated
- [ ] Nothing in the script requires the participant to understand design jargon

→ `students/UX{n}/week5/R3-4-consent.md`

### R3.5 — Recruit

**Method**
1. Write your screener: three or four questions that confirm someone matches your R3.3 description.
2. Reach out. Real people. Aim to confirm five with two backups, because two will cancel.
3. Log every attempt, including refusals. Who you could not reach is itself a finding about who the service excludes.
4. Schedule for week 6.

**If recruiting fails,** that is not a disaster and it is not an excuse. It is a finding. Write down who you could not reach and why, and adjust your method — a shorter session, a phone call instead of a video call, a different time of day. Document the change.

**Done when**
- [ ] Screener written
- [ ] 5 confirmed, 2 backups
- [ ] Every attempt logged including refusals
- [ ] Sessions scheduled in week 6
- [ ] Any change of method documented with the reason

→ `students/UX{n}/week5/R3-5-recruitment-log.md`

---

# Day 4

## LEARN — 75 minutes

| Source | What exactly | Time |
|---|---|---|
| **Just Enough Research** | Ch. 6 "Competitive Research" | 30 min |
| **Interviewing Users**, Portigal | Ch. 1, on why interviewing is harder than it looks | 30 min |
| **Your R3.3** | Re-read your three questions before writing the guide | 15 min |

→ **Commit** `session4-learning.md`

## DO — 2 hours (plus critique)

### R3.6 — Discussion guide

**Method**
1. Structure: warm-up, the participant's own story, the specific experience, then wrap-up.
2. Start broad. "Tell me about the last time you applied for something for your child's education" before anything about this specific form.
3. Every question must be open. If it can be answered with yes or no, rewrite it.
4. **Ban list, written at the top of your own guide:** any question containing "would you", "do you like", "how easy was", or the name of a feature.
5. Write your follow-up probes: "tell me more about that", "what happened next", "what were you expecting", "walk me through that".
6. Plan for silence. Write "wait 5 seconds" into the guide at three places, because you will not do it unless it is written down.

**Worked example**

| ❌ Bad | Why | ✅ Better |
|---|---|---|
| "Would you use an app for this?" | Hypothetical. People are bad at predicting their own behaviour. | "How did you fill it in last time? Walk me through what you did." |
| "Was the form too long?" | Leading, and it hands them your hypothesis. | "Tell me about the last time you filled this in. Where did you stop?" |
| "Do you find uploading documents difficult?" | Yes/no, and it suggests the answer. | "Tell me about the documents you needed. How did you get them?" |

**Done when**
- [ ] Four sections, in order
- [ ] Zero yes/no questions
- [ ] Zero hypotheticals
- [ ] Ban list written at the top of your own guide
- [ ] Probes written down
- [ ] Silence planned at three specific points
- [ ] It fits in 45 minutes with room to go off script

→ `students/UX{n}/week5/R3-6-discussion-guide.md`

### P5.1 — Stakeholder map

**Method**
1. List everyone who affects or is affected: applicants, parents, teachers, the mission's programme staff, the state education department, the verification officers, the fund disbursers.
2. For each: what they want, what they fear, what they control.
3. Mark where two stakeholders want opposite things. Those conflicts are your real design constraints, and they will not be in the brief.

**Done when**
- [ ] Seven or more stakeholders
- [ ] Each has wants, fears, and controls
- [ ] At least two genuine conflicts identified
- [ ] Each conflict has one line on how it shows up in the product

→ `students/UX{n}/week5/P5-1-stakeholders.md`

### Critique — 90 minutes
Present your research plan. The critique question is not "is this nice", it is **"could this plan produce a result that surprises you?"** If not, it is confirmation, not research.

---

# Day 5

## LEARN — 60 minutes

| Source | What exactly | Time |
|---|---|---|
| **NNGroup** | "Analytics and User Experience" and "Funnel Analysis" | 30 min |
| **Just Enough Research** | Ch. 7, on evaluative research, as preparation for week 7 | 30 min |

→ **Commit** `session5-learning.md`

## DO — 90 minutes

### R3.7 — Desk research

**Method**
1. Find three comparable services: another state's scholarship portal, a bank's education loan application, a government benefit application.
2. For each, walk the flow as far as you can and note: how they handle documents, how they handle eligibility, how they handle status after submission.
3. Note one thing each does better than the brief's service, and one thing each does worse.
4. Cite what you found. Screenshots, dates.

**Done when**
- [ ] Three services examined
- [ ] Documents, eligibility, and status covered for each
- [ ] One better and one worse thing per service, both specific
- [ ] Evidence attached, with dates

→ `students/UX{n}/week5/R3-7-desk-research.md`

### P5.2 — Reframe the brief

**Method**
1. The brief says drop-off is caused by form length.
2. Using R3.1, R3.2, and R3.7, write what you now think the problem *might* be. Note the word might.
3. Use the Sprint 1 problem statement shape, but add a confidence line: what you would need to know to state it with confidence.
4. **You are not allowed to have concluded anything yet.** You have not spoken to a user. This document is a hypothesis, labelled as one.

**Done when**
- [ ] A reframed hypothesis, explicitly labelled as unverified
- [ ] It differs from the brief's framing, or you have stated why the brief is probably right
- [ ] A confidence line stating what would confirm it
- [ ] No claim about users that is not marked as an assumption

→ `students/UX{n}/week5/P5-2-reframed-brief.md`

---

# Day 6 — Cohort day

## S6 — System, 90 minutes

The Sprint 1 system carries forward. This week it needs the components a research-heavy sprint will use.

**S6.1** — Add or document: radio group, checkbox group, date input, and a status badge. Same documentation standard as Sprint 1: all states, keyboard behaviour, screen reader announcement, semantic element, one do and one do not.
→ `system/components/{component}.md`

**S6.2** — Review one peer's contribution, naming one thing that will break in use.

**S6.3** — Work through one item from the Sprint 1 `system/docs/debt.md`. It does not get to sit there for 20 weeks.

## F5 — Fundamentals

**F5.1 — Why session: memory, attention and cognitive load.** From *100 Things Every Designer Needs to Know About People*. Illustrated with the scholarship form, not with textbook examples.
→ `fundamentals/why-sessions/week05-memory-attention.md`

**F5.2 — Teardown:** a state government scholarship or benefit portal, other than the one in the brief.
→ `fundamentals/teardowns/05-benefit-portal.md`

**F5.3 — Drill continues.** Session 21 onward.

---

## End of week checklist

- [ ] 5 learning summaries
- [ ] R3.1 through R3.7
- [ ] P5.1, P5.2
- [ ] 5 participants confirmed and scheduled, 2 backups
- [ ] Consent forms ready, including the minor version
- [ ] Critique attended

**Do not enter week 6 without confirmed participants.** Everything in weeks 6 to 8 depends on it. If you are not scheduled by the end of the week, tell the admin on Day 5, not on Day 1 of week 6.

Next: `03-week6.md`
