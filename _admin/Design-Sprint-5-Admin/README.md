# Design Sprint 5, Admin

Private. General machinery is in `../Design-Sprint-1-Admin/`. This covers Sprint 5 only: the self-directed capstone.

---

## What this sprint is testing

Whether a designer can run a whole project without scaffolding: scope it, research it, design it to the standard, test it, absorb a severe change, and defend twenty weeks of decisions. Nothing new is taught. That is the point.

## Before week 17

- **Approve every project in writing before week 17.** Options A to D or a proposal. A proposal passes only if the users are reachable, the scope is a flow and not a product, the ethical tension is stated, and the baseline number exists or can be got in week 17. Push every scope down once.
- Confirm each designer can reach **five real users twice** (weeks 17 and 19). If not, steer to a different option now, not in week 17.
- Anything involving minors (Option C) needs written guardian consent and your approval of the consent form before any session.
- Book the external bench for JR5 (Mock interview 3: behavioural and whiteboard, 60 minutes) in week 20, and an external reviewer for the 20-minute presentation.
- Seal the injection (`failure-injections/sprint5.md`). It is individual and severe; choose one per designer.

## Weekly focus

**Week 17.** Do not let anyone design before research is signed off (evidence gate). The task list each designer writes is itself graded: under- and over-scoping both lose points. L-AI5 is the same for everyone. Read the "over-trust and under-trust behaviours" before the screens; if the behaviours are generic ("users may trust it too much"), the design will be generic.

For Option D designers, the domain study is the gate. A designer who does not know what a debt-service coverage ratio is or why bank statement variance matters will design a beautiful screen an underwriter cannot use, and will not know why. Density is where Sprint 1 to 4 craft is tested: 38 fields, scannable in 40 seconds, while WCAG 2.2 asks for 24px targets. The resolution has to be stated, not fudged.

**Week 18.** The craft gate week. Check system compliance: extensions documented and contributed back, no silent forks. L-PR4: read the "seams" list; a designer who cannot name three places a participant would see the prototype is fake has not looked.

For Option D, C18.1 (or its equivalent in their task list) must include "do not show the score at all" as one of the alternatives. Enforce it. Anchoring is where the strongest thinking appears: if the score is visible before the underwriter reads the file, it anchors judgement; sequencing it after costs time per application, and time is what the underwriter is measured on daily. That tension has no clean answer and the quality of the reasoning is the best signal this sprint produces.

**Week 19.** Findings must have changed the design, with the trace. The ethics review of their own work should find something; "nothing" means they did not look. For Option D, model unavailable is not an error, it is a normal condition at 2 to 8 seconds of latency. Anyone who designed it as an error toast has designed for the demo. The decline sentence catches the regulatory misunderstanding: watch for any sentence that attributes the decision to the model or presents a contributing factor as a cause.

**Week 20.** Screen reader pass with the announced text written out verbatim. The capstone rubric (`../../Design-Sprint-5/06-capstone-rubric.md`) is applied by you and the external reviewer separately. JR5 and the mock interview happen here as well; schedule them so they do not collide with the 75-minute defense.

## The injection

`failure-injections/sprint5.md`. Week 19, Day 4 morning, with one week left. Individual and severe: it may invalidate a finding, remove a user group, or impose a technical limit that breaks the core interaction.

## Defense notes for this sprint

The defense is 75 minutes and covers all five sprints. Anything from week 1 is fair game.

**The adversarial round.** Use the project's own worst risk. For Option D, this is the strongest in the program:

> "An underwriter approved a ₹12 lakh loan in 11 seconds. Your interface showed a green score. The business defaulted in four months. You are in front of the audit committee. Explain your design."

Hold it. Push twice. What you are looking for is whether they can distinguish between an interface that failed and a human who made a bad decision, and whether they can accept the part that is theirs without accepting the part that is not. The best answer names the specific thing in their design that permitted an 11-second approval, states what it would cost to prevent it, and states why they made that trade. The worst answer blames the underwriter; the second worst accepts total blame.

For the others, build the equivalent: a patient who arrives on the wrong day (A), a worker who loses a dispute because the 48-hour window closed in the background (B), a student whose father overrides the application (C).

**Numbers round additions:** their baseline, their guardrail, the sample in each round, the contrast ratio of their primary text, the smallest target, the number of states in their matrix.

## The failure specific to this sprint

Designers who make the thing look impressive rather than trustworthy. For Option D: confidence rings, animated score reveals, gradient risk bands. Each increases over-trust, because visual sophistication reads as epistemic authority. The question that stops it: "does this make an underwriter more likely to read the file, or less."

The second failure is the opposite and rarer: a designer so worried about over-trust that they bury the score until the model is useless. Both are failures of calibration, which is the actual subject.

The third: a capstone with no number. If the baseline did not exist, say so in the ledger, because it will recur in Sprint 6.

## JR5 session

Mock interview 3: two behavioural questions, one 30-minute whiteboard, one salary question. Collect scorecards. Record the three worst questions per designer in the ledger.
