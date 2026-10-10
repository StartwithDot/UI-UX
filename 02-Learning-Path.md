# 02 — Learning Path

The 24 weeks of learning, week by week. This is the answer to "what am I supposed to be learning right now".

Every week has a topic, the named primary sources, and the skill you should be able to demonstrate by the end of it. The week files inside each sprint folder break this down to the day. Current standards and tools for each area are in `09-Modern-Practice-Map.md`.

---

## How to use this file

- **At the start of every week:** read your row. Then open the week file for the details.
- **Nothing is assigned that is not used.** If a book is in a row, a task that week needs it.
- **Reading ahead is fine.** Reading instead of doing is not.
- **Labs.** Fourteen short labs sit on the week's Day 6, in three families: `L-AI` (AI in design, `07-AI-In-Design.md`), `L-PR` (prototyping and responsive, `08-Prototyping-And-Responsive.md`) and `JR` (job readiness, `06-Job-Readiness-Track.md`). They appear in the tables below.

Primary sources are listed by short name. Full details, cost, and where to get them are in `03-Books-And-Resources.md`.

---

## Sprint 1 · Weeks 1 to 4 · Visual craft and one complete flow
*Project: the Aadhaar address update flow, for a state government digital services unit.*

| Week | Topic | Primary source | You can do this by the end of the week |
|---|---|---|---|
| 1 | **Frame.** Reframe a vague brief; hierarchy, type, spacing and colour foundations | Refactoring UI ch. 1–6 · Practical Typography · NNGroup heuristics · WCAG 2.2 AA · Figma Learn: Auto Layout, Components | Turn a bad brief into a problem statement; audit a live service; build a type scale, spacing scale and colour ramp and say why each step exists |
| 2 | **Build.** Flows, forms, labels, validation, error messages | Form Design Patterns ch. 1–3 · NNGroup on error messages · Polaris content guidance · Figma Learn: Variants | Draw a flow with every failure path; design a form where every field has a label, hint and validation rule; write every error message · **L-AI1** |
| 3 | **Test and fix.** Every state a screen can be in; usability testing | Refactoring UI ch. 8 (empty states) · Material 3 and Polaris state guidance · Rocket Surgery Made Easy ch. 1–4 | Produce a states matrix; test with three people without leading them; trace every change to a finding; write a post mortem on a change you did not choose · **L-PR1** |
| 4 | **Ship and defend.** Accessibility, high fidelity, handoff | WCAG 2.2 AA · web.dev Learn Accessibility · Deque University · Refactoring UI ch. 6–8 · Norman ch. 1–4 | Run a real accessibility gate with evidence on every line; use a screen reader on your own design; write a handoff spec; defend four weeks of decisions · **JR1** |

**Fundamentals spine:** Gestalt principles · visual hierarchy and whitespace · cognitive load and progressive disclosure · affordances, signifiers and mental models.

---

## Sprint 2 · Weeks 5 to 8 · Research and problem framing
*Project: a skill scheme with a 38% drop inside its enrolment form; the client has already diagnosed "motivation".*

| Week | Topic | Primary source | You can do this by the end of the week |
|---|---|---|---|
| 5 | **Plan.** What research is for; assumptions and risk; ethics and consent | Just Enough Research (whole book) · Interviewing Users ch. 1 · `06-research-ethics.md` | Write a research plan that can fail, with a ranked assumption list; recruit five real participants |
| 6 | **Talk.** Interviewing without leading | Interviewing Users ch. 2–5 · Just Enough Research on synthesis · NNGroup on affinity diagramming | Run a 45-minute interview, critique your own transcript, turn five conversations into patterns · **L-AI2** |
| 7 | **Test.** Usability testing with no budget | Rocket Surgery Made Easy ch. 1–6 · Don't Make Me Think · NNGroup severity ratings | Run a moderated study on five people; severity-rate every finding; absorb a research-invalidating constraint |
| 8 | **Synthesise.** Findings, confidence, contradiction | Just Enough Research on reporting · NNGroup on sample size and personas · journey mapping and service blueprints · Norman on human error | Present findings with honest confidence levels; trace every design change to a finding; defend a sample of five · **JR2** |

