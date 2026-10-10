# Week 1 Answers, Admin Only

Model answers and the acceptable range. Never shared. A designer who reads this file loses the week.

The purpose is calibration, not a key. Most of these tasks have several right answers and one shape of wrong answer, and the shape of wrong is what you are checking for.

---

## P1.1 Questions the brief does not answer

**Strong questions**
- How many of the counter visits are from people who tried online and failed, versus people who never tried. Answerable from centre operator logs, two weeks.
- What is the current rejection rate on online submissions and what are the top three rejection reasons. Answerable from UIDAI processing data, one week if the department has access.
- What proportion of citizens attempting this have access to the mobile number registered on their Aadhaar. Answerable only by a survey, four weeks, and this is the question that decides whether Lakshmi's case is an edge case or a third of the volume.

**The tell for a weak answer.** Questions about preference: "what colour scheme does the department want", "should it be mobile first". Those are answerable by the designer and are therefore not the department's questions.

## P1.2 Problem statement

**Acceptable**
> A citizen who has moved cannot update the address on their Aadhaar without visiting a service centre, because the online flow does not tell them which document qualifies until after they have paid and waited, which costs them ₹50 plus half a day per attempt and costs the department a counter transaction it has already paid for twice.

Checks: names the user, names the job, names the obstacle specifically enough to design against, states both costs. No solution words.

**Fails**
> Users need a better, more intuitive address update experience with clearer guidance and a modern interface.

That contains three solutions and no obstacle.

## P1.3 Constraints

The five in the brief must appear. The three found by using the service should include at least one of:

- Session times out at roughly 15 minutes with no warning
- The document upload accepts a file then rejects it server side, so the failure arrives after the wait
- The URN is displayed once and is not emailed or messaged
- The address fields do not match how addresses are written in most of India, so people improvise
- No indication anywhere of processing time

**The classification is what to check.** A designer who marks "OTP to registered mobile only" as assumed rather than fixed policy has not read the constraint. A designer who marks "₹50 fee" as fixed and then also notes that whether the fee is refundable is assumed, not stated, has read it very well.

## P1.4 Metrics

**Primary:** online completion rate, submissions completed divided by flows started. Accept variants that are measurable and directional.

**Input metrics, strong choices:** document rejection rate after submission, session expiry abandonment, time to first submission, proportion of status checks that do not result in a helpline call.

**Guardrail, and this is the discriminating part of the task.** The guardrail must protect against the design succeeding at the metric while damaging something. Strong answers:

- Rate of incorrect or fraudulent address submissions must not rise. Bad design that only chases completion would drop the document requirement or accept any upload.
- Rejection rate must not rise. A flow that gets more people to submit worse applications has moved the metric and increased total counter visits, which is the opposite of the brief.

**Fails:** "user satisfaction", with no way to measure it. Or naming a guardrail that is really a second success metric.

## R1.2 Heuristic audit

Twelve findings is the floor. Expect these to appear, and expect a strong audit to find them without prompting:

| Heuristic | The finding |
|---|---|
| Visibility of system status | No processing time stated anywhere, no progress on upload |
| Match to the real world | Address fields do not match how addresses are written |
| Error prevention | Document rules revealed after payment, not before |
| Recognition over recall | URN shown once, user must remember or copy it |
| Error messages | Rejection arrives as a code, not a sentence |
| User control and freedom | No way to save and resume, no back without loss |
| Consistency | Terminology differs between screens for the same thing |
| Help and documentation | 40 accepted document types listed with no guidance |

**Severity is where most audits fail.** A designer who rates everything 3 and 4 has not prioritised. The rejection code with no explanation is a 4, because it directly causes a counter visit. Inconsistent terminology is a 2. If those two carry the same severity, the rating is decorative.

## R1.3 Accessibility audit

Expect, at minimum, and each must carry a criterion number:

- Focus indicator missing or invisible on at least one control, 2.4.7
- Placeholder used as label somewhere, 3.3.2
- Contrast failure on secondary or helper text, 1.4.3
- Error identified by colour alone, 1.4.1
- Form field with no programmatic label, 1.3.1 or 4.1.2
- Session timeout with no warning or extension, 2.2.1

**The tell for a real audit.** They ran the keyboard pass and can say which control they could not reach. A designer who lists only contrast failures ran the extension and nothing else, and the extension is the third of the work that a tool can do.

## C1.1 Type scale

Accept any defensible base and ratio: 16 with 1.25, 16 with 1.2, 17 with 1.125 for a dense flow. Reject a scale with no stated ratio, because that is a list of sizes rather than a scale.

**The part most will skip:** the Devanagari test. Devanagari has taller ascenders and the matra marks sit above the line, so a line height set comfortably for Latin at 1.4 will clip or crowd at the same value. A designer who found this and adjusted line height per script has done the task. A designer whose file shows Latin lorem at every step has not, and it will surface in week 3 when the injection lands.

## C2.1 Colour system

Check three things and nothing else:

1. Every step states a measured ratio, not an estimate
2. The ramp was generated perceptually, not by eyeballing lightness. Uneven steps show up as a mid ramp value that looks muddy against its neighbours.
3. The error, warning, success, and information colours are distinguishable from each other in greyscale. If they are not, C2.3 cannot pass honestly.

## C2.2 Semantic roles

The discriminating question: is there a separate token for focus ring, or is it reusing the primary interactive colour.

Reusing it is acceptable and common, but it must be a stated decision, because the moment a primary button is focused, the ring and the button are the same colour and the ring disappears. A designer who noticed that has understood what the semantic layer is for.

## S1.2 Foundations decision

The output to check is not which scale won. It is whether the rejected ones were recorded with a reason.

**A good record** says: "UX4's scale was rejected because the 1.333 ratio produced only two usable body sizes before the jump to heading sizes, which the address form needs three of". That is a reason another person can evaluate.

**A bad record** says: "we chose UX2's scale". That is a vote, not a decision, and in week 3 nobody will remember why.

## What to do with the strongest and the weakest

**Strongest week 1 audit** gets the file upload component in week 2. They will find the real states.

**Weakest technically** gets the select component. Native versus custom forces them into the accessibility question with no way around it.

**Anyone who started designing screens in week 1** gets one comment on their pull request and nothing else: "show me your problem statement". Do not explain further. They will find it.
