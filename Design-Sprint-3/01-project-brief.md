# Sprint 3 Project Brief: The Transporter Platform

**Weeks 9 to 12 | Track focus: Product and Business | Cohort: UX1 to UX5**

---

## 1. The client

A three year old company selling fleet management software to small transporters. Web plus a basic Android app. ₹2,400 per truck per year.

The numbers:

| Metric | Value |
|---|---|
| Paying customers | 400 fleet owners |
| Trucks under management | 4,800 |
| Signed up in the last 12 months | 1,900 |
| Still active at day 30 | 410, which is 22 percent |
| Still paying at month 12 | 61 percent of those who reach day 30 |
| Average fleet size | 12 trucks |
| Runway | 14 months |

The pattern is clear and it is the entire brief: people who get past day 30 stay for years. People who do not get past day 30 leave in the first fortnight. Everything the company spends on acquisition is being poured into a bucket with a hole in the first two weeks.

Their brief: "improve onboarding".

## 2. What the product does

Trip management, driver records, fuel logs, maintenance schedules, document expiry tracking for permits, insurance and fitness certificates, and basic profit per trip.

What the customer does today instead, and this is the real competitor:

| Job | Current tool |
|---|---|
| Assign a trip to a driver | Phone call |
| Track where the truck is | Call the driver |
| Record fuel | Paper slip in the glovebox, entered into a diary weekly |
| Know when insurance expires | Memory, plus an agent who calls |
| Know if a trip made money | Mental arithmetic, monthly, roughly |
| Share a delivery note | WhatsApp photo |

**WhatsApp and a diary are the competitor.** Not another software product. A design that is better than the other software and worse than the diary loses.

## 3. The users

**Suresh, 44, owns 14 trucks.** Runs the business from a small office and his phone. Types slowly, uses voice notes constantly, has never used a desktop spreadsheet. Sharp about money and can tell you the margin on any route from memory. Failure mode: signs up, sees a form asking him to enter 14 trucks with 9 fields each, closes it, never returns.

**Anita, 31, runs operations for her father's 30 truck fleet.** Comfortable with software, uses Excel well, is the person who would actually adopt this. Failure mode: adopts it, finds that the drivers do not submit anything, and abandons it after three weeks of doing double entry.

**Ravi, 38, driver.** Android phone, low storage, prepaid data, drives 10 hours a day. He is not the buyer and he is the one who has to enter the data. Failure mode: every single one of them. If the driver does not submit, the platform holds stale data and stale data is worse than no data.

The buyer and the data entry user being different people is the structural problem of this product. A designer who solves for Suresh alone has designed something that fails in week two.

## 4. What is known

- The first three days are where 60 percent of the loss happens
- The signup flow requires adding at least one truck before anything can be seen
- Adding a truck asks for 9 fields, four of which need documents the owner does not have to hand
- 71 percent of accounts never add a second truck
- Accounts that record 10 or more trips in the first month retain at 4 times the rate of those that do not
- Support requests in the first week are overwhelmingly "how do I get my drivers to use this"

That last one and the 10 trip number are the two most useful facts in the brief. What a designer does with them separates this sprint's outcomes.

## 5. Constraints

| Constraint | Consequence |
|---|---|
| Drivers are on cheap Android phones with little storage and prepaid data | The driver side has a hard weight budget. An app install may be the wrong answer. |
| Permit, insurance, and fitness documents are legally required and vary by state | Document tracking cannot be simplified away, only staged |
| The company has 14 months of runway | A design that takes 9 months to build is a design that does not happen |
| Engineering is 4 people | Scope is real. Shape Up appetite applies. |
| Owners will not do data entry | Anything requiring the owner to type regularly fails |
| No integrations with GPS providers yet | Live location is out of scope. Designing around its absence is in scope. |

## 6. The metric work

This sprint requires you to define, not just cite, the metrics.

**Primary:** day 30 activation, and you must define activation. The company has not. Is it a trip recorded? Three trips? A second truck added? A driver submitting once? Your definition must be defensible against the retention data, which shows 10 trips in month one is a strong signal.

**Input metrics:** time to first trip recorded, proportion of accounts with a second truck in the first week, proportion of drivers who submit at least one record, first week support contact rate.

**Guardrail:** paid conversion and month 12 retention must not fall. An onboarding that gets people to a hollow activation event and then loses them at month 3 has moved a number and destroyed value.

## 7. Deliverables by week

| Week | Ships |
|---|---|
| 9 | Activation defined with evidence, funnel mapped, IA proposed, competitive teardown including WhatsApp as the competitor |
| 10 | Feature scoped in Shape Up terms with an appetite, IA tree tested, end to end flow designed |
| 11 | Prototype with real logic, tested with 5 users, persuasion audit, the ethics decision |
| 12 | Final flow, instrumentation plan, experiment design, business case, defense |

## 8. The scope exercise

You have a six week appetite, not a scope list. What fits in six weeks of four engineers is the design. Anything that does not fit gets cut and the cut is written down with the reason.

A designer who delivers a beautiful flow requiring nine months of engineering has not designed a product, they have drawn one.

## 9. The ethics decision

In week 11 the client will ask for one of the following, delivered through the core admin. You do not know which one until it arrives.

- A default that opts fleet owners into a paid add on
- A cancellation flow with a retention offer that requires a phone call
- A notification pattern that pushes drivers harder than they consented to
- A trial expiry that hides the fleet's own data behind the paywall

Your answer, in writing, must state: what it does to the number, what it costs the user, where it sits against the dark pattern catalogue and the DPDP Act, and what you would do instead that achieves a defensible share of the same business outcome.

**Refusing without an alternative is not an answer.** Neither is complying. The reasoning is the deliverable.

## 10. Reading

Assigned:
- Inspired, Cagan, parts 1 to 4
- Shape Up, the shaping and betting sections
- The Google HEART framework paper
- Deceptive Design, the pattern catalogue
- Information Architecture, Rosenfeld et al, the navigation and labelling chapters

Full list: `../../Learning Resources.md` Sprint 3 section.
