# Sprint 1 Project Brief: Aadhaar Address Update

**Weeks 1 to 4 | Track focus: Craft and Interface | Cohort: UX1 to UX5**

---

## 1. The client story

A state government digital services unit has budget to rebuild one citizen service. They picked the Aadhaar address update because it generates the highest volume of assisted service centre visits in the state. Citizens who could complete it online come to a physical counter instead, and each counter visit costs the department money and costs the citizen half a day.

The unit's brief, verbatim: "make it so people stop coming to the counter".

That brief is deliberately bad. Part of week 1 is turning it into something answerable.

## 2. Why this service and not a social app

Four reasons, stated because designers ask.

1. **The stakes are real.** A failed address update means a blocked bank account, a delayed gas subsidy, a school admission held up. The cost of a confusing error message is measurable in someone's week.
2. **The constraints are real.** Document upload on a slow connection, OTP dependency, government identity verification rules, Hindi and English and one regional language, users on ₹6000 Android phones, users who are functionally new to smartphones, users who have never typed their own address.
3. **The current version is genuinely bad and studying it teaches more than admiring good design.** Every heuristic violation you will ever need to name is already present in the live flow.
4. **Nobody has redesigned it on Dribbble.** There is no aesthetic to copy, so craft has to come from reasoning.

## 3. The service, as it exists

The real flow, in order:

1. Log in with Aadhaar number plus OTP to the registered mobile
2. Choose "update address"
3. Choose document based update or head of family based update
4. Type the new address across separate fields: house, street, landmark, area, village or town, post office, district, state, PIN
5. Upload one proof of address document
6. Pay ₹50
7. Receive a URN, the request number used to check status later
8. Wait, then check status separately

Where it breaks, observably:

| Break | What the citizen experiences |
|---|---|
| Document list is a wall of 40 accepted types with no guidance | Uploads the wrong one, gets rejected days later |
| Upload rejects silently on size or format | Retries the same file repeatedly, gives up |
| Address fields have no examples and unexplained rules | Fills them wrong, request rejected |
| OTP session expires mid form with no warning | Loses everything typed |
| URN appears once and is easy to lose | Cannot check status, calls the helpline, visits the counter |
| Rejection reason arrives as a code, not a sentence | Does not know what to fix, visits the counter |
| No language support at the point of confusion | Abandons |
| Zero indication of how long anything takes | Assumes it failed, visits the counter |

## 4. Users

Three primary users, each with a different failure mode. Every designer designs for all three, not one.

**Ramesh, 52, small shop owner, tier 2 town.** Second hand Android, 4G that drops indoors, reads Hindi comfortably and English slowly. Has the electricity bill but not in his name. Failure mode: picks the wrong document because he does not know that "in your name" is the actual rule.

**Priya, 24, nurse, moved cities for work.** New phone, good connection, English fluent, in a hurry, does this on a night shift break. Failure mode: session expires while she finds her rental agreement, loses everything, does not restart.

**Lakshmi, 67, retired, lives with her son.** Uses her son's phone. Cannot receive the OTP because the registered mobile is a number she no longer has. Failure mode: cannot even begin, and no path in the interface explains why or what to do.

Secondary user: the **assisted service centre operator**, who does 40 of these a day on a shared desktop, keyboard first, and needs speed over friendliness. This user shows up properly in Sprint 5 but the operator's needs are noted here.

## 5. Constraints, all real

| Constraint | Consequence for design |
|---|---|
| OTP to registered mobile only | Lakshmi's case must have a designed path, not a dead end |
| Documents must be in the applicant's name | The rule must be stated before upload, not after rejection |
| ₹50 payment, no refund on rejection | Rejection risk must be reduced before submit, not explained after |
| Processing takes 5 to 30 days | Status and expectation setting is core, not a nicety |
| Three languages: English, Hindi, one regional | Type must survive Devanagari, layout must survive 30 percent text expansion |
| Slow 3G is common | Every image, every step, every retry has a cost |
| Government accessibility obligation (RPwD Act, GIGW) | WCAG 2.2 AA is a requirement, not a preference |
| Existing backend rules cannot be changed | You redesign the experience, not the policy |

Constraints do not get negotiated away. A solution that requires changing UIDAI policy is out of scope and saying so is part of the work.

## 6. Scope

**In scope**
- Entry and identity verification, including the no access to registered mobile case
- Document guidance and upload
- Address entry
- Review and payment
- Confirmation and URN handling
- Status check
- Rejection and resubmission
- All of the above at 390px and 1440px
- The shared design system that all five flows are built on

**Out of scope**
- Account creation, biometric update, name or date of birth update
- The operator console (Sprint 5)
- Native app design
- Backend, policy, or payment gateway design
- Brand or logo work

## 7. Success measures

Named in week 1, before design starts. The department cares about counter visits. Designers must translate that into something a design can move.

**Primary metric.** Online completion rate for address update, measured as submissions completed divided by flows started.

**Input metrics.** Document rejection rate after submission. Time to first submission. Session expiry abandonment rate. Status check without helpline contact.

**Guardrail metric.** Fraudulent or incorrect submissions must not rise. A flow that is easy because it stopped checking anything is a failure. Every designer names one guardrail and defends it at the defense.

## 8. Deliverables by week

| Week | Ships |
|---|---|
| 1 | Problem reframe, constraint list, heuristic audit of the live flow, accessibility audit of the live flow, type scale, spacing scale, colour system, metric definition |
| 2 | Flow diagram, first four components in the shared system, mid fidelity screens for the happy path, microcopy for every error the service can produce |
| 3 | All states for all screens, usability test on your own flow with 3 participants, injected failure handled, post mortem |
| 4 | High fidelity flow at both widths, accessibility gate passed, handoff spec, decision record, defense |

## 9. The shared system

All five designers build one design system together in `system/`. Not five systems.

Rationale: a system that only one person uses proves nothing. A system five people build on immediately surfaces the real problems, which are naming, ownership, and the cost of changing a token everyone depends on.

The system owner rotates weekly. The system must build and its documentation must match what is in it before the sprint is called done.

## 10. Reference material

The full list with tiers is in `../../Learning Resources.md`, Sprint 1 section. The four that are assigned reading, not reference:

- Refactoring UI, Wathan and Schoger
- Form Design Patterns, Adam Silver
- The Design of Everyday Things, Norman, chapters 1 to 4
- WCAG 2.2 quick reference, AA criteria

Study the live service at `myaadhaar.uidai.gov.in` before writing anything. Screenshot everything. Do not create an account with anyone else's Aadhaar.

## 11. The client conversation you will not get

Real government units do not run design reviews. The core admin plays the department. Expect a scope change in week 3, and expect it to be inconvenient. That is not unfair, it is the job.
