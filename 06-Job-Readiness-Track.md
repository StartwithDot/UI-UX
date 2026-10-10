# 06 — Job Readiness Track

The portfolio is built during the program, not after it.

Sprint 6 is the sprint where you finish the portfolio and apply. If it is the first time you write a case study, you will have four weeks to do something that normally takes months, and you will do it badly. So the work starts in Sprint 1 and every sprint ends with something a stranger can look at.

---

## 1. The rules of the track

1. **Every sprint ends with a case-study draft.** One page is enough. It is rewritten later; the point is that it exists.
2. **A public portfolio is live by week 12.** It can be small. It must be a real URL that opens on a phone.
3. **Every sprint has external eyes.** Someone who does not know the cohort and owes you nothing looks at your work and talks to you.
4. **Every sprint has a mock interview.** Different format each time, so the whole loop is rehearsed by week 24.
5. **The first screen carries the argument.** A hiring manager spends about ninety seconds on a portfolio. The first screen has to say who you are, what you design, and why they should keep reading.
6. **Nothing here is a placement guarantee.** The program can make you ready. It cannot create openings. See section 6.

---

## 2. The five tasks

Task IDs start with `JR`. Each is built in the week's Day 6 (cohort day). The writing and the reviews are committed to `students/UX{n}/portfolio/` in the current sprint folder; the portfolio site itself lives in your own repository, linked from your `portfolio/README.md`. The hours are on top of the normal week. They are the reason lab weeks run longer; see `01-How-The-Program-Works.md` section 13.

| ID | Week | Time | You produce | External input |
|---|---|---|---|---|
| **JR1** | 4 | 2 h | Positioning, platform decision, portfolio repo and asset checklist | None |
| **JR2** | 8 | 3 h | Case study 1 (Sprint 1) as a one-page draft, and a published skeleton site | 20-minute async review by a working designer |
| **JR3** | 12 | 3 h | Live portfolio with two case studies and an About page | 30-minute live portfolio review, plus **Mock interview 1: portfolio walk** |
| **JR4** | 16 | 3 h | Case study 3 (the design system), LinkedIn skeleton | **Mock interview 2: craft and critique** |
| **JR5** | 20 | 3 h | Capstone case study draft, target list of 20 companies | **Mock interview 3: behavioural and whiteboard** |

Sprint 6 then turns these drafts into the final three case studies, the polished site, the résumé, ten applications and the final loop. See `Design-Sprint-6/00-READ-FIRST.md`.

### JR1 — Position yourself (week 4)

**Learn first:** your own Sprint 1 work, and three portfolios of designers at the level you want.

**Method**
1. Write three sentences: *I design [what] for [whom]. The evidence is [one specific thing from the program]. I am looking for [kind of role].* No adjectives like "passionate" or "creative".
2. Write a one-page decision record for the platform: hand-coded, Framer, Webflow, Notion, GitHub Pages or similar. Score each on: accessibility of the output, load speed on a mid-range Android phone, ownership of your content, and the hours it will cost you. Pick one.
3. Create `students/UX{n}/portfolio/` with `positioning.md`, `platform-decision.md` and `assets-checklist.md`.
4. The assets checklist lists, per project, what you must export as you go: final PNGs at 2x, a 20-second prototype recording, the problem statement, one number, one mistake. Build the habit now so week 21 is not an archaeological dig.

**Done when**
- [ ] Positioning is three sentences and contains one specific piece of evidence
- [ ] The platform decision has scores and a reason, not a preference
- [ ] The assets checklist exists for Sprint 1

→ `students/UX{n}/portfolio/JR1-positioning.md`

### JR2 — Case study 1 and a live skeleton (week 8)

**Learn first:** `Design-Sprint-6/06-case-study-structure.md`, the whole file. You are using the structure early on purpose.

**Method**
1. Write the Sprint 1 (Aadhaar) case study as one page using the nine-part structure. Part 9, *what you got wrong and what you would do differently*, is mandatory. Cut every sentence that does not serve the argument.
2. Publish a skeleton site at a real URL with a home page, this case study, and a contact link. Put the URL in your README.
3. Send it for the async review. The reviewer answers three questions in 20 minutes: *What do you think this person does? Would you keep reading? What is the first thing you would cut?*
4. Commit the reviewer's answers verbatim, and your response in two lines.

**Done when**
- [ ] One-page case study with all nine parts
- [ ] A URL that opens on a phone
- [ ] The three reviewer answers, uncut
- [ ] One change you made because of them

→ `students/UX{n}/portfolio/JR2-case-study-1.md`

### JR3 — Live portfolio and Mock interview 1 (week 12)

**Learn first:** your JR2 review answers.

**Method**
1. Add the Sprint 3 flow (the consumer subscription showpiece, task C12.3) and an About page. Two case studies is enough; three weak ones are worse.
2. Run the portfolio against `Design-Sprint-6/03-week22.md` task B2.6 (accessibility and performance). Fix what fails now rather than in week 22.
3. **Live review, 30 minutes with an external designer.** Share your screen on a phone-sized window. They think aloud while they read.
4. **Mock interview 1, portfolio walk, 20 minutes.** Walk one case study in five minutes, then take questions. Record it.
5. Write down the three questions you answered worst.

