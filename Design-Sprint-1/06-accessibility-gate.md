# The Gates

Three checklists. They apply in every sprint. A deliverable that fails any gate is not done, regardless of how it looks or how close the deadline is.

Answer every line with evidence, not a tick. "Yes" is not an answer. "Tab reaches all 7 controls in visual order, screenshot attached" is.

---

## 1. Accessibility gate

Run on the primary flow of anything claiming done. Based on WCAG 2.2 AA. The criterion number is given so the finding is checkable, not arguable.

### Keyboard and focus

| Check | Criterion | Evidence needed |
|---|---|---|
| Every task completable with keyboard only, no mouse | 2.1.1 | Screen recording or a step by step list of keys pressed |
| No keyboard trap. Focus can always leave a component | 2.1.2 | Which key exits each modal, drawer, and date picker |
| Focus indicator visible on every interactive element | 2.4.7 | Screenshot of focus on 5 different element types |
| Focus indicator meets contrast and is not obscured by sticky headers, footers, or toasts | 2.4.11, 2.4.13 | Screenshot of focus on the element nearest a sticky element |
| Tab order matches visual reading order | 2.4.3 | Numbered screenshot of the tab path |
| Skip link to main content on any page with repeated navigation | 2.4.1 | Where it is and what it skips |

### Contrast and colour

| Check | Criterion | Evidence needed |
|---|---|---|
| Body text 4.5:1 against its background | 1.4.3 | Measured ratio for text primary, secondary, and disabled |
| Large text (24px, or 19px bold) 3:1 | 1.4.3 | Measured ratio |
| UI component boundaries and states 3:1 | 1.4.11 | Measured ratio for input borders, focus ring, icon buttons |
| Colour is never the only carrier of meaning | 1.4.1 | Show the error state with colour removed, still readable |
| Text remains readable at 200 percent zoom, no horizontal scroll at 320px width | 1.4.4, 1.4.10 | Screenshot at 320px and at 200 percent |

### Targets and input

| Check | Criterion | Evidence needed |
|---|---|---|
| Interactive targets 24 by 24 minimum, or spacing exception documented | 2.5.8 | Measured size of the smallest target |
| Every input has a visible persistent label. Placeholder is not a label | 3.3.2 | Screenshot with a field filled, label still visible |
| Autocomplete attribute set on name, address, phone, email fields | 1.3.5 | List of fields and the attribute value |
| Information the user already entered is not asked for again in the same flow | 3.3.7 | Where you carried data forward |
| Any dragging action has a single pointer alternative | 2.5.7 | What the alternative is |
| Authentication does not require a cognitive test such as retyping a code from memory | 3.3.8 | How OTP entry is designed, paste allowed |

### Structure and screen reader

| Check | Criterion | Evidence needed |
|---|---|---|
| Heading levels used in order, one h1 per page, no skipped levels | 1.3.1 | Heading outline written out |
| Landmarks present: header, nav, main, footer | 1.3.1 | Which regions map to which landmark |
| Every icon only button has an accessible name | 4.1.2 | List of icon buttons and their names |
| Images have alt text, or empty alt if decorative | 1.1.1 | Alt text for every informative image |
| Status changes announced without moving focus | 4.1.3 | Which live region announces what |
| Screen reader pass on the primary flow | overall | The announced text written out, screen by screen, with the reader named |

### Motion and time

| Check | Criterion | Evidence needed |
|---|---|---|
| Reduced motion alternative for any animation over 200ms | 2.3.3 | What changes when prefers-reduced-motion is set |
| No animation that flashes more than 3 times per second | 2.3.1 | Confirm none exists |
| Any time limit can be extended, or the user is warned with time to act | 2.2.1 | Session expiry design |
| Content in motion can be paused | 2.2.2 | Carousels, auto advancing steps, live tickers |

### Errors and help

| Check | Criterion | Evidence needed |
|---|---|---|
| Error identifies the field and states the fix in words | 3.3.1, 3.3.3 | Every error message from the inventory |
| Error is announced to a screen reader, not only shown visually | 4.1.3 | How it is announced |
| Destructive or financial actions are reversible, confirmed, or checked | 3.3.4 | Which one applies to the payment step |
| Help is available in a consistent place across the flow | 3.2.6 | Where help lives on each screen |

**Automated tooling note.** axe or Stark catch roughly a third of real issues. Running the tool is not the gate. The keyboard pass and the screen reader pass are the gate.

---

## 2. States gate

Every screen in the flow ships every state that applies to it. Missing state means not done.

| State | The question it answers | Common failure |
|---|---|---|
| Default | What does it look like with normal content | none, everyone does this one |
| First run | What does a brand new user see with nothing yet | shown as an empty grey box with no guidance |
| Empty | What when there is genuinely no data | "no results" with no next action |
| Loading | What during the wait, and at 3, 15, and 45 seconds | one spinner for every duration |
| Partial | What when some data arrived and some did not | not designed at all |
| Success | How does the user know it worked, and what next | a toast that disappears before it is read |
| Error, recoverable | What went wrong, why, what to do | "something went wrong" |
| Error, unrecoverable | What when retry will not help | same screen as recoverable, which lies |
| Offline | What when the network is gone mid task | typed data lost silently |
| Permission denied | What when the user is not allowed | a blank screen or a raw 403 |
| Zero results | What when a search or filter returns nothing | no way back to a result |
| Rate limited or quota | What when the system says slow down | not designed |
| Destructive confirm | What before something irreversible | a browser confirm dialog |
| Session expired | What when the clock ran out | full data loss |
| Long content | What when the text is 3 times longer, or in Hindi | layout breaks |
| Truncated | Where text cuts off and how the user reads the rest | ellipsis with no access to the full value |

For this sprint, the states matrix is committed as a table: rows are screens, columns are states, cells link to the Figma frame or say "not applicable" with the reason.

---

## 3. Evidence gate

Every claim about users traces to a source. Four acceptable sources:

| Source | What it looks like | Strength |
|---|---|---|
| Your own usability test | Task, participants, result, quote | Strongest at this scale |
| Analytics or a measured number | The number, where it came from, the date | Strong for magnitude, weak for why |
| A documented convention from a named system | Carbon, Polaris, HIG, Material, plus the specific page | Medium, it is someone else's context |
| A named heuristic with the user cost spelled out | Nielsen heuristic plus what it costs this user | Weakest, but valid if stated as reasoning not evidence |

**Fails the gate:** "users prefer", "it is best practice", "research shows", "this is more intuitive", "everyone does it this way", any claim citing an article you did not link.

**Passes the gate:** "two of three participants tapped Continue before uploading, and both said they thought the document step was optional, so the step is now blocking with the reason stated".

Weak evidence is allowed as long as it is labelled weak. Overstating evidence is what fails.

---

## 4. Sign off

The deliverable is done when all three gate files are committed and the reviewer can check every claim without asking a question.

```
students/UX{n}/week4/S4-1-gate-result.md      accessibility gate, filled
students/UX{n}/week3/C5-1-states-matrix.md    states gate, filled
evidence cited inline in every task file       evidence gate
```

Core admin signs off. A designer cannot sign off their own gate.
