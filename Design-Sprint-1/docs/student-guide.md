# Student Guide

How to work, day to day. Applies to every sprint. Read once properly, then use as reference.

---

## 1. Setup, before day one

1. Fork the sprint repo, clone your fork
2. Add the upstream remote so you can stay current:
   ```
   git remote add upstream https://github.com/StartwithDot/Design-Sprint-1.git
   git remote -v
   ```
3. Set your git identity to the email on your GitHub account, otherwise commits do not attribute to you:
   ```
   git config user.name "Your Name"
   git config user.email "you@example.com"
   ```
4. Accept the Figma team invite. Create your practice file named `SPRINT-1 Practice UX{n}`
5. Install: Stark or axe DevTools browser extension, and turn on VoiceOver (macOS: Cmd plus F5) or NVDA (Windows) at least once so it is not new to you in week 4

## 2. Find your work

Your folder is `students/UX{n}/`. Your code is assigned by the admin and does not change for 24 weeks.

Each week: `students/UX{n}/week{n}/problem_statement.md`. That file is the week. The full sprint view is `docs/task-list.md`.

## 3. The daily loop

```
git checkout main
git fetch upstream
git merge upstream/main          sync before you start, every time
git checkout -b UX3-C1-1         one branch per task
... do the work ...
git add students/UX3/week1/C1-1-type-scale.md
git commit -m "C1.1 type scale with Devanagari test"
git push origin UX3-C1-1
... open a pull request to upstream main ...
```

**One task, one file, one commit.** The commit message starts with the task ID. This is what makes review possible and what makes your contribution graph honest.

## 4. What goes in git and what goes in Figma

Figma holds the canvas. Git holds the reasoning. Neither is optional.

| Thing | Where |
|---|---|
| Screens, components, prototypes | Figma, source of truth |
| A link to the Figma frame, plus an exported PNG of the final state | Git, in the task file |
| Tokens | `system/tokens/*.json`, git is source of truth |
| Flow and IA diagrams | Mermaid in Markdown, git is source of truth |
| Every decision, every reason, every finding | Markdown, always |

If your work exists only in Figma, it cannot be reviewed as a diff and it does not count as committed.

### Task file format

Every task file follows this shape. Keep it short.

```markdown
# C1.1 Type scale

**Figma:** https://figma.com/file/... (frame: Type Scale)
**Time:** 90 min

## What I did
Three sentences maximum.

## Decisions
- Base 16px because ...
- Ratio 1.25 because ...

## What I would change
One line.

---
AI use: none. / AI use: Claude for microcopy variants, all copy rewritten and tested on 2 people.
```

The AI line is required on every file. Omitting it is treated as an undisclosed use.

## 5. Pull requests

- Title: the task ID plus a short description. `C1.1 type scale with Devanagari test`
- Body: what changed, and what you want the reviewer to look at hardest
- One task per pull request. Do not batch a week of work into one PR.
- Open PRs as work completes across the week. A Friday dump means nobody can review properly.

### Reviewing

You review two peers per week, minimum. A valid review comment does one of these:

- Names a principle and the user cost: "the error appears after upload, so Ramesh pays ₹50 before learning the document is wrong"
- Names something that will break: "this component has no disabled state, so the payment screen cannot use it"
- Asks for the evidence: "which test finding drove this change"

An invalid comment: "looks clean", "nice work", "maybe try a different colour". If you approve with no substantive comment, the critique lead logs it.

## 6. Merge policy

Regular merge or rebase merge. **Never squash.** Squashing collapses your commits into one and erases individual authorship in the shared zones. Your commit history is part of what you show later.

## 7. The shared zones

`system/` and `delivery/` are shared. Rules are stricter because a mistake there blocks four other people.

- Only the week's system owner merges into `system/`
- Core admin approval required on top of that
- Never edit someone else's component to fix your own screen. Open an issue or a PR against the component with the reason.
- If you need a variant that does not exist, propose it. If you override locally, write one line on why the system could not absorb it.

## 8. The gates

Three gates, all in `docs/accessibility-gate.md`. A deliverable that fails a gate is not done regardless of how it looks.

- **States gate.** Every state present.
- **Accessibility gate.** Keyboard, focus, contrast, targets, headings, names, errors, screen reader, reduced motion, colour independence.
- **Evidence gate.** Every claim about users names its source.

Run the gates on yourself before opening a PR. Failing a gate in review costs everyone time.

## 9. The week

| Day | What happens | Your job |
|---|---|---|
| Mon | Kickoff, 15 min | Read the week goal, know which position you hold |
| Tue to Wed | Build | Open PRs as work completes |
| Thu | Critique, 90 min | Present 12 min, take notes, do not defend live |
| Fri | Fix and merge | Address critique, run gates, land PRs |
| Sat | Spine, 90 min | Why session, teardown, drill review |

### Critique, how to present

12 minutes. Structure that works:

1. The problem, in one sentence, before you show anything
2. What you tried and rejected, 2 minutes
3. What you are showing, 5 minutes
4. The specific thing you want feedback on, stated as a question
5. Listen. Write everything down. Do not explain away a comment in the room.

You address feedback on Friday, not in the session. Arguing in the session burns everyone's time and usually means you have not heard the comment yet.

## 10. Asking for help

Ask in the cohort channel. Ask for a nudge, not an answer.

Good: "I cannot decide whether address entry is one page or four steps. I have read the Form Design Patterns chapter and my observation from R1.5 points both ways. What should I be weighing?"

Not useful: "how should I design the address form".

Rule: 45 minutes stuck, then ask. Sooner is fine if you are blocked on a decision the cohort has to make together.

## 11. Contribution graph, stated accurately

Commits in your fork do **not** count toward your GitHub contribution graph until they are merged into the upstream default branch. You will not see green squares immediately after pushing. That is normal, not a mistake on your end. Once your PR merges, the commits attribute to you, which is exactly why the program never squashes.

## 12. Honesty rules

- If you did not test it, do not write that users prefer it
- If AI generated something, disclose it on the file and say how you verified it
- If you did not finish, commit what exists with one line on what is missing. A partial commit with an honest note beats a silent week.
- "I do not know yet, here is how I would find out" is a passing answer at every defense. Bluffing is not.

## 13. Time

12 to 15 hours a week. 8 to 10 on sprint tasks, 4 to 5 on the spine.

If a week runs over, cut Craft tasks first and tell the admin what you cut. Evidence, systems, and spine tasks do not get cut, because those are the ones that cannot be retrofitted later.

## 14. What gets you removed from the cohort

Only two things: silence across two weeks with no response to a direct message, and passing off someone else's work or an AI output as your own tested finding. Everything else is coachable.