**Fundamentals spine:** memory, attention and cognitive load · mental models and the gulf of evaluation · bias · the psychology of decision-making.

---

## Sprint 3 · Weeks 9 to 12 · Interaction, motion, metrics and ethics
*Project: Sutra, a language-learning app, and its subscription flow. The consumer, visually ambitious project, and your portfolio's front page.*

| Week | Topic | Primary source | You can do this by the end of the week |
|---|---|---|---|
| 9 | **Transitions.** State machines, feedback, latency; activation and funnels | About Face (postures, undo) · statecharts.dev · NNGroup on response times · Google HEART paper · Lean Analytics (funnels) | Draw a state machine with every guard; specify feedback by real latency; define activation and a metric set with a guardrail · **L-AI3** |
| 10 | **Motion.** Animation that communicates | Designing Interface Animation (Val Head) · Material motion · WCAG 2.3.3 | Choose duration and easing for a reason; delete decoration; build a reduced-motion version that is not just "instant"; write a motion spec · **L-PR2** |
| 11 | **Dark patterns.** Persuasion versus manipulation | deceptive.design · CMA, FTC and India CCPA guidance · Ruined by Design · Fogg behaviour model | Name the mechanism behind a dark pattern; build one and account for its cost; make the business case for the honest version with an experiment design; handle a business demand |
| 12 | **Ethics and ship.** Where your line is | ACM Code of Ethics · `06-ethics-position.md` · WCAG for interactive components · ARIA APG | Write an ethics position and a refusal a manager could receive; ship an accessible, specified flow with instrumentation; produce the showpiece · **JR3** |

**Fundamentals spine:** feedback loops and the two gulfs · perception of time and change blindness · persuasion, nudging and choice architecture · ethics in practice.

---

## Sprint 4 · Weeks 13 to 16 · Design systems, scale and governance
*Project: a health tech company with three products on three frameworks and two brands.*

| Week | Topic | Primary source | You can do this by the end of the week |
|---|---|---|---|
| 13 | **Tokens.** Audit; three-layer architecture; theming | Design Systems (Kholmatova) ch. 1–3 · `06-token-architecture.md` · Design Tokens spec 2025.10 · Style Dictionary and Tokens Studio docs · Material 3 and Polaris token docs · Expressive Design Systems | Cost the divergence; build a primitive, semantic and component token set that themes three products without redesign; export it in the standard format · **L-PR3** |
| 14 | **Components.** APIs, variants, slots, documentation | Atomic Design · Design Systems ch. 4–5 · Radix, React Aria or Headless UI docs (composition) · ARIA APG · Storybook docs | Design a component API and defend every property; write documentation a stranger can build from; compose without impossible combinations · **L-AI4** |
| 15 | **Governance.** Who decides; rejection; deprecation | Design Systems ch. 6–7 · Polaris, Carbon and GOV.UK contribution guides · semver | Write a contribution model with rejection criteria; reject a contribution kindly; deprecate something people use |
| 16 | **Adoption.** Measurement; migration; being ignored | Design Systems ch. 8 · Sparkbox and Zeroheight articles on adoption · semver · web.dev Learn HTML (for L-PR3 and L-AI4) | Measure adoption with something better than a feeling; diagnose a fork; write a migration guide someone completes · **JR4** |

**Fundamentals spine:** abstraction and indirection · Conway's law · APIs as contracts · standardisation versus autonomy.

---

## Sprint 5 · Weeks 17 to 20 · The capstone
*Project: your choice of four (public health appointments, gig worker earnings and disputes, school-to-work, loan underwriting console with an AI score), or your own, approved.*

