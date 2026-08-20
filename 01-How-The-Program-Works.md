# 01 — How The Program Works

Read after `00-START-HERE.md`. This is the operating manual: your week, your roles, what blocks your work from being called done, and how you are assessed.

---

## 1. The shape of everything

```
24 weeks
 └── 6 sprints × 4 weeks each
      └── each sprint: 1 client project, 1 defense at the end
           └── each week: 5 learn-then-do days + critique + session
                └── each task: LEARN block, then DO block
```

Nothing changes about this rhythm across 24 weeks. Only the content gets harder.

---

## 2. Your day

Two blocks of work per study session, repeated through the week.

### The LEARN block, 1 to 2 hours

Your week file (`02-week1.md` and so on) names exactly what to read or watch. Chapter numbers. Page ranges. Video titles with durations. Never "read about typography".

At the end of the block, write a summary. It is short and it has a fixed shape:

```markdown
# Week 1, session 1 — Learning summary

## What I read or watched
- Refactoring UI, "Hierarchy is Everything", pp. 27–52
- Figma Learn: Auto Layout, 18 min

## Three things I learned
1. ...
2. ...
3. ...

## One thing I did not understand
...

## Where I will use this
...
```

Commit it to `students/UX{n}/week{n}/session{n}-learning.md`. Ten minutes. Not optional.

### The DO block, 1 to 2 hours

The task that uses what you just learned. Every task in this program gives you four things:

| Part | What it means |
|---|---|
| **Learn first** | Which part of this week's reading this task is built on |
| **Method** | The numbered steps. Not the answer, but the procedure. |
| **Worked example** | What a correct answer looks like, for a different case |
| **Done when** | The checklist that says you can stop |

If a task ever feels impossible, you skipped the LEARN block. Go back to it.

---

## 3. Your week

```
WEEK OPENS ──────────► WORK ──────────► CRITIQUE ──────► GATE ──────► WEEK CLOSES
kickoff 15m            learn + do       90 min           check        session 90 min
                       commit as        in-progress      what you     why session
                       you finish       work shown       call done    + teardown
```

**Kickoff, 15 minutes.** Admin posts the week goal, names who holds which role, and says which gate applies. You read the week file end to end before you start.

**Work.** Learn, do, commit. Open a pull request as each task finishes, not in one batch at the end.

**Critique, 90 minutes.** Each designer presents in-progress work for 12 minutes. Run against the rubric in the sprint's `07-critique-guide.md`. The critique lead files the log straight after.

**Gate.** Address critique feedback, merge, run the gate on anything you are calling done.

**Week close session, 90 minutes.** One designer presents the week's "why session". One teardown is discussed. No new sprint work happens in this session.


---

## 4. Two rotating roles

Five designers. Two roles rotate every week, so across a 4-week sprint everyone holds each role at least once.

| Role | Who | Duty |
|---|---|---|
| **Critique lead** | 1 person, weekly | Runs the week's critique against the rubric. Reviews every peer pull request. Files the critique log. |
| **System owner** | 1 person, weekly | Owns `system/` that week. Merges component contributions, keeps tokens and docs current, writes the changelog. |
| **Builder** | The other 3 | Sprint tasks plus one contribution to `system/` or `delivery/` |

The rotation is logged in each sprint's `students/` area by the admin.

**Why these two roles exist.** Critique lead teaches you to name the user cost of a flaw instead of saying you do not like it, which is exactly what a design interview tests. System owner teaches you contribution governance and how to say no to a component, which is what design systems teams hire for.

Neither role is a promotion. Neither role gets to overrule anyone.

---

## 5. The four tracks

Every task has a letter. The letter tells you which muscle it trains.

| Letter | Track | Covers |
|---|---|---|
| **C** | Craft and Interface | Typography, colour, layout, hierarchy, states, motion, microcopy, prototyping |
| **R** | Research and Evidence | Interviews, usability testing, synthesis, analytics, measurement |
| **P** | Product and Business | Framing, metrics, scoping, IA, competitive analysis, stakeholders |
| **S** | Systems and Technical | Tokens, components, documentation, governance, HTML and CSS literacy, git, handoff |
| **F** | Fundamentals | The learning spine: why sessions, teardowns, explainers, drills |
| **X** | Injected failure | The thing that goes wrong mid-sprint |

Task IDs look like `C1.1`, `R2.3`, `S4.2`. The number after the letter is the week-station, the number after the dot is the task within it.

All four tracks run in every sprint so no skill goes cold. Sprints differ by which track carries the most weight.

---

## 6. The three gates

A gate is a checklist, not an opinion. Work that fails a gate is not done, no matter how it looks.

### Gate 1 — States

Every flow must show: default, empty, loading, partial, error, success, offline, permission denied, zero results, first run, and destructive confirm where it applies.

A missing state is a missing design, not a detail.

### Gate 2 — Accessibility

Run on the primary flow of everything you ship. Full checklist in each sprint's `06-accessibility-gate.md`. The short version:

