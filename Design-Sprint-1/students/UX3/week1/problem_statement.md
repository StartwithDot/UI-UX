# Sprint 1, Week 1: Frame

**UX3 | Position this week: builder | Theme: understand before designing**

Nothing gets designed this week. You audit what exists, reframe a bad brief, and build the foundations the whole cohort will use.

Read `../../../docs/project-brief.md` first. Then use the live service at `myaadhaar.uidai.gov.in` before writing a single word.

---

## Product and Business

**P1.1** The department's brief is "make it so people stop coming to the counter". Write the three questions that brief does not answer. For each, state who could answer it and how long that would take.
→ `P1-1-brief-questions.md`

**P1.2** Rewrite the brief as a problem statement: [user] cannot [job] because [obstacle], which costs [cost to user] and [cost to department]. One paragraph. No solution words in it.
→ `P1-2-problem-statement.md`

**P1.3** List every constraint from the brief plus three you found by using the live service. Mark each as fixed policy, technical, or assumed.
→ `P1-3-constraints.md`

**P1.4** Name the primary metric, two input metrics, and one guardrail metric. For the guardrail, one sentence on what bad design would look like if only the primary metric mattered.
→ `P1-4-metrics.md`

## Research and Evidence

**R1.1** Walk the live flow on a phone. Screenshot every screen including every error you can trigger. Do not use anyone else's Aadhaar number.
→ `R1-1-current-flow-screens/` plus `README.md` listing screens in order

**R1.2** Heuristic evaluation against Nielsen's 10 heuristics. Table: screen, heuristic violated, what the user experiences, severity 1 to 4. Minimum 12 findings. "Looks outdated" is not a finding.
→ `R1-2-heuristic-audit.md`

**R1.3** Accessibility audit of the live flow. Keyboard only pass, contrast on 5 elements, focus visibility, form label check. State the WCAG 2.2 criterion for each failure.
→ `R1-3-accessibility-audit.md`

**R1.4** Your three worst findings. For each, the user cost in one sentence a department official would understand. No design jargon.
→ `R1-4-worst-three.md`

**R1.5** Watch one real person attempt the live flow. Do not help them. Note hesitation, what they say out loud, where they stop. 20 minutes maximum.
→ `R1-5-observation.md`

## Craft and Interface

**C1.1** Build a type scale. Base size, ratio, every step with its use. Test with Devanagari at every step and note where it breaks.
→ `C1-1-type-scale.md` plus Figma link

**C1.2** Build a spacing scale. Base unit and every step. For three steps, name a specific place in this flow where that step is right.
→ `C1-2-spacing-scale.md`

**C1.3** One long paragraph at three measures. Screenshot all three, state which is right and why, in line length and reading terms, not preference.
→ `C1-3-measure-test.md`

**C1.4** Take one live screen. Rebuild it with no colour, only type, weight, spacing. Hierarchy readable in greyscale.
→ `C1-4-greyscale-hierarchy.md` plus Figma link

**C2.1** Colour system: 10 step neutral ramp, primary ramp, semantic colours for success, warning, error, information. Use Leonardo. Every step states its contrast ratio against white and against your darkest neutral.
→ `C2-1-colour-system.md`

**C2.2** Map colours to semantic roles: page background, surface, border, text primary, text secondary, text disabled, interactive default, hover, pressed, focus ring, error text, error surface.
→ `C2-2-semantic-roles.md`

**C2.3** Prove your error colour works for deuteranopia and for bright sunlight at low brightness. Show what carries the meaning when colour does not.
→ `C2-3-colour-independence.md`

## Systems and Technical `[MILESTONE]`

Cohort session, Thursday after critique. The week 1 system owner commits, everyone participates.

**S1.1** Agree one token naming convention. Three correct examples, three incorrect with the reason.
→ `system/docs/token-naming.md`

**S1.2** Five type scales, five spacing scales, five colour systems now exist. Pick one of each or synthesise. Record what was rejected and why. Not reopened after week 2 without a decision record.
→ `system/docs/foundations-decision.md`

**S1.3** Write the agreed foundations as token JSON, primitive and semantic layers.
→ `system/tokens/primitive.json`, `system/tokens/semantic.json`

**S1.4** Set up the shared Figma library with variables and modes. Light mode only.
→ `system/docs/README.md`

## Spine

**F1.1** Why session, Saturday. This week's presenter: **UX1**. Gestalt principles, every example taken from the live Aadhaar flow, not a textbook diagram.
→ `fundamentals/why-sessions/week01-gestalt.md`

**F1.2** Teardown: IRCTC ticket booking. Minimum 6 findings. One must be an accessibility failure with the criterion number, one must be a flaw you believe is a deliberate business decision, one must name something that works and what would break if it changed.
→ `fundamentals/teardowns/01-irctc.md`

**F1.3** Drill, daily, 10 minutes. Rebuild one component from any real Indian product from memory, then compare. One line per day.
→ `fundamentals/drills/UX3-log.md`

## Your position this week: critique lead

- Run Thursday critique, 90 minutes. Rules in `../../../docs/critique-guide.md`.
- Every comment names a principle and a user cost. Stop the session if it drifts into taste.
- Review all peer pull requests this week.
- Commit the critique log the same day: `delivery/design/critique-log-week01.md`
- Include the cross cutting section. A mistake three people made is a curriculum problem, not three individual problems.

## Done when

- Every file above is committed with the AI disclosure line
- R1.2 has 12 findings minimum, each with a severity and a user cost
- R1.3 names a WCAG criterion for every failure, not a general complaint
- The cohort has one agreed type scale, spacing scale, and colour system in `system/`
- Critique log committed with the cross cutting section filled

## Reading this week

Assigned, not optional:
- Refactoring UI, chapters on hierarchy and spacing
- Practical Typography, the key rules summary
- WCAG 2.2 quick reference, AA criteria only
- Nielsen's 10 usability heuristics

Full list with tiers: `../../../../Learning Resources.md` Sprint 1 section.
