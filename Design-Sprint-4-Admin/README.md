# Design Sprint 4, Admin

Private. General machinery is in `../Design-Sprint-1-Admin/`. This covers Sprint 4 only.

---

## What this sprint is testing

Whether a designer can do work that nobody will compliment. Systems work is documentation, governance, and negotiation, and the visible output is a page of JSON.

## Weekly focus

**Week 13.** S13.3 is the honest task: audit the cohort's own drift from Sprints 1 to 3. They made that mess and there will be more of it than they expect. Do not let anyone skip it in favour of auditing the client's three products, which is safer because it is someone else's fault.

The divergence cost in S13.2 is where most designers underestimate by an order of magnitude. Push once: "how many hours does one accessibility fix take, and how many times has this company paid for that same fix in three codebases."

**Week 14.** Check one thing before anything else: does any semantic token reference a raw value. Grep for hex codes in the semantic file. This is the single most common architectural failure and it invalidates the layer.

The two brands question is the interesting one. Patient warmth and clinical density are genuinely opposed. If a designer's answer puts the difference in the primitive layer, they have built two systems and called it one. If it is in the semantic layer, they have understood the architecture.

**Week 15.** The contribution round is the week's real content. Both directions must complete: they accept someone's component and get one of theirs accepted. A designer who only submits has not experienced the other side of governance, which is where the learning is.

The deprecation exercise catches something specific. Deprecating a component the cohort has used since Sprint 1 means writing a message to people who will be inconvenienced. Watch for a deprecation notice with no migration path, which is a designer breaking three products and calling it a cleanup.

**Week 16.** The adoption pitch in P16.1 is the sprint's hardest task and it is not a design task. Three engineering leads who think their system is fine. The pitch that works names what each team gives up, not only what they gain. A pitch that claims everyone wins is a pitch nobody in that room believes.

## The injection

`failure-injections/sprint4.md`. Week 15, two weeks in.

Engineering rejects the token naming format and requires a different one. Chosen because it tests whether the system was built for one consumer or for change. A designer with a generated pipeline changes a config. A designer who hand named 200 tokens in Figma has three days of manual work and will learn the actual argument for automation in a way no lecture achieves.

## Defense notes for this sprint

**The handoff round changes character.** The engineer is now a system consumer:

> "I need a component you do not have. My deadline is Friday. Your governance process takes two weeks. What do I do."

The correct answer has an escape path in the governance model already, because a system with no escape path gets forked on the first Friday deadline, and every real system needs a documented way to build something locally and contribute it back later. A designer who says "follow the process" has designed a system that will be bypassed.

**Numbers round additions:** how many tokens in each layer, what a component contribution requires before merge, the ARIA role of their most complex component, how many greys the client had, what their own cohort's drift count was.

**The adversarial round:** "you have spent four weeks on a system and shipped no features. The patient app team shipped six. Justify your existence."

The answer that works uses the accessibility regulatory exposure and the duplicated fix cost, because those are the arguments that survive contact with a company. A designer who answers with consistency and craft has given the answer that gets design systems cancelled.

## The failure specific to this sprint

Two, and they are opposite.

**The librarian.** Beautiful token architecture, immaculate documentation, no consideration of whether any team will adopt it. Catch it by asking who has agreed to use this and what they said.

**The pragmatist who skips the writing.** Good components, no governance, no versioning, no deprecation policy. The system works for four weeks and dies in eighteen months. Catch it in week 15 by asking who decides when two teams disagree.

Both look productive during the sprint. The defense separates them.
