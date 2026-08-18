# Sprint 5 Project Brief: The Loan Underwriting Console

**Weeks 17 to 20 | Track focus: Complex and AI interfaces | Cohort: UX1 to UX5**

---

## 1. The client

An NBFC lending to small businesses. Loans of ₹50,000 to ₹15,00,000. 200 underwriters, each processing 30 to 60 applications a day.

A model now scores every application before a human sees it. The model outputs a risk band, a confidence figure, and the four factors that most influenced the score. The underwriter decides. The model does not.

The company's brief: "put the AI score in the interface".

That is a one line brief hiding the hardest interface problem in the program.

## 2. The real problem

The model is right about 82 percent of the time in the top band and about 71 percent in the middle band.

Two failure modes, and both are worse than they look:

**Over trust.** The underwriter sees a green score and approves without reading. This is what will happen if the score is presented as a verdict. When the model is wrong, a business that should have been declined gets money it cannot repay, and the underwriter has no defence in an audit because their reasoning was "the score was green".

**Under trust.** The underwriter ignores the score entirely and the company has paid for a model nobody uses. Everything measured stays where it was.

The interface has to land between those, and where it lands is a design decision with a legal consequence.

## 3. Regulatory reality

- The applicant has a right to a reason for a decline, and "the model said so" is not a reason
- The underwriter is accountable for the decision, not the model
- The audit trail must show what the underwriter saw and what they did
- The model's factors are explanatory, not causal, and presenting them as causal is a misrepresentation

That last point is the one designers get wrong. "Your loan was declined because of your bank balance variance" is a statement the model cannot support. The factor contributed to a score. It did not cause a decision.

## 4. The users

**Meena, 29, underwriter, 3 years in.** 45 applications a day, judged on throughput and on default rate. Fast, keyboard driven, has never used the mouse for anything she does often. Failure mode: adopts the score as a shortcut because throughput is measured daily and default rate is measured quarterly.

**Rajesh, 51, senior underwriter, 22 years in.** Does not believe the model. Has seen three risk systems come and go. His judgement is genuinely better than the model in the middle band and worse in the tails, and he does not know that. Failure mode: ignores the score, and teaches the juniors to.

**Priya, 38, credit head.** Needs the portfolio view, the override rate, and to know when the model is drifting. Failure mode: sees only aggregate numbers and never learns that the middle band is where all the disagreement lives.

## 5. What is in an application

38 fields, 6 uploaded documents, a bank statement analysis with 6 months of transactions, GST filing history, an existing loan check, and now the model output. A single application is genuinely dense and cannot be made sparse.

This sprint's craft problem is density done well: 38 fields on one screen that a person can scan in 40 seconds, not 12 wizard steps.

## 6. Constraints

| Constraint | Consequence |
|---|---|
| Model latency is 2 to 8 seconds | The score is not there when the screen loads. Design the wait. |
| Confidence is sometimes unavailable | Design for its absence, not just its presence |
| 45 applications a day per underwriter | Every extra click costs 45 clicks a day. Keyboard first is not a preference. |
| Decisions are legally accountable to the human | The interface cannot imply the model decided |
| Regional language support is not required for this internal tool | One of the few constraints that removes work |
| Screen readers are used by two underwriters in the company | Accessibility here is not hypothetical, it is two named colleagues |

## 7. Success measures

**Primary:** decision quality, measured as default rate at 6 months on approved loans, with throughput held constant. Both halves matter. Speed alone is easy and worthless.

**Input metrics:** time per application, override rate against the model, proportion of decisions where the underwriter opened the bank statement detail, rate of decisions made in under 20 seconds on middle band applications.

**Guardrail:** the proportion of approvals made without opening any supporting evidence must not rise. That is the over trust metric and it is the one that predicts the audit finding.

## 8. Deliverables by week

| Week | Ships |
|---|---|
| 17 | Domain study, information hierarchy for 38 fields, density strategy, keyboard model |
| 18 | The AI surface: score presentation, confidence, factors, uncertainty, and the wait |
| 19 | Error and edge cases, model unavailable, model wrong, override flow, explanation to the applicant |
| 20 | Full console, screen reader pass, decision record, defense |

## 9. The three hard questions

Answer all three in writing, and expect to be attacked on all three at the defense.

**How do you present a score so it informs without deciding.** Consider not showing the number at all. Consider showing it only after the underwriter forms a view. Consider showing the factors without the score. Each of those has a cost. Pick one and own the cost.

**How do you present confidence to someone who does not think in probability.** 71 percent means nothing useful to a person deciding one case. It is a statement about a population, not about this application. Anything you design here is a translation, and every translation loses something. Say what yours loses.

**What does the applicant get told.** The underwriter declined. The model contributed. The applicant is entitled to a reason. Write the actual sentence.

## 10. Reading

Assigned:
- People + AI Guidebook, Google, fully
- Microsoft Human AI Interaction Guidelines, all 18
- Apple Human Interface Guidelines, Machine Learning section
- The RBI guidance on digital lending, the sections on transparency and grievance
- Data driven design and enterprise density: Few, and any two dense professional tools studied properly

Full list: `../../Learning Resources.md` Sprint 5 section.
