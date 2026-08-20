# Sprint 1 — Read First

**Weeks 1 to 4 · Visual craft and one complete flow**

---

## What you are building

You are rebuilding the **Aadhaar address update flow** for a state government digital services unit. One flow, done completely: every screen, every state, working for a 52-year-old shop owner on a cheap Android phone with a connection that drops, and passing a real accessibility check.

Not a concept. Not three pretty screens. A complete, defensible flow.

---

## Read these in this order

| # | File | When |
|---|---|---|
| 1 | `00-READ-FIRST.md` | now |
| 2 | `01-project-brief.md` | now, before the start of the week |
| 3 | `02-week1.md` | when week 1 opens |
| 4 | `03-week2.md` | when week 2 opens |
| 5 | `04-week3.md` | when week 3 opens |
| 6 | `05-week4.md` | when week 4 opens |

Reference, open when a task points at them:
- `06-accessibility-gate.md` — the checklist that decides whether you shipped
- `07-critique-guide.md` — how the week's critique works and what a valid comment is
- `08-glossary.md` — every term used in this sprint, defined plainly

---

## The four weeks

| Week | Called | You learn | You produce |
|---|---|---|---|
| **1** | Frame | Hierarchy, type scales, spacing, colour ramps | A reframed brief, an audit of the live service, and your visual foundations |
| **2** | Build | Forms, validation, error messages, microcopy | The full flow at mid fidelity with every error message written |
| **3** | Test and fix | Every state a screen can be in | A usability test on 3 people, a states matrix, and fixes traced to findings |
| **4** | Ship and defend | Accessibility: WCAG AA, keyboard, screen readers | High fidelity flow, a passed accessibility gate, a handoff spec, and a defense |

---

## Every task

```
STUDY    LEARN     1 to 2 h    named source, then a committed summary
BUILD  DO        1 to 2 h    a task built on that study time's reading
```

Week files give you the exact chapter, the exact page range, the exact video. Never "read about typography".

Every task in this sprint has four parts:

| Part | What it gives you |
|---|---|
| **Learn first** | Which part of the study time's reading this uses |
| **Method** | Numbered steps. The procedure, not the answer. |
| **Worked example** | A correct answer for a different case, so you know the shape |
| **Done when** | The checklist that says you can stop |

---

## What you commit

```
students/UX{n}/week1/
  session1-learning.md          ← one per session
  session2-learning.md
  session3-learning.md
  session4-learning.md
  session5-learning.md
  P1-1-brief-questions.md   ← task outputs, task ID first
  C1-1-type-scale.md
  ...
```

One task, one file, one commit. Commit message starts with the task ID:

```
git commit -m "C1.1 type scale with Devanagari test"
```

---

## The shared design system

`system/` is one design system that the whole cohort depends on, and it is the same system for all 24 weeks. In week 1 it is a type scale, a spacing scale, and a colour ramp. By Sprint 4 it is a real multi-brand token architecture.

Because it is shared, mistakes there block five people. It gets stricter review than your own folder.

The **system owner** for the week merges contributions. That role rotates.

---

## What ships at the end of week 4

- The full flow, high fidelity, at 390px and 1440px
- Every state designed, not described
- Every error message written
- A completed accessibility gate with evidence on every line
- A handoff spec an engineer could build from
- One decision record for the choice a department official would question
- One post mortem on the mid-sprint failure
- 20 learning summaries
- A passed defense

---

## What will be hard, and it is meant to be

**The brief is deliberately bad.** "Make it so people stop coming to the counter." Week 1 is about turning it into something answerable. If you start designing screens on the first task you will design the wrong thing.

**You cannot invent users.** Three real users are described in the brief, each with a different failure mode. You design for all three, not the easiest one.

**Something will break in week 3.** A constraint will change. You will not know which one until it lands. You write a post mortem about what it cost you.

**The accessibility gate does not move.** Pretty work that fails the gate is not done. You will run a screen reader over your own flow, and the first time is unpleasant for everyone.

---

## Before the start of the week

- [ ] Read `01-project-brief.md`
- [ ] Have Refactoring UI downloaded
- [ ] Figma set up, four Learn lessons done (see root `04-Tools-Setup.md`)
- [ ] axe DevTools installed
- [ ] Repo forked and cloned
- [ ] Use the live service at `myaadhaar.uidai.gov.in` once, on your phone, with your own Aadhaar. Do not use anyone else's.

Then open `02-week1.md`.
