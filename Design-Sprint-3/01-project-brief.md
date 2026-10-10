# Sprint 3 Project Brief: Sutra, a Subscription That Has to Be Cancellable

**Weeks 9 to 12 | Track focus: Interaction, Product and Ethics | Cohort: UX1 to UX5**

*Sutra is a fictional company. The numbers are invented for this exercise and are consistent across the sprint. Do not quote them outside it.*

---

## 1. The client

Sutra is a spoken-language learning app. Learners practise English, and Hindi, Tamil or Telugu as a second language, in ten-minute daily lessons with a voice coach. Three years old, 45 people, Android first, iOS second.

| Metric | Value |
|---|---|
| App installs, last 12 months | 1,200,000 |
| Created an account | 520,000 (43% of installs) |
| Completed a first lesson | 286,000 (55% of accounts) |
| Completed 5 lessons within 7 days | 74,000 (26% of first-lesson completers) |
| Started the 7-day free trial | 41,000 |
| Paid after the trial | 8,200 (20% of trials) |
| Paying learners today | 31,000 |
| Price | ₹499 per month, or ₹3,999 per year |
| Still paying at month 3 | 54% |
| Still paying at month 3, if they completed 5 lessons in their first week | 81% |
| Cancellation attempts per month | about 3,400 |
| Support contacts that include the words "cancel" or "charged" | 22% of all support volume |
| Runway | 16 months |

The pattern is the brief. People who build a habit in week one stay; people who do not leave quietly or, worse, leave angrily. The company's instinct is to fix the second group with friction in the cancellation flow, and a board member has already suggested it.

The company's brief: "reduce churn."

That is a goal, not a brief. Your first job is to find out which churn.

## 2. What the product does

Daily lessons, a streak counter, voice practice with feedback, a weekly progress summary, and a subscription: free trial, monthly, annual, pause, cancel, reactivate.

What learners use instead, and this is the real competition:

| Job | What they do today |
|---|---|
| Learn English phrases | Free video lessons and short clips on their phone |
| Practise speaking | A WhatsApp group with friends, or nothing |
| Stay motivated | A study group, or a coaching centre they pay in cash |

Free and good enough is the competitor. A design that is better than other apps and worse than a free video loses.

## 3. The users

**Divya, 21, college student.** Pays through UPI AutoPay set up on her father's phone. Uses the app on a prepaid Android phone with limited storage. Failure mode: an autopay debit fails, her subscription goes past due, she gets one notification she does not see, and her streak resets. She believes she did something wrong and stops opening the app.

**Imran, 34, retail supervisor.** Bought the annual plan to get a promotion that needs spoken English. Travels for Ramzan every year and will not study for a month. Failure mode: looks for a way to pause, cannot find one, and cancels. Six months later he would have come back.

**Mr. Prakash, 58.** Subscribed because his son set it up as a gift, and does not know it renews. Failure mode: sees a charge he does not recognise, believes it is fraud, calls his bank, and files a chargeback. Sutra pays a fee and a penalty to the card network, and gets a one-star review.

The buyer, the user and the person watching the bank statement are often three different people. A designer who solves for the engaged learner alone has solved for the people who were never going to cancel.

## 4. What is known

- 60% of the learners who leave in the first month never completed five lessons in their first week
- Learners who reach a streak of 5 days convert from trial to paid at roughly three times the rate of those who do not
- 35% of cancellation attempts happen within 48 hours of a renewal charge
- Of those who reach the cancel screen today, about one in four abandons it because it asks them to email support
- A quarter of "I want to cancel" support contacts say they had already tried in the app
- 11% of past-due subscriptions are recovered by the one email that goes out; nobody has measured whether the in-app banner helps

The 5-lesson number and the 35% renewal number are the two most useful facts. What you do with them separates this sprint's outcomes.

## 5. Constraints

