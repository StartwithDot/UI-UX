# Sprint 5: Project Options

**Weeks 17 to 20 | The capstone | Cohort: UX1 to UX5**

*All clients here are fictional and all numbers are invented for the exercise. Choose one option, or propose your own, and get written approval from the admin before week 17.*

---

## How to choose

You are graded on the choice. A project you can defend is part of the work. Ask yourself four questions about each option:

1. **Can I reach five real users twice** (week 17 and week 19)? A project where the users are unreachable is a project where your research is invented.
2. **Which option frightens me least?** Be suspicious of that one. It is probably the one that will teach you least.
3. **Where will my accessibility work be hardest?** Every option has a real accessibility problem built in. Find it before you commit.
4. **Do I know what my baseline number is, or how to get it?** Without a number there is no result to defend.

| Option | Centre of gravity | Hardest part | Best if you want to show |
|---|---|---|---|
| **A** Public health appointments | Low digital literacy, intermittent connectivity, a human in the loop | Designing for a receptionist and a patient at once | Service design and inclusive design |
| **B** Gig worker earnings and disputes | Adversarial interests, trust, money | Deciding whose side the interface is on | Product judgement and ethics |
| **C** School-to-work service | Multiple stakeholders, no prior experience | Designing for someone who does not know what they do not know | Research depth and content design |
| **D** Loan underwriting console | Dense professional UI with an AI score | Informing without deciding | Complex interface craft and AI |

Option D is the only one with a model in it. Everyone completes lab L-AI5 in week 17 whichever option they choose (`../07-AI-In-Design.md`), but Option D designers extend it into their whole capstone.

---

## Option A: A public health appointment system

### The client
A state health department runs a network of 38 district hospitals and 210 primary health centres. Appointments are taken in person, by queue, from 7am. A pilot app exists and was downloaded 41,000 times; 6,300 people booked an appointment through it in three months.

| Fact | Number |
|---|---|
| Patients booked through the app in the pilot | 6,300 |
| No-shows among app bookings | 31% |
| No-shows among walk-in tokens | 12% |
| Average wait at the counter | 2 hours 10 minutes |
| Receptionists per district hospital outpatient department | 3 |
| Share of patients who are over 55 | 44% |

The department's brief: "get more people to use the app."

### The real problem
Higher no-shows in the app than in the queue means the app is making a booking that does not mean what a booking should mean. A patient who books for Thursday and does not know she needs to bring a referral letter, or that the doctor is not there on Thursdays at this centre, does not turn up. The receptionist is currently the entire system: she knows which doctor is on which day, which tests need fasting, and which patients to squeeze in. The app knows none of it.

### The users
- **Kamala, 63, farmer's widow.** Registered mobile number belongs to her son who works in another city. Reads Hindi slowly. Failure mode: a reminder goes to her son's phone and she never knows.
- **Ravi, 29, receptionist.** Sees 90 patients a shift. Failure mode: the app adds a second queue he must manage on top of the first, and he quietly tells people to ignore it.
- **Dr. Sharma, 47.** Wants to see fewer no-shows and more patients with complete referral paperwork. Failure mode: the app's slots do not match his real schedule.

### Constraints
Intermittent 2G; most patients use a feature phone or a shared phone; the registered mobile number is often a relative's; SMS and IVR are cheaper than push; the receptionist must be able to override anything; there are two official languages and several dialects in the catchment.

### The accessibility challenge
Low literacy and low vision at the same time, a shared phone, and a receptionist who is the real screen reader. Voice and numeric flows must work end to end.

### The ethical tension
Reminders and nudges reduce no-shows, but a reminder sent to a relative's phone discloses a patient's health appointment to a third party. Where is the line on privacy against attendance?

### What you need to start
Five patients or carers, one receptionist and one doctor, reachable in person. If you cannot reach a receptionist, do not choose this option.

---

## Option B: A gig worker earnings and dispute tool

### The client
A food-and-grocery delivery platform with 62,000 active delivery partners in 14 cities. Partners are paid per order, with deductions for fuel surcharges, insurance, equipment and penalties.

| Fact | Number |
|---|---|
| Active delivery partners | 62,000 |
| Median partners' deductions as a share of weekly earnings | 11% |
| Partners who file a dispute in a month | 4% |
| Disputes resolved in the partner's favour | 38% |
| Median time to resolution | 9 days |
| Share of partners who say they do not understand at least one deduction | 61% (platform survey) |

The company's brief: "reduce dispute volume."

### The real problem
Reducing dispute volume is easy: make disputing harder. The harder question is whether partners are being deducted correctly. 38% of disputes are upheld, so a large part of the volume is the company's own mistakes. The company's interest (fewer disputes) and the worker's interest (being paid correctly) genuinely conflict, and you have to decide whose interface this is.

