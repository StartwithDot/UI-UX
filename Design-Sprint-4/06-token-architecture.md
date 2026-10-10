# Token Architecture

The three-layer token model in full, with naming rules. Read it in the first LEARN block of week 13, and again before you write your architecture decision record.

---

## The one problem tokens solve

A value used in fifty places should be changeable in one place, and its name should describe its job, not its appearance.

`blue-500` cannot become green. `interactive-default` can. Everything below follows from that sentence.

---

## The three layers

```
 Primitive                Semantic                      Component
 (what it is)             (what it is for)              (where it is used)

 color.blue.500    ──►    color.interactive.default ──► button.primary.background
 color.neutral.900 ──►    color.text.default        ──► input.text
 space.4           ──►    space.stack.md            ──► card.padding
```

### Layer 1: Primitive
Raw values, named for **what they are**. Colour ramps, type sizes, spacing steps, radii, shadows, durations, easings.

- Nothing references anything else. Primitives are the bottom.
- No screen and no component reads a primitive directly. This is the rule everyone breaks.
- Names describe the value: `blue-500`, `space-4`, `radius-md`, `duration-200`.

### Layer 2: Semantic
Roles, named for **what a value is for**. This is where theming lives.

- Every semantic token points at a primitive (or another semantic token). Never at a hex value.
- Screens and components read semantic tokens.
- Names describe a job: `color.text.default`, `color.text.muted`, `color.surface.raised`, `color.feedback.error.text`, `space.stack.md`.
- A theme is a different mapping from semantic tokens to primitives. A brand is a different set of primitives. A density mode is a different mapping for spacing and type.

### Layer 3: Component
Tokens that exist only where a component genuinely needs to diverge from the semantic layer: `button.primary.background`.

- Create one only when a component cannot be expressed by consuming the semantic token directly.
- **A component token for everything is not architecture, it is bureaucracy.**
- Each component token must be justified in a single line.

---

## Naming grammar

```
{category}.{role-or-property}.{variant?}.{state?}
```

| Part | Examples | Rule |
|---|---|---|
| category | `color`, `space`, `font`, `radius`, `shadow`, `motion` | Fixed list. Adding one needs a review. |
| role / property | `text`, `surface`, `border`, `interactive`, `feedback` | Named for the job |
| variant | `default`, `muted`, `inverse`, `error`, `success` | Describes intent, not hue |
| state | `hover`, `active`, `disabled`, `focus` | Only if the state needs its own value |

### Rules

1. **A name must survive its value changing.** If a rebrand would make the name a lie, rename it now.
2. **No hue in a semantic name.** `color.text.error`, not `color.text.red`.
3. **No component name in a semantic name.** `color.interactive.default`, not `color.button.default`.
4. **No value in any name above the primitive layer.** No `16`, no `blue`.
5. **Consistent order.** The same grammar everywhere. If the order differs between colour and space, engineers will make mistakes.
6. **Write the rule down and enforce it in review.** A naming convention nobody checks is a suggestion.

---

## Theming and modes

| Need | Solved by |
|---|---|
| Two brands (patient, clinical) | Different primitives, same semantic names |
| Light and dark | Different semantic-to-primitive mapping |
| Comfortable and compact density | A density scale: `space-comfortable-*` and `space-compact-*` primitives, mapped by a mode |
| High contrast | A third mapping for colour semantics |

If you find yourself redesigning a component to theme it, your architecture has failed. If the difference between two products lives in the primitives, you have two systems. If it lives in the semantics, you have one system with two expressions.

---

## Format

Use the Design Tokens Community Group format, which reached its first stable version (**2025.10**) in October 2025. One vendor-neutral file can feed all three frameworks, and tools such as Figma, Tokens Studio and Style Dictionary can read and write it. The group's own FAQ notes the spec is not on the W3C Standards Track, so treat the core format as stable for production but expect refinements.

In 2025.10 colours and dimensions are **structured values**, not bare strings. Files use the extension `.tokens.json` (or `.tokens`) and the media type `application/design-tokens+json`.

```json
{
  "color": {
    "blue": {
      "500": {
        "$type": "color",
        "$value": { "colorSpace": "srgb", "components": [0.12, 0.37, 0.75], "hex": "#1f5fbf" }
      }
    },
    "interactive": {
      "default": {
        "$type": "color",
        "$value": "{color.blue.500}",
        "$description": "Default colour for links and primary actions"
      }
    }
  },
  "space": {
    "4": { "$type": "dimension", "$value": { "value": 1, "unit": "rem" } }
  }
}
```

A semantic token points at a primitive with the curly-brace reference `{color.blue.500}`. The spec supports modern colour spaces (Display P3, OKLCH and the other CSS Color 4 spaces), which matters for your ramps (see `Leonardo` and OKLCH in `../04-Tools-Setup.md`). A transform tool (Style Dictionary is the common one) turns the file into CSS custom properties, a React Native object, or whatever each platform needs.

Check the current spec at designtokens.org before you finalise. Specs move.

---

## What tokens cannot do

Say this in your decision record. Examples:

- Change a component's **shape** or structure (a 4-sided radius is a token; a stepper that turns vertical is a component variant).
- Fix behaviour. A date picker that fails keyboard access is a component problem, not a token problem.
- Make products agree. Tokens make a decision visible; someone still has to make it.

---

## Deprecating a token

A token is a promise. Removing one without warning breaks every product that reads it.

1. Mark it deprecated in `$description` with the replacement and a removal date.
2. Keep it working for at least one full release cycle.
3. Announce in the changelog.
4. Remove it in a major version.

---

## Checks before you export

- [ ] No semantic token has a hex value
- [ ] No component reads a primitive
- [ ] Every name survives a rebrand
- [ ] Every component token is justified in one line
- [ ] Contrast verified for every text/surface pair in every theme
- [ ] The file validates against the format, and loads in all three frameworks' tooling