| Constraint | Consequence |
|---|---|
| Recurring UPI and card debits need a pre-debit notification, about 24 hours before each charge | A renewal cannot be a surprise to the user, and the notification is a design surface |
| India's consumer protection authority has published guidance naming dark patterns, including subscription traps and false urgency | The legal exposure of a manipulative flow is real and written down |
| The Digital Personal Data Protection Act applies to learner data | What happens to a learner's data after cancellation is a design decision with a legal consequence |
| Payment provider confirms a cancellation in 4 to 6 seconds | A latency state you must design, not hide |
| Android storage is tight for most learners | Heavy motion and heavy assets have a real cost |
| Engineering is 6 people | Scope is real |
| Learners study in a noisy room, often one-handed, in short sessions | Interaction must be forgiving and fast |

## 6. The metric work

This sprint requires you to define the metrics, not cite them (task P9.2).

**Primary:** you must define **activation**. The company has not. Is it one lesson, five lessons in week one, a 5-day streak, a voice exercise passed? Your definition has to be defensible against the retention data in section 1.

**Input metrics:** time to first completed lesson, share of trial starters who reach a 3-day streak, share of past-due accounts recovered within 7 days.

**Guardrail:** month-3 retention, refund rate and chargeback rate must not get worse. A flow that lifts activation by pushing discounts and then loses people at month 3 has moved a number and destroyed value.

**Traffic for experiments** (needed in E1.5): about 3,400 cancellation attempts a month, of which roughly 40% see a retention offer today. Use this to decide whether an experiment can detect an effect in a sensible time.

## 7. Deliverables by week

| Week | Ships |
|---|---|
| 9 | The subscription state machine with every guard, a latency plan and feedback design, undo and irreversibility decisions, a transition inventory, high-fidelity states, state-change microcopy, five interaction principles, and the funnel with an activation definition and metric set |
| 10 | A motion audit of three real products, duration and easing decisions, a purpose test that deletes decoration, built transitions, a reduced-motion version, and a motion spec |
| 11 | A dark pattern audit of three real products, a persuasion test, one built dark pattern with its cost accounted, the honest version with a business argument and an experiment design. **The business demand lands.** |
| 12 | An ethics position, a written refusal, the shipped flow with an accessibility pass and a full spec with instrumentation, the showpiece pass, and the defense |

## 8. The scope exercise

You have a **six-week appetite** with six engineers, not a scope list. What fits is the design. Anything that does not fit gets cut, and the cut is written down with the reason.

A designer who delivers a beautiful flow that needs nine months of engineering has not designed a product, they have drawn one.

## 9. The ethics decision

In week 11 the client will make one of the following requests, delivered through the core admin. You do not know which until it arrives.

- Pre-select the annual plan at checkout, with auto-renewal, and show the monthly price in small grey text
- Replace the in-app cancel button with a chat, so that cancelling needs a conversation with a retention agent
- When the trial ends, show a countdown and "your streak and progress will be deleted in 24 hours" unless the learner pays
- Charge the renewal first and send the pre-debit reminder afterwards, to catch learners who would have cancelled

Your answer, in writing, must state: what it does to the number, what it costs the learner, where it sits against the dark pattern catalogue and the law, and what you would build instead that earns a defensible share of the same business outcome.

**Refusing without an alternative is not an answer.** Neither is complying. The reasoning is the deliverable.

## 10. The showpiece standard

This is the sprint's visual project. Sutra is a consumer app that people choose to open, and it has to feel like one: considered type, colour with a point of view, delight in the lesson-complete moment, motion with a purpose. Week 12 includes a showpiece pass (C12.3) because this is the work that goes on the front page of your portfolio.

The standard does not replace the accessibility gate. It sits above it. A beautiful screen that fails contrast is not a showpiece, it is a failure.

## 11. Reading

Assigned across the sprint (see the week files for the exact chapters):

- About Face, Cooper, chapters on postures, undo and error tolerance
- Designing Interface Animation, Val Head
- Ruined by Design, Mike Monteiro
- deceptive.design, the pattern catalogue
- The published guidance on dark patterns from the CMA, the FTC and India's consumer protection authority
- The Google HEART framework paper, and the funnel chapters of Lean Analytics (for P9.2)

The full resource list is in the root `03-Books-And-Resources.md`.
