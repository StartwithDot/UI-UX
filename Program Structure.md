# Program Structure

How this cohort operates. 5 designers, 6 sprints of 4 weeks, 24 weeks total.

---

## 1. Why design needs a different structure from engineering

The data engineering program works because code is objectively reviewable. A query either returns the right row count or it does not. Design has no equivalent, so three substitutions are made:

| Engineering mechanism | Design equivalent | Why |
|---|---|---|
| CI passes or fails | Accessibility and states gate, run as a checklist | Objective, binary, blocks sign off the same way |
| Code review by review lead | Structured critique by critique lead, against a written rubric | Taste comments are unreviewable, rubric comments are |
| One shared pipeline in `platform/` | One shared design system in `system/` | Same purpose: one real artefact the whole cohort depends on |
| Row count reconciliation | Usability test result and metric movement | Both are the independent source that says whether the work is right |

With 5 people there is no room for spectators. Every designer works every week, holds a rotating position twice per sprint, and reviews two peers per week.

---

## 2. Cohort and positions

5 designers, coded **UX1 to UX5**.

### Positions, rotated weekly

| Position | Count | Duty | Works in |
|---|---|---|---|
| Critique lead | 1 | Runs Thursday critique, reviews all peer pull requests against the rubric, files the critique log | Reviews, no system merges |
| System owner | 1 | Owns `system/` that week. Merges component contributions, keeps tokens and docs current, maintains the changelog | `system/` and `delivery/` |
| Builder | 3 | Sprint tasks in own folder plus one contribution to `system/` or `delivery/` | `students/UX{n}/week{n}/` |
| Core admin | 1 to 2, not rotated | Final approval on `system/` and `delivery/`, runs sprint defense, holds the admin repo | Everywhere |

Rotation over a 4 week sprint with 5 people: each designer is critique lead once and system owner once, with one designer doubling per sprint. The doubling designer rotates by sprint so the load is even across 24 weeks. Log lives in `docs/rotation-log.md` in each sprint repo.

### What each position teaches

Critique lead learns to name the user cost of a flaw instead of stating a preference, which is the exact skill tested in the app critique interview round. System owner learns contribution governance, versioning, and saying no to a component, which is what design systems roles hire for. Neither is an authority position.

---

## 3. Repository zones

Each public sprint repo has four zones.

```
Design-Sprint-N/
  README.md                    sprint brief summary and how to work
  docs/
    project-brief.md           the client story, users, constraints
    task-list.md               every task in the sprint, station by station
    student-guide.md           daily working rules, file naming, PR flow
    critique-guide.md          how critique is run and what a valid comment is
    accessibility-gate.md      the checklist that blocks sign off
    rotation-log.md            who held which position, which week
    tools-setup.md             tool accounts, plugins, file conventions
  students/
    UX1/ ... UX5/
      week1/ week2/ week3/ week4/
        problem_statement.md   that week's tasks, pulled from task-list
  system/                      the one shared design system
    tokens/                    JSON token sets
    components/                component specs and docs
    docs/                      usage, governance, changelog
    code/                      implemented components, Storybook
  delivery/                    the shared outputs
    research/                  plans, guides, findings, repository
    design/                    flows, IA, wireframes, high fidelity
    prototype/                 prototype links and interaction specs
    handoff/                   specs, annotations, engineering notes
    presentation/              stakeholder deck and script
  fundamentals/                the spine, runs under every sprint
    why-sessions/
    teardowns/
    explainers/
    adr/
    drills/
```

Individual folders are for practice. Mistakes cost nothing. The `system/` and `delivery/` zones are the one real shared build. Mistakes there block everyone, so they carry stricter review.

### Figma file convention

Figma is not versionable in git, so the repo holds the decision record and the link, never the source of truth alone.

| Artefact | Lives in Figma | Lives in git |
|---|---|---|
| Screens and components | Yes, source of truth | Link plus exported PNG of the final state |
| Tokens | Figma variables | `system/tokens/*.json`, git is source of truth |
| Flows and IA | FigJam optional | Mermaid diagram in Markdown, git is source of truth |
| Decisions and rationale | No | Markdown, always |
| Specs and annotations | Dev mode | Markdown spec next to the link |

