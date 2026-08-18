# Design Sprint 5, Admin

Private. General machinery is in `../Design-Sprint-1-Admin/`. This covers Sprint 5 only.

---

## What this sprint is testing

Whether a designer can design an interface whose main risk is what a person will believe about it.

Everything else this sprint, the density, the keyboard model, the states, is craft they should already have by week 17. The AI surface is the new thing and it is genuinely hard.

## Weekly focus

**Week 17.** Do not let anyone design before the domain study. A designer who does not know what a DSCR is or why bank statement variance matters will design a beautiful screen that an underwriter cannot use, and they will not know why.

C17.2, density, is where Sprint 1 to 4 craft gets tested properly. 38 fields, scannable in 40 seconds, and WCAG 2.2 asks for 24px targets. Those requirements are in tension and the resolution has to be stated, not fudged. A designer who claims both without naming the compromise has not measured anything.

**Week 18.** The week that matters.

C18.1 requires one of the three alternatives to be "do not show the score at all". Enforce it. Designers who have not seriously considered that option have not understood the over trust problem, they have only read about it.

C18.5, anchoring, is where the strongest thinking appears. If the score is visible before the underwriter reads the file, it anchors judgement. Sequencing it after costs time per application, and time is what the underwriter is measured on daily. That tension has no clean answer and the quality of a designer's reasoning about it is the single best signal this sprint produces.

**Week 19.** The failure states are the sprint's honesty check. Model unavailable is not an error, it is a normal condition at 2 to 8 seconds of latency with any real infrastructure. Anyone who designed it as an error toast has designed for the demo.

C19.4, the decline sentence, catches the regulatory misunderstanding. Watch for any sentence that attributes the decision to the model, or that presents a contributing factor as a cause. Both are wrong and both are what most people write first.

**Week 20.** The screen reader pass is not optional and it is not hypothetical: two people at this company use one. Require the announced text written out, verbatim, for the score, confidence, factors, and override.

## The injection

`failure-injections/sprint5.md`. Week 19.

Model latency triples and the confidence score becomes unavailable. Chosen because designers build the AI surface around the capability as described, and this removes half of it two weeks before the defense.

A designer whose design degrades gracefully has designed for a real system. A designer whose entire score presentation depends on a confidence figure that no longer exists has designed for a specification, and the difference is exactly what this sprint is for.

## Defense notes for this sprint

**The adversarial round, and this is the strongest one in the program:**

> "An underwriter approved a ₹12 lakh loan in 11 seconds. Your interface showed a green score. The business defaulted in four months. You are in front of the audit committee. Explain your design."

Hold it. Push twice. What you are looking for is whether they can distinguish between an interface that failed and a human who made a bad decision, and whether they can accept the part that is theirs without accepting the part that is not.

**The best possible answer** names the specific thing in their design that permitted an 11 second approval, states what it would cost to prevent it, and states why they made that trade. The worst answer blames the underwriter. The second worst accepts total blame, because a designer who accepts responsibility for every human decision made in their interface cannot reason about accountability at all.

**Numbers round additions:** the model's stated accuracy per band, their own confidence threshold and what changes below it, latency range, their row height and target size, the WCAG target size minimum, how many fields on screen at rest.

## The failure specific to this sprint

Designers who make the AI look impressive. Confidence rings, animated score reveals, gradient risk bands. Every one of those increases over trust, because visual sophistication reads as epistemic authority.

The question that stops it: "does this make an underwriter more likely to read the file, or less."

The second failure is the opposite and rarer: a designer so worried about over trust that they bury the score to the point where the model is useless and the company has paid for nothing. Both are failures of calibration, which is the actual subject of the sprint.
