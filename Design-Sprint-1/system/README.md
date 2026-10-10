# The Shared System

One design system, built by five designers. Not five systems. It starts here in Sprint 1 and is handed forward at each sprint release: the next sprint's `system/` begins as a copy of this one (tasks S5, S10, S15, S20), so every shortcut taken in week 2 is still there in week 20.

**Figma library:** to be added by the week 1 system owner
**Current version:** 0.1.0 pre release
**System owner this week:** see `docs/rotation-log.md`

---

## What is here

| Path | Contents |
|---|---|
| `tokens/primitive.json` | Raw values. Colour ramps, spacing steps, type sizes. Nothing references these from a screen. |
| `tokens/semantic.json` | Roles. What a colour is for, not what it is. Screens reference only these. |
| `components/` | One file per component: anatomy, variants, states, keyboard behaviour, markup, usage. |
| `docs/rotation-log.md` | Who holds critique lead and system owner each week. Filled by the admin. |
| `docs/debt.md` | Shortcuts taken and not yet repaid. Reviewed every sprint. Nothing sits here for 20 weeks. |
| `docs/token-naming.md` | The naming convention, agreed in week 1, not reopened casually. |
| `docs/foundations-decision.md` | Which type scale, spacing scale, and colour system won, and what was rejected. |
| `docs/CHANGELOG.md` | Every change, with who and why. |
| `docs/review-log.md` | Component reviews and what each review caught. |
| `code/` | Empty until Sprint 4, when Storybook arrives. |

## Contribution rules

1. Only the week's system owner merges. Core admin approves on top.
2. One component per pull request.
3. A component is not merged until it has: every state, every variant, keyboard behaviour, screen reader behaviour, semantic markup note, one do and one do not.
4. Never edit a component to fix your own screen. Open a PR against the component with the reason, or note the local override and why the system could not absorb it.
5. A component that only your screen uses is not a system component. Keep it local.

## Component template

Every file in `components/` uses this shape.

```markdown
# Component name

**Status:** draft / stable / deprecated
**Owner at creation:** UX{n}
**Figma:** link to the component set

## Purpose
One sentence. What problem it solves.

## When not to use it
The most useful section in the file. Name the component that should be used instead.

## Anatomy
Named parts, with which are required and which optional.

## Variants
| Variant | When |

## States
default, hover, focus, active, disabled, loading, error, read only. Any state marked
not applicable needs a reason.

## Keyboard and screen reader
- Tab:
- Enter or Space:
- Escape:
- Arrow keys:
- Announced as:

## Markup
Which HTML element, and why that element rather than a div.

## Tokens used
Semantic tokens only. If a primitive appears here, a semantic role is missing.

## Content guidance
Label length, sentence case or title case, what the button text must never say.

## Do
One example.

## Do not
One example, with the reason.

## Changelog
| Version | Change | Why | By |
```

## Sprint 1 target

The component template above is also saved as `components/_TEMPLATE.md`. Copy it.

Eight components by week 4.

| Component | Built in | Why this one |
|---|---|---|
| Button | week 2 | Every screen needs it, and every state question shows up here first |
| Text input | week 2 | Labels, hints, validation, error, all in one place |
| Select | week 2 | Native versus custom is a real decision with a real accessibility cost |
| File upload | week 2 | The hardest component in this flow and the one that fails most |
| Alert or inline message | week 3 | Where error, warning, success, and info converge |
| Step indicator | week 3 | Only if the flow is multi step, which is a week 2 decision |
| Card or summary row | week 3 | The review screen needs it |
| Modal or sheet | week 4 | Focus management, the thing most designers get wrong |

If the cohort decides a component on this list is not needed, remove it and write one line on why. A system with a component nobody uses is worse than a system missing one.

## Open questions

Kept here so they are visible rather than rediscovered.

- Does the select use the native control on mobile. Native wins on accessibility, loses on styling. Decide in week 2 and record it.
- Is the step indicator worth the vertical space at 390px.
- Does dark mode ship in Sprint 1 or wait. Currently: three screens in week 4 as a token test, not a full mode.
