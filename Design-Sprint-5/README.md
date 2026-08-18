# Design Sprint 5: Complex Interfaces and AI

**Weeks 17 to 20. UX1 to UX5.**

The project: a **loan underwriting console** where a model scores every application and a human is legally accountable for the decision. 200 underwriters, 45 applications a day each, 38 fields per application, and a model that is right 71 percent of the time in the band where most cases sit.

The hardest interface problem in the program. Not because of the visuals, because of what the interface is asking a person to believe.

## Read first

1. `docs/project-brief.md`
2. `docs/task-list.md`
3. `docs/ai-patterns.md`
4. Your own `students/UX{n}/week17/problem_statement.md`

## What ships by week 20

- A domain study, because you cannot design this screen without understanding underwriting
- 38 fields on one screen, scannable in 40 seconds, keyboard complete
- The AI surface: score, confidence, contributing factors, and uncertainty
- Every failure state: model unavailable, model slow, model wrong, confidence missing
- The override flow and what it records
- The decline sentence an applicant actually receives
- A screen reader pass, because two people at this company use one
- An anchoring test with real evidence about what the score does to human judgement

## The two failures this sprint exists to teach

**Over trust:** the underwriter approves in 11 seconds because the score was green. When the model is wrong, money goes to a business that cannot repay it and nobody can explain the decision.

**Under trust:** the score is ignored, the model is wasted, and nothing improves.

Every design decision in these four weeks sits somewhere between those two, and at the defense you will be asked to say exactly where yours sits and why.

## The rule of this sprint

**The model informs. The human decides. The interface must make that true, not just say it.** An interface that presents a probability as a verdict has made the decision on the underwriter's behalf and left them holding the accountability.
