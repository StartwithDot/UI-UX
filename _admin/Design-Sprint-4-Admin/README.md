# Design Sprint 4, Admin

Private. General machinery is in `../Design-Sprint-1-Admin/`. This covers Sprint 4 only: the multi-product system for a health tech company, tokens, components, governance and adoption.

---

## What this sprint is testing

Whether a designer can do work that nobody will compliment. Systems work is documentation, governance, and negotiation, and the visible output is a page of JSON.

## Before week 13

- Make sure Sprint 3's `system/` has been released with a changelog and a debt list, and that Sprint 4's `system/` starts as a copy on Day 1.
- Book the external bench for JR4 (Mock interview 2, craft and critique) in week 16.
- Have the injection scenario sealed (`failure-injections/sprint4.md`).

## Weekly focus

**Week 13.** T1.0 is the honest task: do not let anyone skip the divergence cost in favour of a quick token build. The cost is where most designers underestimate by an order of magnitude. Push once: "how many hours does one accessibility fix take, and how many times has this company paid for that same fix in three codebases." Then audit the cohort's own drift from Sprints 1 to 3 from `system/docs/debt.md`; they made that mess and there will be more of it than they expect. Check the export (T1.6) is in the 2025.10 format with structured colour and dimension values, and that a theme switch works in the generated CSS with no component edits.

Check one thing before anything else: does any semantic token reference a raw value. Grep for hex codes in the semantic file. This is the single most common architectural failure and it invalidates the layer.

The two brands question is the interesting one. Patient warmth and clinical density are genuinely opposed. If a designer's answer puts the difference in the primitive layer, they have built two systems and called it one. If it is in the semantic layer, they have understood the architecture.

**Week 14.** Documentation is graded as a product: the peer who builds from the docs alone is the test, and the gap log is the evidence. Check at least one component is documented in Storybook with every state reachable. L-AI4: read the claims-versus-verified table; a designer who found zero AI errors either looked lightly or got lucky.

**Week 15.** The contribution round is the week's real content. Both directions must complete: they accept someone's component and get one of theirs accepted. A designer who only submits has not experienced the other side of governance, which is where the learning is. The deprecation exercise catches something specific: watch for a notice with no migration path, which is a designer breaking three products and calling it a cleanup.

**Week 16.** The adoption pitch is the sprint's hardest task and it is not a design task. Three engineering leads who think their system is fine. The pitch that works names what each team gives up, not only what they gain. A pitch that claims everyone wins is a pitch nobody in that room believes. JR4: the design-system case study is hard to write because the output is invisible. Read it as a stranger; if you cannot tell what decision was theirs, send it back.

## The injection

`failure-injections/sprint4.md`. Week 15, Day 5 morning. A governance failure: something bypassed the process, the process blocked something legitimate, or a team has quietly forked components. The designer's job is to say which of their own rules caused it.

## Defense notes for this sprint

**The handoff round changes character.** The engineer is now a system consumer:

> "I need a component you do not have. My deadline is Friday. Your governance process takes two weeks. What do I do."

The correct answer has an escape path in the governance model already, because a system with no escape path gets forked on the first deadline, and every real system needs a documented way to build something locally and contribute it back later. A designer who says "follow the process" has designed a system that will be bypassed.

**Numbers round additions:** how many tokens in each layer, what a component contribution requires before merge, the ARIA role of their most complex component, how many greys the client had, what their own cohort's drift count was.

**The adversarial round:** "you have spent four weeks on a system and shipped no features. The patient app team shipped six. Justify your existence."

The answer that works uses the accessibility regulatory exposure and the duplicated fix cost, because those are the arguments that survive contact with a company. A designer who answers with consistency and craft has given the answer that gets design systems cancelled.

## The failure specific to this sprint

Two, and they are opposite.

**The librarian.** Beautiful token architecture, immaculate documentation, no consideration of whether any team will adopt it. Catch it by asking who has agreed to use this and what they said.

**The pragmatist who skips the writing.** Good components, no governance, no versioning, no deprecation policy. The system works for four weeks and dies in eighteen months. Catch it in week 15 by asking who decides when two teams disagree.

Both look productive during the sprint. The defense separates them.