| Week | Topic | Primary source | You can do this by the end of the week |
|---|---|---|---|
| 17 | **Frame.** Scope it yourself; research; evidence gate | You choose and justify · Google People + AI Guidebook and Microsoft HAX (for L-AI5) | Write your own scoped task list; run research without a template; pass an evidence gate · **L-AI5** |
| 18 | **Design.** The whole flow to the standard in a week | You choose · current Apple HIG or Material 3 for your platform | Hold Sprint 1 to 4 standards unprompted; pass the craft gate · **L-PR4** |
| 19 | **Test.** Real users; iterate; absorb the injection | You choose | Change a design because of evidence and show the trace; absorb a severe late constraint; review your own work for the ethical problem you created |
| 20 | **Ship.** Spec, present, defend all twenty weeks | — | Ship a complete, specified, accessible design; present to a stranger; defend anything from week 1 · **JR5** |

**Fundamentals spine:** self-directed. Present the concept the capstone forced you to learn.

---

## Sprint 6 · Weeks 21 to 24 · Portfolio, interview, and getting hired
*The project is the evidence that you can do the job.*

| Week | Topic | Primary source | You can do this by the end of the week |
|---|---|---|---|
| 21 | **Case studies.** Three arguments from twenty weeks | `06-case-study-structure.md` · NNGroup on how users read the web · five real case studies | Choose three on evidence; write them to a structure; include a failure; cut by a third |
| 22 | **Portfolio.** Build it, get it reviewed by a stranger, fix it | Portfolio patterns · résumé conventions · axe and Lighthouse | Ship a live portfolio that passes its own accessibility check; take external criticism without arguing |
| 23 | **Interview craft.** Talking about the work | `07-interview-question-bank.md` · whiteboard method | Walk a case study in five and in twenty minutes; solve a design problem on a whiteboard; critique without being soft or unpleasant |
| 24 | **Market.** Applications, a full loop, and a plan | Application strategy | Send ten real applications; complete a mock loop; say honestly what you are still weak at; leave with a 90-day plan |

**Fundamentals spine:** how hiring managers read portfolios · how design interviews are scored · teaching the hardest concept.

---

## The learning summary

After each LEARN block, ten minutes:

```markdown
# Week {n}, Day {n} — Learning summary

## What I read or watched
- {source}, {chapter or section}, {pages or duration}

## Three things I learned
1.
2.
3.

## One thing I did not understand
## Where I will use this
```

Commit to `students/UX{n}/week{n}/session{n}-learning.md`.

**Why this matters more than it looks.** At the end of the sprint you sit a defense where you are asked what you know. The only reliable preparation is 20 of these files in your own words. Notes you did not write are notes you do not have.

---

## The weekly why session

Ninety minutes at the close of each week. One designer presents the week's fundamentals topic to the other four, using the cohort's own work as the examples, never textbook diagrams.

Rotates so everyone presents four to five times across the program. Committed to `fundamentals/why-sessions/week{nn}-{topic}.md`.

**Presenting is the test.** You find out what you actually understand at the moment someone asks "why" and you have to answer without the slide.

---

## The weekly teardown

One product surface, pulled apart in writing. Assigned by the admin each week.

Format, every time:

| Section | Content |
|---|---|
| The flaw | What is wrong, specifically, with a screenshot |
| The principle | Which named principle or guideline it violates |
| The user cost | What it costs a real person, in their words not yours |
| The fix | What you would do instead |
| The cost of the fix | What it takes to build. If it is expensive, say so. |

Committed to `fundamentals/teardowns/{nn}-{subject}.md`.

Subjects are drawn from products with real constraints: government service portals, bank apps, insurance claims, airline booking, hospital appointments, food delivery checkout, payment confirmation, enterprise consoles, AI assistants, and subscription cancellation flows. Cancellation and consent flows are assigned on purpose, because that is where dark patterns live.

---

## The drill

Ten minutes per session, all 24 weeks.

Pick one component from any real product. Rebuild it from memory in Figma. Then open the real one and compare. Log one line.

```
Session 14 — Razorpay payment method selector. Missed that the selected state
uses a border plus a check, not just a fill. Overestimated the padding.
```

Committed to `fundamentals/drills/UX{n}-log.md`, appended as you go.

Ten minutes × 120 days is 20 hours of pure visual observation. Nothing else in the program builds an eye faster.

---

Next: `03-Books-And-Resources.md`.
