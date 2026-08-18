# Sprint 4 Project Brief: Three Products, One Company

**Weeks 13 to 16 | Track focus: Systems | Cohort: UX1 to UX5**

---

## 1. The client

A health tech company, seven years old, 340 employees. Three products:

| Product | Users | Built | Stack |
|---|---|---|---|
| Patient app | 2.1 million | 2019, outsourced | React Native |
| Doctor console | 14,000 doctors | 2021, in house | React web |
| Admin portal | 900 hospital staff | 2022, acquired with a company | Vue |

Three teams, three systems, three sets of decisions made independently, none of them written down.

## 2. The evidence of the problem

An audit last quarter found:

- 6 button implementations, 4 of which have different focus behaviour
- 4 date pickers, 2 of which cannot be operated by keyboard
- 3 different colours in use for "urgent"
- 19 distinct greys
- The same status, "awaiting review", rendered amber in one product and grey in another
- Accessibility fixed once in the doctor console and never propagated

The last two are the ones with teeth. A doctor sees amber and treats it as needing attention. The same record in the admin portal is grey and reads as inactive. That is not a consistency problem, it is a clinical communication failure that happens to look like a styling issue.

## 3. What the company thinks the problem is

"We need a design system."

They have three. The problem is not the absence of a system, it is the absence of a shared one, and more precisely the absence of any agreement about who decides. A fourth system built by a fourth team solves nothing and the company will have paid for it.

## 4. What is actually true

| Fact | Consequence |
|---|---|
| Three different frameworks | The system cannot be a component library in one framework. It has to be tokens plus specification. |
| Three teams with three roadmaps | Nobody will stop feature work to migrate |
| The acquired team did not choose this | Resistance is a design problem, not a compliance problem |
| Accessibility is a regulatory exposure in health | The strongest available argument for adoption, and it is not a design argument |
| Two brands: patient facing and clinical | One token set has to serve both without either looking borrowed |

## 5. Constraints

| Constraint | Consequence |
|---|---|
| React Native, React, Vue | Tokens in a format all three consume. W3C format, JSON, not a Figma library alone. |
| No engineering resource dedicated to migration | Incremental adoption or nothing |
| Clinical safety requires colour to be unambiguous | The semantic layer carries real risk here |
| Patient app supports 8 languages | Type and layout tokens must survive script changes |
| Regulatory audit in 9 months | Gives you the deadline and the leverage |

## 6. Success measures

**Primary:** proportion of shipped surfaces consuming the shared token set. Define what counts as consuming and what counts as forking.

**Input metrics:** number of components adopted per team, time from a component request to acceptance, number of forks created, colour values in use outside the token set.

**Guardrail:** feature velocity must not fall in any of the three teams. A system that slows the teams down gets abandoned in a quarter, whatever its quality.

## 7. Deliverables by week

| Week | Ships |
|---|---|
| 13 | Full audit, divergence cost, token architecture proposal, consumer analysis |
| 14 | Primitive and semantic layers, two brands, two themes, three proof screens |
| 15 | Four documented components, composite, governance, contribution round, deprecation, migration plan |
| 16 | Full documentation, adoption metrics, one rebuilt surface, adoption pitch, defense |

## 8. The part that is not design

Half of this sprint is politics and writing. The governance model, the deprecation notice, the migration sequence, and the adoption pitch are all documents whose audience is a team that did not ask for this.

A component library with excellent components and no governance is dead in eighteen months. Everyone in this sprint will have seen that happen by the time they are five years in, and the ones who understood it in week 15 will be the ones who prevent it.

## 9. The two brands

**Patient:** warm, reassuring, non clinical. Larger type, more space, softer colour. The user is anxious and possibly unwell.

**Clinical:** dense, precise, fast. A doctor sees 40 patients a day and needs 30 records on one screen. Warmth here reads as wasted space.

These are genuinely opposed requirements. One token set has to serve both, and the interesting question of this sprint is which layer the difference lives in. If the difference is in the primitives, you have two systems. If it is in the semantics, you have one system with two expressions.

## 10. Reading

Assigned:
- Design Systems, Alla Kholmatova, fully
- The W3C Design Tokens Community Group format specification
- Expressive Design Systems, Yesenia Perez-Cruz
- Two published system documentation sites, read as documentation not as inspiration
- The WAI-ARIA Authoring Practices patterns for the components you build

Full list: `../../Learning Resources.md` Sprint 4 section.