- Complete the task with keyboard only, no mouse
- Visible focus on every interactive element
- Contrast 4.5:1 for body text, 3:1 for large text and UI components
- Target size at least 24 × 24 px
- Every icon button has an accessible name
- Errors say what happened and what to do, and name the field
- Screen reader pass on the primary flow
- Reduced motion alternative for anything over 200ms
- Colour is never the only thing carrying meaning

### Gate 3 — Evidence

Any claim about users needs a source. Valid sources:

- A usability test, with the tasks and results attached
- A number, with the query or method stated
- A documented convention from a named design system
- A named heuristic, with the user cost spelled out

"Users prefer this" with nothing attached fails the gate. Every time.

---

## 7. How you are assessed

### Every task
Learning summary committed. Task committed.

### Every week
Critique log filed. Two peer reviews given, each with at least one substantive comment. The week-close artefact committed.

### Week 3 of each sprint — Whiteboard why
15 minutes. No notes, no files open. Draw your current flow from memory and answer three questions pulled at random from the sprint question bank.

"Needs work" is a normal result and just schedules a re-run in week 4.

### Week 4 of each sprint — The defense
55 minutes per designer, six parts.

| Part | Time | What is being tested |
|---|---|---|
| Flow walk from your own diagram | 10 min | Can you hold the whole thing in your head |
| Terminology and tradeoff | 10 min | Vocabulary with the tradeoff attached, not recall |
| Failure story | 10 min | Judgement and honesty about what went wrong |
| Business framing | 5 min | Who reads this and what decision changes |
| Evidence defense | 10 min | Defend your test, your sample, your metric |
| Alternative design | 10 min | Redo it with one constraint changed |

Constraint cards used in the last part: no colour · screen reader only · 2G network · one third the budget · ten times the data · offline first · one hand on a phone in sunlight · regulated industry with audit requirements.

**To pass you need all four of these:**
1. Correct vocabulary
2. One piece of evidence you can defend
3. One coherent alternative design
4. One honest "I do not know yet, and here is how I would find out"

The fourth is deliberate. A designer who cannot say that is guessing and hiding it.

### Across the program — your ledger
The admin keeps a running record per designer: concepts owned, teardowns written, tests run, components shipped, gates cleared, defenses passed, roles held. By Sprint 6 that record is your portfolio narrative and your interview story bank.

---

## 8. Where work lives

Each sprint repository has four zones.

| Zone | What it is | Review level |
|---|---|---|
| `students/UX{n}/` | Your own practice. Mistakes cost nothing. | Peer review |
| `system/` | The one shared design system. Everyone depends on it. | Strict. System owner plus admin. |
| `delivery/` | Shared final outputs for the client. | Strict. |
| `fundamentals/` | Learning summaries, why sessions, teardowns, explainers. | Filed, spot checked |

### Figma and git together

Figma cannot be diffed, so git holds the reasoning and Figma holds the canvas.

| Thing | Source of truth |
|---|---|
| Screens and components | Figma. Commit the link plus an exported PNG of the final state. |
| Tokens | Git. `system/tokens/*.json` |
| Flows and diagrams | Git. Mermaid inside Markdown. |
| Decisions and rationale | Git. Markdown, always. |
| Specs and annotations | Git, Markdown, next to the Figma link |

File naming in Figma: `SPRINT-1 Practice UX3`, `SPRINT-1 System`, `SPRINT-1 Delivery`.

---

## 9. The git loop

```bash
git checkout main
git fetch upstream
git merge upstream/main            # sync before you start, every time

git checkout -b UX3-C1-1           # one branch per task

# ... do the work ...

git add students/UX3/week1/C1-1-type-scale.md
git commit -m "C1.1 type scale with Devanagari test"
git push origin UX3-C1-1

# open a pull request against upstream main
```

One task, one file, one commit, message starting with the task ID.

---

## 10. When things go wrong

| Situation | What happens |
|---|---|
| You open no pull request for a week | Admin messages you before the week closes. The question is what is blocking you, not why you are behind. |
| Critique becomes personal taste | Session stops, the rubric is read out loud, critique restarts. Every comment names a principle and a user cost. |
| The shared system is blocked | Admin pairs with the system owner straight away. A blocked system blocks five people. |
| The cohort splits on a shared decision | New work stops. One session to decide. Decision recorded. Everyone released together. |
| Everyone designs the same thing | Each designer gets a different constraint card for one round. Convergence in week 2 usually means nobody explored. |
| You want to skip the accessibility gate to ship prettier work | The gate does not move. You run a screen reader over your own flow once and the argument ends. |
| Research recruiting fails | That is sprint content, not an accident. Switch method, reduce n, and state the limitation in writing. |

---

## 11. Buffer weeks

Two weeks sit outside the 24: one after Sprint 3, one after Sprint 6. They exist for catch-up and for defense re-runs. Using one is normal.

---

## 12. What must be true before a sprint is called done

- Every designer cleared the accessibility gate on their primary flow
- Every claim traces to a source
- The shared system builds and its documentation matches what is in it
- Every designer held one rotating role
- Every designer passed the defense or has a scheduled re-run
- One post mortem per designer is committed
- Every learning summary for the sprint is committed

Next: `02-Learning-Path.md`.