**Done when**
- [ ] Portfolio is live, two case studies, About page, passes keyboard-only navigation
- [ ] Review notes committed
- [ ] Recording exists, and the three worst questions are written down

→ `students/UX{n}/portfolio/JR3-live-portfolio.md`

### JR4 — Case study 3 and Mock interview 2 (week 16)

**Method**
1. Write the design-system case study. This is the hardest to write because the output is invisible. The argument is not "I made components", it is "I made decisions about who may change what, and here is the one that went wrong".
2. Draft the LinkedIn headline and about section from your positioning.
3. **Mock interview 2, craft and critique, 45 minutes, external.** You are shown an unseen screen and asked to critique it; then you are asked to redesign one part live. Record it.
4. Commit the interviewer's scorecard.

**Done when**
- [ ] Case study 3 reads to someone who has not seen the system
- [ ] LinkedIn draft committed
- [ ] Scorecard and recording committed

→ `students/UX{n}/portfolio/JR4-case-study-3.md`

### JR5 — Capstone draft and Mock interview 3 (week 20)

**Method**
1. Write the capstone case study from the decision log. It must include the injected-failure post mortem and one result you cannot prove.
2. Build a target list of 20 companies and teams. Columns: company, role, why you, what you can show them, who you know. You will send applications to ten of them in Sprint 6.
3. **Mock interview 3, behavioural and whiteboard, 60 minutes, external.** Two behavioural questions, one 30-minute design whiteboard, one question about salary expectations.
4. Commit the scorecard.

**Done when**
- [ ] Capstone case study draft with the post mortem in it
- [ ] Target list of 20
- [ ] Scorecard and recording committed

→ `students/UX{n}/portfolio/JR5-capstone-draft.md`

---

## 3. Mock interview scorecard

The same four-point scale every time, used by the external interviewer. Full admin rubric is in the private admin material.

| Dimension | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| **Clarity** | Could not say what they did | Said it, but I had to dig | Clear in the first minute | Clear in ten seconds and the structure helped |
| **Reasoning** | Decisions with no reasons | Reasons, no alternatives | Reasons and rejected alternatives | Reasons, alternatives and what would change their mind |
| **Evidence** | Opinion | Some evidence, not defended | Evidence defended | Evidence defended, with its limits stated unprompted |
| **Honesty** | Everything went well | Mistakes mentioned | A mistake they learned from | A mistake that cost something, owned without defensiveness |
| **Presence** | Read from notes, froze, or defended | Uneven | Calm, engaged | Calm, curious, easy to talk to |

Each mock interview also records the question the designer answered worst. That list becomes the Sprint 6 practice list.

---

## 4. Who the external people are

The admin recruits them before Sprint 1 ends and keeps a bench of at least five.

| Requirement | Why |
|---|---|
| Working product designer, design manager, or someone who hires designers | They know what a real shortlist looks like |
| Has not seen the cohort's work | No benefit of the doubt |
| Owes the designers nothing | No kindness |
| Available for about three hours per sprint | One critique, one defense, one portfolio or mock session |

Rotate them. If a designer sits in front of the same external person twice in a row, the second session is worth much less.

---

## 5. The placement-readiness check (week 24)

The final loop in `Design-Sprint-6/05-week24.md` is scored by externals who have not seen the designer before. Each designer receives one of three honest outcomes:

| Outcome | Meaning | What happens next |
|---|---|---|
| **Ready** | Would put this person through to an interview round | Apply now. 90-day plan stays. |
| **Ready, with a named gap** | Would interview them, but one thing will cost them offers | The gap is named in writing. The 90-day plan is built around closing it. |
| **Not yet** | Portfolio or interview performance will not survive a real shortlist | Honest conversation, and a specific list: what to do, and in what order. |

"Not yet" is a result, not a failure. The program should say it plainly rather than let someone discover it after fifty rejections.

---

## 6. What the program can and cannot say

**It can say:** graduates leave with three portfolio-grade case studies, a live portfolio, three recorded mock interviews, a rehearsed answer bank, and an external assessment of where they stand.

**It cannot say:** graduates get jobs. Entry-level product design is a competitive market. Outcomes depend on the market, on location, on prior experience, and on how many applications a designer is willing to send and learn from.

**What the program does promise:** it will track outcomes and publish them. The admin contacts every graduate at 30, 90 and 180 days after week 24 and records: applications sent, interviews, offers, and what they would change. Those numbers go in the next cohort's welcome pack, whatever they are.

---

## 7. Optional: a live project

A designer who can secure a real client may substitute it for one of the Sprint 5 options, with the admin's written approval before week 17. Four conditions, all required:

1. A named contact who has agreed in writing
2. Five real users reachable in weeks 17 and 19
3. Something that can ship, even partially, inside four weeks
4. A number that exists before you start

A live project that cannot meet all four is a distraction. Choose a Sprint 5 option instead.

---

Next: `07-AI-In-Design.md`.
