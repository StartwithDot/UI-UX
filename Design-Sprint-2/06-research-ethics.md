# Research Ethics

Read before you contact a single participant. Not a formality. The participants in this sprint are people who tried to get vocational training and did not, which means asking them about it touches something that cost them.

---

## 1. Consent

Every session needs consent, taken before recording starts, in the participant's language, spoken and confirmed rather than only signed.

What consent must state:

1. Who you are and that this is a student program, not the government
2. What you are studying and why
3. That participation is voluntary and they can stop at any moment without giving a reason
4. That they can skip any question
5. What you are recording, audio, video, or notes
6. Where it will be stored, who can see it, and for how long
7. That they can withdraw afterwards and have their data removed
8. That nothing they say affects their eligibility for the scheme, because they will assume it does

Point 8 is the one people forget and it is the one that most distorts answers. Someone who thinks their answers affect a government benefit will tell you the scheme is excellent.

## 2. The power imbalance

You are a designer with a laptop asking someone who did not get training why they did not get it. That is not a neutral conversation.

What follows from that:

- Never imply you can influence their enrolment, because you cannot
- Never ask why they failed. Ask what happened.
- Do not push when someone deflects. A deflection is data.
- If someone becomes distressed, stop. The session is over. Do not resume it, and do not use partial data from it unless they confirm afterwards.
- Compensate where you can. Time is not free. If the program cannot pay, say so upfront rather than after.

## 3. What you may not do

| Never | Why |
|---|---|
| Record without consent | Illegal in effect and disqualifying in this program |
| Use anyone's Aadhaar number, real or in a screenshot | Identity data, no exceptions |
| Store personal data in the public repo | It is a public repository, permanently, and searchable |
| Share a transcript with real names | De-identify before anything leaves your machine |
| Use a quote that identifies someone by circumstance | "the woman at the Nagpur centre whose brother works there" identifies her |
| Report a finding from a session the participant later withdrew | This is the week 7 injection, and it is a real situation |
| Present a paraphrase as a quote | A quote is verbatim. Anything else is a summary and gets labelled as one. |

## 4. De-identification

Participants get IDs, not names. `P1` through `P5` inside your own set, with your designer code prefixed when findings merge across the cohort: `UX3-P2`.

The mapping from ID to person lives in one place only: a local file, never committed, never shared, deleted at the end of the sprint.

What has to be removed or generalised from a transcript before it is committed:

| Remove | Replace with |
|---|---|
| Name | P{n} |
| Exact age | a range, "mid twenties" |
| Village or specific locality | "a tier 3 town in the district" |
| Employer name | "a private security firm" |
| Family member roles that identify them | generalise, or remove |
| Phone number, Aadhaar, bank details, ID numbers | remove entirely, never paraphrased |

## 5. Storage

| Data | Where | Deleted |
|---|---|---|
| Raw recording | Your machine only, never uploaded | End of sprint |
| ID to name mapping | Your machine only, one file | End of sprint |
| De-identified transcript | The repo, committed | Retained |
| Findings | The repo, committed | Retained |
| Consent record | Your machine, plus a committed log stating consent was taken, with the ID and date | Consent record end of sprint, log retained |

## 6. Interviewing, the parts that are ethics rather than technique

**Silence is allowed.** Three seconds of silence feels long and it is where the real answer arrives. Filling it with a follow up question is the most common way a designer destroys their own data.

**Do not correct them.** If a participant misunderstands the scheme, that misunderstanding is the finding. Explaining the correct version ends the finding and starts a briefing.

**Do not thank them for the answer you wanted.** "That's really helpful" after one answer and nothing after another teaches them what to say for the rest of the session.

**Ask about the last time, not about generally.** "Tell me about the last time you tried to enrol" produces an event. "How do you generally feel about enrolment" produces an opinion, and opinions are what the client already has.

## 7. What to do when someone tells you something you cannot act on

It will happen. Someone will tell you the centre coordinator asked for money, or that the certificate did not get them a job, or something worse.

- Record it if it is within consent
- Do not investigate it, you are not equipped to and it is not your role
- Do not name the person to the client
- Raise it with the core admin privately, the same day
- If it is a safeguarding matter, the admin decides the escalation, not you

## 8. The consent script

Use this, in the participant's language, adapted for a real voice rather than read aloud.

> "Thank you for the time. I am a design student. I am not from the government and I have no role in the scheme, so nothing you say here changes anything about your enrolment or eligibility, in either direction.
>
> I want to understand what actually happened when you tried to join the training. There are no right answers. I am not testing you, I am trying to find out where the process failed people.
>
> I would like to record the audio so I do not have to write while you talk. Only I will hear it, and I will delete it in four weeks. In anything I write, you will be P2, not your name. Is recording alright with you.
>
> You can stop at any time, skip any question, and if you tell me afterwards you want your information removed, I will remove it. Do you have any questions before we start."

Then wait. Do not start recording until they answer.

## 9. The check

Before you commit any research file, answer these:

1. Could a person be identified from this, by someone who knows them
2. Is every quote verbatim
3. Does every finding name its participant IDs
4. Is the confidence level stated
5. Is there any personal data in here at all
6. Did every participant in this file consent, and is that logged

Six yeses, or four yeses and two definite nos for questions 1 and 5. Anything else, do not commit.