One Figma team, one file per zone: `SPRINT-N Practice UX{n}`, `SPRINT-N System`, `SPRINT-N Delivery`. Branching is used for system contributions.

---

## 4. The sprint shape

Four weeks. Same rhythm every sprint so nobody has to ask what happens next.

```
WEEK 1                WEEK 2               WEEK 3               WEEK 4
Frame                 Build                Test and fix         Ship and defend
brief read            core work            usability test        final polish
constraints listed    peer critique        whiteboard why        accessibility gate
tasks started         mid build review     injected failure      handoff written
                                           post mortem           defense
```

### Week inside the sprint

```
MON            TUE ─────── WED            THU              FRI              SAT
kickoff        build                      critique         fix and merge    spine
15 min         individual + system        90 min group      PRs land        why session
week goal      PRs opened continuously    rubric based     gate checked     teardown
gate reminder                             log filed        rotation ends    drill review
```

**Monday kickoff, 15 minutes.** Admin posts the week goal, names the critique lead and system owner, states which gate applies this week.

**Tuesday to Wednesday, build.** Designers work in their own folders. System owner works in `system/`. Pull requests open as work completes, not in a Friday dump.

**Thursday critique, 90 minutes.** Every designer presents in progress work for 12 minutes. Critique lead runs it against the rubric in `docs/critique-guide.md`. The log is committed the same day.

**Friday merge and gate.** Critique feedback addressed, PRs merged, accessibility gate run on anything claiming done.

**Saturday spine, 90 minutes.** One why session presented by a rotating designer, one teardown discussed, drill streaks reviewed. Mentor interrogates, does not lecture.

---

## 5. The four tracks

Every sprint task belongs to one of four tracks. Tracks run in parallel across all 24 weeks so no skill goes cold. Task IDs carry the track letter.

| Track | ID prefix | Covers |
|---|---|---|
| Craft and Interface | **C** | Typography, colour, layout, hierarchy, states, motion, microcopy, prototyping |
| Research and Evidence | **R** | Interviews, usability testing, synthesis, analytics, experiments, measurement |
| Product and Business | **P** | Framing, metrics, prioritisation, scoping, IA, competitive analysis, stakeholder work |
| Systems and Technical | **S** | Tokens, components, documentation, governance, HTML and CSS literacy, git, handoff, performance |

Accessibility is not a track. It is a gate applied to every station, because a track can be skipped and a gate cannot.

AI product design enters as content inside the C and P tracks from Sprint 5, not as a fifth track, so it is treated as normal product work rather than a novelty.

### Station numbering

Stations are groups of related tasks: `C3` is the third Craft station. Tasks are `C3.2`. Milestone stations are marked `[MILESTONE]` and the whole cohort must clear them before anyone moves far ahead, because later stations depend on the shared decision.

---

## 6. Gates

Three gates. All three are checklists, not opinions. A deliverable that fails a gate is not done, regardless of how it looks.

### 6.1 States gate

Every flow ships: default, empty, loading, partial, error, success, offline, permission denied, zero results, first run, and the destructive confirm where relevant. Missing state means not done.

### 6.2 Accessibility gate

Run on the primary flow of every shipped deliverable. Full checklist in `docs/accessibility-gate.md`.

- Keyboard only pass, complete task without a mouse
- Visible focus on every interactive element, focus never obscured
- Contrast: 4.5:1 body text, 3:1 large text and UI components
- Target size 24 by 24 minimum with spacing exception noted
- Headings structure and landmarks present
- Every icon button has an accessible name
- Error messages identify the field and the fix, not just that something failed
- Screen reader pass on the primary flow, VoiceOver or NVDA
- Reduced motion alternative for any animation over 200ms
- Colour is never the only carrier of meaning

### 6.3 Evidence gate

Any claim about users needs a source. Options: a usability test with tasks and results, an analytics number with the query stated, a documented convention from a named design system, or a heuristic named with the user cost spelled out. "Users prefer" with no source fails.

---

## 7. Assessment

### Weekly
Critique log filed, two peer reviews given with at least one substantive comment each, spine artefact committed. Rubber stamp approvals are named in the log.

