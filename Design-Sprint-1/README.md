# Design Sprint 1: Craft and the Single Flow

**Weeks 1 to 4. 5 designers, coded UX1 to UX5.**

The project: rebuild the **Aadhaar address update flow** as a usable product. Real service, real constraints, genuinely bad current experience, and every designer has either used it or watched a family member struggle with it.

By week 4 each designer ships one complete flow with every state, passing the accessibility gate, built on a shared design system the cohort owns together.

## Read first

1. `docs/project-brief.md` for the client, the users, the constraints
2. `docs/student-guide.md` for how to work day to day
3. `docs/task-list.md` for every task in the sprint
4. `docs/accessibility-gate.md` for the checklist that blocks sign off
5. Your own `students/UX{n}/week1/problem_statement.md` to start

## Zones

| Zone | What goes there | Review |
|---|---|---|
| `students/UX{n}/week{n}/` | Your own practice. Mistakes cost nothing. | Critique lead, one peer |
| `system/` | The one shared design system. Tokens, components, docs. | System owner plus core admin |
| `delivery/` | Shared outputs: flows, audits, handoff, presentation. | System owner plus core admin |
| `fundamentals/` | The spine: why sessions, teardowns, explainers, decision records. | Core admin |

## What ships by week 4

- A shared design system with tokens, a type scale, a spacing scale, a colour system with semantic roles, and eight documented components
- Each designer's full address update flow at 390px and 1440px
- Every state for every screen: default, empty, loading, partial, error, success, offline, permission denied, zero results, first run, destructive confirm
- An accessibility audit of the current government flow and of your version
- One decision record per designer explaining a choice a stakeholder would question
- One post mortem per designer from the week 3 injected failure
- A handoff spec an engineer could build from

## Non negotiable

- Every flow passes the accessibility gate before it is called done
- Every screen ships all states
- Every claim about users names its source
- One task, one file, one commit, named with the task ID
- Figma is the canvas, git holds the decisions
