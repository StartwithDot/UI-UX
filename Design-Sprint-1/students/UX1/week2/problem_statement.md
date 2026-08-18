# Sprint 1, Week 2: Build

**UX1 | Position this week: builder | Theme: real content, real states, no lorem ipsum**

Foundations are decided. Now build. Grey boxes are not mid fidelity. Every label, every button, every error is real text you wrote.

---

## Product and Business

**P2.1** Full flow as a Mermaid diagram: every screen, every decision point, every exit. Include the three failure paths from the brief's user section.
→ `P2-1-flow.md`

**P2.2** Lakshmi cannot receive the OTP because the registered mobile is not hers. Design the path. It cannot end in "visit a centre" without first exhausting what the interface can do.
→ `P2-2-no-otp-path.md`

**P2.3** Address entry: one page or multiple steps. Write both options, the tradeoff, your decision with the reason. Cite a documented convention, a heuristic, or your R1.5 observation.
→ `P2-3-form-structure-decision.md`

## Craft and Interface

**C3.1** Happy path at mid fidelity, 390px. Real content, real labels, real button text.
→ `C3-1-happy-path-mobile.md` plus Figma link

**C3.2** Document guidance screen. Ramesh does not know the document must be in his name. Design the moment he learns that, before he uploads. State how you decided where that moment goes.
→ `C3-2-document-guidance.md`

**C3.3** Address entry screen. Every field needs a label, an example where format is not obvious, and a stated validation rule. List the fields with their rules before you design the screen.
→ `C3-3-address-entry.md`

**C3.4** Upload screen, five states: file too large, wrong format, unreadable photo, interrupted at 60 percent on a bad connection, success.
→ `C3-4-upload-states.md`

**C4.1** Every error this service can produce. Minimum 15. Source from the live flow, the constraint list, the upload rules.
→ `C4-1-error-inventory.md`

**C4.2** Write every error message. Each says what happened, why, what to do next. No error codes as the primary message. No "something went wrong" anywhere.
→ `C4-2-error-messages.md`

**C4.3** Confirmation screen copy. Paid ₹50, waiting up to 30 days. What happens next, when, how they will know, what to do if nothing happens, and how the URN is preserved.
→ `C4-3-confirmation-copy.md`

**C4.4** Three of your messages rewritten for a reader slow in English. Shorter words, same information. Note what you could not simplify and why.
→ `C4-4-plain-language.md`

## Systems and Technical

Component assignment comes from the week 2 system owner (UX3). You get one of: button, text input, select, file upload.

**S2.1** Build your assigned component in the shared system. Every state, every variant, accessibility notes, usage guidance with one do and one do not.
→ `system/components/{component}.md` plus the Figma component

**S2.2** Review one peer's component. Your review must name one thing that will break when someone else uses it.
→ PR comment, logged in `system/docs/review-log.md`

**S2.3** Focus and keyboard behaviour for your component. Where focus goes, what Tab does, what Escape does, what a screen reader announces.
→ inside your component file, Keyboard and screen reader section

**S2.4** Semantic HTML for your component. Which element, and one sentence on why that element and not a div with a click handler.
→ inside your component file, Markup section

## Spine

**F2.1** Why session, Saturday. This week's presenter: **UX2**. Visual hierarchy and whitespace, using one screen from this cohort's week 2 work, rebuilt live.
→ `fundamentals/why-sessions/week02-hierarchy.md`

**F2.2** Teardown: a state electricity board bill payment flow. Same format as week 1.
→ `fundamentals/teardowns/02-electricity-payment.md`

**F2.3** Drill continues. Same log file.

## Done when

- Happy path exists at mid fidelity with zero placeholder text
- Error inventory has 15 entries and every one has a written message
- Your component is merged into `system/` with keyboard and markup sections filled
- Your peer review named something that will break, not something that looks nice
- The no OTP path ends somewhere other than a dead end

## Watch for

The two most common week 2 failures:

1. **Designing the happy path only, then treating states as week 3 cleanup.** States are where the design actually lives. The C3.4 upload task exists to make that unavoidable.
2. **Writing microcopy last.** If you design the screen then fill in the text, the layout dictates the message. Write C4.2 before you finish C3.1 and you will find the screens change.

## Reading this week

- Form Design Patterns, the chapters on validation and error messages
- Refactoring UI, the chapter on working with text
- Your assigned component in Carbon and in Polaris, side by side, before you build yours
