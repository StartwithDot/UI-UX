# Critique Guide

Day 4, 90 minutes, every week. Run by that week's critique lead. Applies to every sprint.

Critique is the highest value hour in the program because it is the same skill as the app critique interview round and the same skill as design review at work.

---

## 1. Format

| Segment | Time |
|---|---|
| Critique lead states the week goal and the rule | 3 min |
| 5 designers present, 12 min each: 5 present, 7 feedback | 60 min |
| Cross cutting patterns: what did more than one person get wrong | 15 min |
| Actions and log | 12 min |

Every designer presents every week, including the critique lead. In progress work is the point. Nothing is too unfinished to critique.

## 2. How to present, 5 minutes

1. **The problem, one sentence, before showing anything.** If you cannot state it in one sentence you do not have it yet.
2. **What you rejected.** One minute. Showing only the final option hides the thinking.
3. **What you are showing.** Two minutes.
4. **The question.** State the specific thing you want examined. "Feedback welcome" wastes the room.

Then stop talking and write.

## 3. How to give feedback

A valid comment has three parts: the observation, the principle, and the user cost.

**Valid**
> "The document rule appears after the upload step. That is a mismatch between system and real world order. Ramesh pays ₹50 and waits nine days before learning his bill is not in his name."

**Valid**
> "This input has no disabled state in the system. The payment screen needs one during processing, so someone will build a one off and the system will fork."

**Valid**
> "You say users found it confusing. Which participant, which task, what did they do."

**Invalid**
> "Looks clean." "I would use a different blue." "Not sure I like the spacing here." "This feels off."

If you cannot name the principle or the cost, you are stating a preference. Preferences are allowed only when labelled as such and they do not count toward your review requirement.

## 4. How to receive feedback

- Write everything. Do not respond in the room beyond a clarifying question.
- Do not explain why the comment is wrong. If it is wrong, that will be true tomorrow too.
- Do not thank each comment individually, it eats the clock.
- On Day 5, decide what to act on. You are allowed to reject feedback. You are not allowed to reject it silently: `S3-2-wont-fix.md` exists for that.

The instinct to defend live is the single biggest waste of critique time. A comment you can defend instantly is usually a comment you have not understood yet.

## 5. Rules the critique lead enforces

1. No comment without a principle and a user cost
2. No redesigning in the room. Naming the problem is the job, proposing the whole solution is not
3. Nobody speaks twice until everyone has spoken once
4. Time is fixed. Five people at 12 minutes, no negotiation
5. The presenter does not defend
6. Every session names at least one thing that is working and why it works, because the reason is the transferable part

## 6. The critique log

Committed straight away by the critique lead: `delivery/design/critique-log-weekNN.md`.

```markdown
# Critique log, week NN
Lead: UX3 | Date: | Present: UX1 UX2 UX3 UX4 UX5

## UX1
Showed: document guidance screen
Top comments:
1. Rule appears after upload, mismatch with real world order, costs ₹50 and 9 days (raised by UX4)
2. Icon button has no accessible name (raised by UX2)
Actions: 2 accepted, 1 rejected with reason
Working well: the rejection reason screen turns a code into an action

## UX2
...

## Cross cutting
Three of five put help behind an icon with no label. Assign the accessible name check to the system button component.

## Review quality
UX5 approved two PRs with no substantive comment. Flagged.
```

The cross cutting section is what makes this log worth keeping. A mistake three people made is a system or curriculum problem, not five individual problems.

## 7. Teardown, the other half of the skill

Day 6, one product surface, 60 minutes. Assigned by admin, never chosen by the presenter, because choosing means picking something easy.

Format per finding, committed to `fundamentals/teardowns/NN-subject.md`:

| Column | Content |
|---|---|
| The flaw | What is observably wrong, with a screenshot |
| The principle | Named heuristic, WCAG criterion, or documented convention |
| The user cost | Who loses what, in time, money, or access |
| The fix | Specific enough to build |
| The cost of the fix | Engineering effort, a policy change, or a tradeoff against another user |

Minimum 6 findings, of which at least one must be an accessibility failure with the criterion number, and at least one must be a case where you think the flaw is a deliberate business decision rather than an oversight. That last one teaches the most.

**Teardowns must include something that works.** One finding per teardown names a good decision and explains what would break if it were changed. Only being able to see flaws is a junior trait.

## 8. Assigned teardown subjects, Sprint 1 to 6

Assigned in this order so the difficulty rises and the domains vary.

| Week | Subject | Why this one |
|---|---|---|
| 1 | IRCTC ticket booking | Density, time pressure, error recovery |
| 2 | State electricity bill payment | Payment, receipts, confirmation |
| 3 | Any insurance claim submission | Document upload, long forms, high stakes |
| 4 | A subscription cancellation flow | Dark patterns and the regulation boundary |
| 5 | Passport Seva appointment booking | Availability, slots, cancellation |
| 6 | A hospital appointment app | Vulnerable users, urgency, trust |
| 7 | Income tax e-filing portal | Complexity, terminology, expert versus novice |
| 8 | A UPI payment app confirmation flow | Irreversibility, confidence, speed |
| 9 | Zomato or Swiggy checkout | Persuasion, defaults, upsell, honesty line |
| 10 | An airline booking with seat selection | Add-on pricing, choice architecture |
| 11 | Any cookie consent surface in India and in the EU | Consent, DPDP versus GDPR, deceptive design |
| 12 | A bank onboarding and KYC flow | Identity, compliance, abandonment |
| 13 | Figma itself | Complex tool UI, keyboard, discoverability |
| 14 | GitHub pull request review | Dense information, expert workflow |
| 15 | Notion onboarding | Empty states, template patterns |
| 16 | Stripe dashboard | Enterprise data density done well |
| 17 | ChatGPT or Claude interface | AI surface, latency, correction, refusal |
| 18 | GitHub Copilot or Cursor inline suggestion | AI as inline suggestion, not chat |
| 19 | Google Search AI overview | Provenance, citation, confidence |
| 20 | A shopping site recommendation surface | Algorithmic transparency, trust |
| 21 | Your own Sprint 1 work | You have grown, prove it |
| 22 | A peer's Sprint 3 work | Critique of a peer, in writing, kindly and precisely |
| 23 | A shipped case study from a company portfolio | Critique the narration, not the pixels |
| 24 | Your own portfolio | Last one, and the hardest |
