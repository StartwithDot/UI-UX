# Sprint 4 — Read First

**Weeks 13 to 16 · Systems, scale, and governance**

---

## What changes from Sprint 3

For three sprints you have been contributing to a design system that someone else maintained. In Sprint 4 you own it — and you own the problem that a design system is not a Figma library. It is a set of decisions about who is allowed to change what, and how a contribution gets rejected.

The technical work is the easy half. The hard half is that other people will use your system wrongly, will not read your documentation, and will fork your component rather than ask you to extend it. Sprint 4 is where you design for that.

---

## The project

A multi-product design system for a fictional company with three products: a customer-facing mobile app, an internal operations tool, and a public marketing site.

Three products is the point. A system for one product is a style guide. A system for three products with genuinely different needs is where every real governance question appears — theming, density, brand divergence, and who wins when two products want opposite things.

---

## Read in this order

| # | File | When |
|---|---|---|
| 1 | `00-READ-FIRST.md` | now |
| 2 | `01-project-brief.md` | before Monday |
| 3 | `02-week13.md` | Monday of week 13 |
| 4 | `03-week14.md` | Monday of week 14 |
| 5 | `04-week15.md` | Monday of week 15 |
| 6 | `05-week16.md` | Monday of week 16 |

Reference: `06-token-architecture.md` — the three-layer token model in full, with naming rules.

---

## The four weeks

| Week | Called | You learn | You produce |
|---|---|---|---|
| **13** | Tokens | Three-layer architecture, naming, theming | A full token set that themes without redesign |
| **14** | Components | APIs, variants, composition, slots | Six components with designed APIs and documentation |
| **15** | Governance | Contribution, review, deprecation · **failure injection** | A governance model and a real deprecation |
| **16** | Adoption | Migration, measurement, and being ignored | An adoption plan with metrics and a migration guide |

---

## The books

**Design Systems** (Alla Kholmatova) — the whole book, weeks 13 to 15. This is the one that is about the human problems rather than the file structure.

**Atomic Design** (Brad Frost) — free online, week 14.

**Expressive Design Systems** (Yesenia Perez-Cruz) — week 15, on the governance and multi-brand parts.

Plus real systems: Polaris, Material 3, Carbon, Spectrum, and GOV.UK. Read their contribution guides and their deprecation policies, not just their component pages. The contribution guide is where the real design of a system lives.

---

## What is harder than Sprint 3

**You will be told your system is not being used.** In week 16 the injection tends to be adoption failure. Two of the three product teams have forked components rather than using yours. Your job is not to be annoyed about it — it is to find out why, and the answer is usually something you did.

**Deprecation is a real deliverable.** You will deprecate a component that other people are using, with a migration path, a timeline, and a communication. Shipping new things is easy. Removing things without breaking people is the skill.

**Documentation is graded as a product.** Not as an afterthought. If a peer cannot use your component correctly from the documentation alone, the component is not done, no matter how good it looks.

---

## What ships at the end of week 16

- A three-layer token set, themed across three products, with naming rules
- Six components with designed APIs, full states, and documentation a stranger can use
- A composition model showing how components combine, and where they must not
- A contribution model with a review process and stated rejection criteria
- One real deprecation, executed with a migration path and a timeline
- An adoption plan with metrics
- A migration guide for one product team
- A governance document naming who decides what
- A post mortem
- 20 learning summaries
- A passed defense

---

## Before Monday

- [ ] Read `01-project-brief.md`
- [ ] Read `06-token-architecture.md`
- [ ] Read the contribution guide of Polaris and of Carbon, and note how they differ
- [ ] Have Design Systems by Kholmatova
- [ ] Look at your own `system/docs/debt.md` from Sprints 1 to 3. You are about to inherit it properly.

Then open `02-week13.md`.
