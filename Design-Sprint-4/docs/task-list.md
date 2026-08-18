# Sprint 4 Task List

Weeks 13 to 16. **C** Craft, **R** Research, **P** Product, **S** Systems, **F** Spine, **X** Injection.

The client: a health tech company with three products, three teams, and three systems that nearly agree. Patient app, doctor console, admin portal.

---

## Week 13: Audit the damage

**S13.1** Inventory every component across all three products. Same purpose, different implementation, counted. Expect 6 button variants and 4 different date pickers.
→ `students/UX{n}/week13/S13-1-inventory.md`

**S13.2** Cost the divergence. Engineering hours duplicated per year, plus the user cost of a doctor and a patient seeing the same status in two different colours. Estimate, state your method, state your confidence.
→ `S13-2-divergence-cost.md`

**S13.3** Audit the cohort's own system from Sprints 1 to 3. Every inconsistency you all introduced. This is the honest one, because you made it.
→ `S13-3-our-own-drift.md`

**S13.4** Token architecture proposal. Three layers, the rule for what may reference what, and the naming convention with the reason for it.
→ `S13-4-token-architecture.md`

**P13.1** Who is this system for. A design system with no defined consumer becomes a museum. Name the teams, their constraints, and what each one will resist.
→ `P13-1-system-consumers.md`

**F13.1** Why session: design systems as organisational artefacts, not component libraries.
→ `fundamentals/why-sessions/week13-systems.md`

**F13.2** Teardown: a published design system of your choice, its documentation not its components.
→ `fundamentals/teardowns/13-published-system.md`

## Week 14: Build the foundation

**S14.1** The primitive layer. Every raw value, in W3C token format, exported as JSON.
→ `system/tokens/primitives.json`

**S14.2** The semantic layer. Every role, referencing primitives only, never raw values.
→ `system/tokens/semantic.json`

**S14.3** Two brands from one token set. The patient brand and the clinical brand, differing only at the semantic layer.
→ `system/tokens/brands/`

**S14.4** Light and dark for both brands. Four combinations, all passing contrast, all measured.
→ `S14-4-theme-matrix.md`

**S14.5** The rule document. What a product team may reference, what they may not, and what happens when they need something that does not exist.
→ `system/docs/token-rules.md`

**C14.1** Prove the architecture. Take one screen from each of the three products and rebuild it on the token set, in both brands and both themes.
→ `C14-1-proof-screens.md`

**F14.1** Why session: theming, brand expression, and what stays fixed across brands.
→ `fundamentals/why-sessions/week14-theming.md`

**F14.2** Teardown: a multi brand product family.
→ `fundamentals/teardowns/14-multibrand.md`

## Week 15: Components and governance

**S15.1** Build four components to full spec: API, props, states, variants, sizes, accessibility annotations, content guidance, and a do and do not section with real examples.
→ `system/components/`

**S15.2** The composite component. One component built from others, with the composition rules stated. Where does the boundary sit and why.
→ `S15-2-composite.md`

**S15.3** Governance model. Proposal, review, acceptance criteria, versioning, deprecation with a timeline, and who breaks a tie.
→ `system/docs/governance.md`

**S15.4** Contribution round. Take a component request from another designer, build it, and have it accepted. Then submit one and have theirs accepted.
→ `S15-4-contribution-log.md`

**S15.5** Deprecation exercise. Pick a component the cohort has been using since Sprint 1 that should not exist. Deprecate it properly: the reason, the replacement, the migration path, the timeline, and the message to consumers.
→ `S15-5-deprecation.md`

**P15.1** Migration plan. Three products, four engineers, feature work continuing. Sequence it and state what breaks if the order changes.
→ `P15-1-migration-plan.md`

**F15.1** Why session: governance, contribution, and why most design systems die.
→ `fundamentals/why-sessions/week15-governance.md`

**F15.2** Teardown: an open source component library's contribution guide.
→ `fundamentals/teardowns/15-contribution-guide.md`

**F15.3** Whiteboard why. Draw the token architecture from memory and explain what may reference what.

## Week 16: Documentation and defense

**S16.1** The system's front page. What it is, who it is for, how to start, and what to do when it does not have what you need. Written for an engineer joining on Monday.
→ `system/docs/README.md`

**S16.2** Documentation for every component you own, complete enough that nobody needs to ask you a question.
→ `system/components/`

**S16.3** Adoption metrics. How would you know if the system is being used rather than forked. Define the measurement.
→ `S16-3-adoption-metrics.md`

**S16.4** The accessibility annotation set. For each component: role, states, keyboard behaviour, focus management, and announced text.
→ `S16-4-a11y-annotations.md`

**C16.1** One full product surface rebuilt on the system, both brands, both themes, gate passed.
→ `C16-1-rebuilt-surface.md`

**P16.1** The pitch. Ten minutes to three engineering leads who each think their existing system is fine. What they gain and what they give up.
→ `P16-1-adoption-pitch.md`

**F16.1** Explainer, Sprint 4.
→ `fundamentals/explainers/UX{n}-sprint4.md`

**X4.1** Post mortem on the injection.
→ `X4-1-postmortem.md`

**F16.2** Defense, six rounds. The handoff round this sprint is a system consumer, not an engineer building one screen: "I need a component you do not have, my deadline is Friday, what do I do."

---

## What fails review in this sprint

| Answer | Why it fails |
|---|---|
| A semantic token referencing a hex value | The layering exists for exactly this reason |
| A component with no documented API | A component nobody can use without asking you is a private component |
| Governance with no named decision maker | Ties do not resolve themselves |
| A deprecation with no migration path | You have broken three products and called it a cleanup |
| A migration plan that requires feature work to stop | No company will do it, so it is not a plan |
| An adoption metric that counts components published | Publishing is not adoption. Consumption is. |