### The users
- **Arjun, 26, full-time partner.** Rides 11 hours a day. Looks at his earnings once, at night, on a small phone. Failure mode: sees a lower payout than expected, cannot tell why, and does not have the 20 minutes the dispute form asks for.
- **Fatima, 34, part-time partner.** Delivers around her childcare. Failure mode: misses the 48-hour dispute window while the app is in the background.
- **Mehul, 41, support team lead.** Runs the dispute queue. Failure mode: sees the new tool as a way to be blamed for the 38%.

### Constraints
Dispute window of 48 hours; screen time is minimal while riding; many partners have limited English; the company holds the data, so any "evidence" a worker uploads is weaker than the platform's logs; the company will review any wording the tool shows.

### The accessibility challenge
Use while moving, one-handed, in sunlight, on a cracked low-end screen; dyslexia and low literacy are common; a voice-first path must exist.

### The ethical tension
You are paid by the company. The design can quietly route workers away from disputing, or it can make the 38% visible. Say in writing which you will do and what you will do if the company objects.

### What you need to start
Five delivery partners who will talk to you, ideally outside the company's own channels. If you cannot reach any, do not choose this option.

---

## Option C: A school-to-work transition service

### The client
A non-profit working with 120 government schools. Its programme helps 17-year-olds who are leaving school find paid apprenticeships. Today it works through phone calls, a paper form and a WhatsApp group run by two coordinators.

| Fact | Number |
|---|---|
| Students in the programme this year | 1,900 |
| Started an application | 1,100 |
| Submitted at least one complete application | 410 |
| Offered an apprenticeship | 96 |
| Students who have a personal email address | 22% |
| Students with their own phone | 38% |

The non-profit's brief: "digitise the process."

### The real problem
Digitising a form does not help a student who does not know what an apprenticeship is, does not have a CV, and is applying alongside a parent who does not trust employers. The drop from 1,100 started to 410 submitted is where the real problem is, and nobody knows why. Is it the form, the documents, the confidence, or the family?

### The users
- **Sana, 17.** Top of her class in a small town. Parents want her to marry or work at the family shop. Failure mode: completes a profile, and then her father says no.
- **Mr. Iyer, 52, teacher-coordinator.** Runs the programme alongside teaching. Failure mode: the tool adds an admin task, so he does not use it.
- **Anand, 33, small-factory owner.** Wants a reliable apprentice. Failure mode: receives applications in a format he cannot compare.

### Constraints
Shared phones; no email; documents are often missing or incorrect; employers want a standard format; students under 18 (consent from a parent or guardian is required for any research you do); two languages.

### The accessibility challenge
First-time users with low confidence, reading ability varying widely, and the primary user cannot yet describe their own skills. The content and the micro-copy carry the accessibility burden.

### The ethical tension
You will be tempted to collect more data on minors than the product needs. What is the least you can collect and still work, and who sees it?

### What you need to start
Five students, or if you cannot reach students directly, five recent school leavers aged 18 to 21 plus one teacher. Research involving minors needs written guardian consent and the admin's approval first. Read `../Design-Sprint-2/06-research-ethics.md` again before you choose this option.

---

## Option D: The loan underwriting console

*This is the only option with an AI model in it. L-AI5 (week 17) is a small version of the same case; here you build the whole console.*

### 1. The client

An NBFC lending to small businesses. Loans of ₹50,000 to ₹15,00,000. 200 underwriters, each processing 30 to 60 applications a day.

A model now scores every application before a human sees it. The model outputs a risk band, a confidence figure, and the four factors that most influenced the score. The underwriter decides. The model does not.

The company's brief: "put the AI score in the interface".

That is a one line brief hiding the hardest interface problem in the program.

### 2. The real problem

The model is right about 82 percent of the time in the top band and about 71 percent in the middle band.

Two failure modes, and both are worse than they look:

**Over trust.** The underwriter sees a green score and approves without reading. This is what will happen if the score is presented as a verdict. When the model is wrong, a business that should have been declined gets money it cannot repay, and the underwriter has no defence in an audit because their reasoning was "the score was green".

**Under trust.** The underwriter ignores the score entirely and the company has paid for a model nobody uses. Everything measured stays where it was.

The interface has to land between those, and where it lands is a design decision with a legal consequence.

### 3. Regulatory reality

- The applicant has a right to a reason for a decline, and "the model said so" is not a reason
- The underwriter is accountable for the decision, not the model
- The audit trail must show what the underwriter saw and what they did
- The model's factors are explanatory, not causal, and presenting them as causal is a misrepresentation