### Mid sprint, week 3: whiteboard why
15 minutes, no notes, no file open. Draw the current flow from memory and answer three questions drawn at random from the sprint question bank. Needs work is normal and schedules a re-run in week 4.

### Sprint end: the defense
6 parts, 55 minutes per designer.

| Part | Time | What is tested |
|---|---|---|
| Flow walk from own diagram | 10 min | Can they hold the whole system in their head |
| Terminology and tradeoff | 10 min | Vocabulary with the tradeoff attached, not recall |
| Failure story with evidence | 10 min | Debugging judgement, honesty |
| Business framing | 5 min | Who reads this, what decision changes |
| Evidence defense | 10 min | Defend the test, the sample, the metric |
| Alternative design | 10 min | Redo it with one constraint changed |

Constraint cards for part 6: no colour, screen reader only, 2G network, one third the engineering budget, ten times the data volume, offline first, one hand on a phone in sunlight, regulated industry with audit requirements.

**Pass bar.** Correct vocabulary, plus one defended piece of evidence, plus one coherent alternative design, plus one honest "I do not know yet, here is how I would find out". The last item is deliberate.

### Program level: the ledger
`ledger/UX{n}.md` in the admin repo, appended every sprint. Concepts owned, teardowns authored, tests run, components shipped, gates cleared, defenses passed, positions held. By Sprint 6 the ledger is the portfolio narrative and the interview story bank.

---

## 8. Tool budget

Two new tools per sprint maximum. Everything else is reuse or one session with a written verdict. Reason: tool count is the easiest thing to inflate and the least valuable thing to own.

| Sprint | New tools | Reused |
|---|---|---|
| 1 | Figma, Stark or axe DevTools | none yet |
| 2 | Maze or Lyssna, Optimal Workshop | Figma |
| 3 | FigJam, ProtoPie or Figma advanced prototyping | Figma, Maze |
| 4 | Tokens Studio, Storybook with git | Figma, prototyping |
| 5 | PostHog, one AI product to study as material | everything prior |
| 6 | Microsoft Clarity, portfolio host of choice | everything prior |

Photoshop, Illustrator, After Effects, Blender, and Spline are covered in `Learning Resources.md` under adjacent tools with an honest statement of when they matter. None are required to clear a product design loop.

---

## 9. When the flow breaks

| Situation | What the admin does |
|---|---|
| A designer opens no pull request for a week | Direct message before critique. Ask what is blocking, not why they are behind. Most silences are a stuck decision, not laziness. |
| Critique is turning into taste comments | Stop the session, re-read the rubric out loud, restart. Every comment must name the principle and the user cost. |
| The shared system is blocked | Core admin pairs with the system owner same day. A blocked system blocks 5 people, which is a different cost from a blocked individual. |
| The cohort splits across a milestone | Stop new station work. One shared session to make the pending decision, record it in the admin decision log, release everyone together. |
| Everyone converges on the same visual solution | Force divergence: assign each designer a different constraint card for one round. Convergence at week 2 usually means nobody explored. |
| A designer wants to skip the accessibility gate to ship prettier work | The gate does not move. Show them a screen reader pass on their own flow once and the argument ends. |
| Research recruiting fails | Recruiting is sprint content, not an accident. Switch to intercept recruiting, guerrilla testing, or a smaller n with the limitation stated in writing. |

---

## 10. Calendar

24 weeks, 6 sprints of 4 weeks. Roughly 12 to 15 hours per week: 8 to 10 on the sprint project, 4 to 5 on the fundamentals spine.

Two buffer weeks are held outside the count, one after Sprint 3 and one after Sprint 6, for catch up and for defense re-runs. A cohort of 5 that never uses a buffer week is probably not being pushed hard enough.

---

## 11. What must be true before a sprint is called done

- Every designer cleared the accessibility gate on their primary flow
- Every claim in every deliverable traces to a source
- The shared system builds and its documentation matches what is in it
- Every designer held one rotating position
- Every designer passed the defense, or has a scheduled re-run
- One post mortem per designer is committed
- The admin decision log explains every design decision a new joiner would question

The last item matters most for the next sprint. Sprint N plus 1 starts from the decisions this one recorded.