That last point is the one designers get wrong. "Your loan was declined because of your bank balance variance" is a statement the model cannot support. The factor contributed to a score. It did not cause a decision.

### 4. The users

**Meena, 29, underwriter, 3 years in.** 45 applications a day, judged on throughput and on default rate. Fast, keyboard driven, has never used the mouse for anything she does often. Failure mode: adopts the score as a shortcut because throughput is measured daily and default rate is measured quarterly.

**Rajesh, 51, senior underwriter, 22 years in.** Does not believe the model. Has seen three risk systems come and go. His judgement is genuinely better than the model in the middle band and worse in the tails, and he does not know that. Failure mode: ignores the score, and teaches the juniors to.

**Priya, 38, credit head.** Needs the portfolio view, the override rate, and to know when the model is drifting. Failure mode: sees only aggregate numbers and never learns that the middle band is where all the disagreement lives.

### 5. What is in an application

38 fields, 6 uploaded documents, a bank statement analysis with 6 months of transactions, GST filing history, an existing loan check, and now the model output. A single application is genuinely dense and cannot be made sparse.

This sprint's craft problem is density done well: 38 fields on one screen that a person can scan in 40 seconds, not 12 wizard steps.

### 6. Constraints

| Constraint | Consequence |
|---|---|
| Model latency is 2 to 8 seconds | The score is not there when the screen loads. Design the wait. |
| Confidence is sometimes unavailable | Design for its absence, not just its presence |
| 45 applications a day per underwriter | Every extra click costs 45 clicks a day. Keyboard first is not a preference. |
| Decisions are legally accountable to the human | The interface cannot imply the model decided |
| Regional language support is not required for this internal tool | One of the few constraints that removes work |
| Screen readers are used by two underwriters in the company | Accessibility here is not hypothetical, it is two named colleagues |

### 7. Success measures

**Primary:** decision quality, measured as default rate at 6 months on approved loans, with throughput held constant. Both halves matter. Speed alone is easy and worthless.

**Input metrics:** time per application, override rate against the model, proportion of decisions where the underwriter opened the bank statement detail, rate of decisions made in under 20 seconds on middle band applications.

**Guardrail:** the proportion of approvals made without opening any supporting evidence must not rise. That is the over trust metric and it is the one that predicts the audit finding.

### 8. Deliverables by week

| Week | Ships |
|---|---|
| 17 | Domain study, information hierarchy for 38 fields, density strategy, keyboard model |
| 18 | The AI surface: score presentation, confidence, factors, uncertainty, and the wait |
| 19 | Error and edge cases, model unavailable, model wrong, override flow, explanation to the applicant |
| 20 | Full console, screen reader pass, decision record, defense |

### 9. The three hard questions

Answer all three in writing, and expect to be attacked on all three at the defense.

**How do you present a score so it informs without deciding.** Consider not showing the number at all. Consider showing it only after the underwriter forms a view. Consider showing the factors without the score. Each of those has a cost. Pick one and own the cost.

**How do you present confidence to someone who does not think in probability.** 71 percent means nothing useful to a person deciding one case. It is a statement about a population, not about this application. Anything you design here is a translation, and every translation loses something. Say what yours loses.

**What does the applicant get told.** The underwriter declined. The model contributed. The applicant is entitled to a reason. Write the actual sentence.

### 10. Reading

Assigned:
- People + AI Guidebook, Google, fully
- Microsoft Human AI Interaction Guidelines, all 18
- Apple Human Interface Guidelines, Machine Learning section
- The RBI guidance on digital lending, the sections on transparency and grievance
- Data driven design and enterprise density: Few, and any two dense professional tools studied properly

Full list: `../03-Books-And-Resources.md`.

---

## Or propose your own

It must have all four: **real users you can reach**, **genuine constraints**, **a real accessibility challenge**, and **an ethical tension**. Your proposal is one page and is due before week 17. It is approved or rejected.

| Section | What it must say |
|---|---|
| The problem | In one sentence, as a user problem. No solution words. |
| Users | Who, how many you can reach, how you will reach them. Name five by code. |
| The number | Your baseline metric, or how you will get it in week 17. |
| Constraint | The one that will hurt most |
| Accessibility challenge | The real one, not "make it accessible" |
| Ethical tension | Where the design could harm someone |
| Why it fits four weeks | And what you will cut first |

A proposal fails if the users are unreachable, the scope is a product rather than a flow, or the ethical tension is missing.

If you want to run a live project with a real client, read `../06-Job-Readiness-Track.md` section 7. All four conditions apply.
