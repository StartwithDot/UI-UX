# Sprint 1 — Glossary

Every term used in Sprint 1, defined plainly. If a task uses a word you do not know, it is here.

Terms are grouped by where you meet them. Each definition includes the tradeoff or the reason, because in the defense you will be asked for the tradeoff and not the definition.

---

## Typography

**Type scale** — A small, fixed set of font sizes chosen in advance, usually generated from a base size and a ratio. You use only these sizes. The value is that you stop choosing sizes by eye, so 20 screens stay consistent and each decision takes no time.

**Ratio** — The multiplier between steps in a type scale. 1.2 is calm and good for dense interfaces. 1.25 is a safe default. 1.333 and above escalate quickly and are better for marketing pages than for forms.

**Line height / leading** — The vertical space from one baseline to the next. Expressed as a multiple of font size. Large text wants tight line height (1.1–1.2) because the lines are already visually separated; body text wants loose (1.5–1.6) so the eye can find the next line.

**Measure** — Line length, counted in characters. 45–90 characters is workable, 60–70 is comfortable. Too narrow forces constant return sweeps; too wide makes the eye lose its place on the return.

**Font weight** — The thickness of the strokes. 400 is regular, 500 medium, 600 semibold, 700 bold. Two or three weights is enough for an entire interface. More weights is usually an attempt to fix hierarchy that should have been fixed with size or colour.

**Devanagari** — The script used for Hindi, Marathi, and others. Relevant to Sprint 1 because Devanagari has taller ascenders and lower descenders than Latin, so a line height that works for English can clip Hindi. Any Indian government service must be tested in both.

**Baseline** — The invisible line that letters sit on. Aligning to baselines rather than to box edges is why professional layouts feel settled.

---

## Colour

**Ramp** — A series of steps of one hue from light to dark, usually 10 steps numbered 50 to 900. Having a full ramp before you design means you never invent a colour mid-screen.

**Perceptually even** — Steps that *look* equally spaced to the eye rather than being mathematically equally spaced in RGB. Human vision is non-linear in lightness, so mathematically even steps look uneven. Tools like Leonardo generate perceptually even ramps.

**Semantic colour** — A colour named for its job, not its hue. `error-text` rather than `red-600`. The point is that the job never changes but the value can, which is what makes theming and dark mode possible.

**Primitive token** — The raw value. `blue-500: #3B82F6`. Means nothing on its own.

**Semantic token** — A role pointing at a primitive. `interactive-default: blue-500`. This is the layer components use.

**Contrast ratio** — The measured difference in relative luminance between two colours, expressed like 4.5:1. WCAG AA requires 4.5:1 for body text, 3:1 for large text and for meaningful non-text elements.

**Non-text contrast** — WCAG 1.4.11. Borders, icons, focus rings, and any graphic that carries meaning need 3:1. This is the criterion most often missed, because people check text and stop.

---

## Layout and hierarchy

**Visual hierarchy** — The order in which a viewer notices things, created deliberately. Built from size, weight, colour, and space. Using all four at once on the same element is usually a sign the hierarchy is not working.

**De-emphasising** — Making the unimportant recede instead of making the important louder. Often the better move, because the loud version has nowhere left to go.

**Spacing scale** — A fixed set of spacing values, e.g. 4, 8, 12, 16, 24, 32, 48, 64. Non-linear at the top end, because adjacent steps need to be visibly different or the scale gives no useful choice.

**Proximity (Gestalt)** — Things placed close together are read as related. This is why the gap between a label and its own input must be smaller than the gap between two different fields. Get this wrong and users read the label as belonging to the field above.

**Common region (Gestalt)** — Things inside a shared boundary are read as a group, even if they are not close together. Cards work because of this.

**Figure-ground** — What the eye reads as the subject and what it reads as the background. Modals rely on it; a modal with a weak overlay fails at it.

**Optical alignment** — Adjusting alignment by eye rather than by coordinate, because round shapes and pointed shapes need to overhang slightly to look aligned. Mathematically aligned is not always visually aligned.

---

## Forms

**Label** — The permanent visible text naming a field. Above the field on mobile. Programmatically linked to the input, which is what makes a screen reader announce it.

**Placeholder** — Grey text inside an empty field. Not a label. It disappears the moment the user starts typing, which is exactly when they need it, and it usually fails contrast. Use it for an example format at most.

**Hint text / help text** — Persistent guidance below the label, explaining the format or the rule. Persistent is the key word: it survives typing and it survives errors.

**Inline validation** — Validating a field as the user leaves it, rather than on submit. Good for formats the user cannot guess (PIN, IFSC). Bad on every keystroke, where it tells people they are wrong while they are still typing.

**Error summary** — A block at the top of a form listing every error, each linking to its field. The GOV.UK pattern. It exists because an error at the bottom of a long form is invisible, and because screen reader users need to know how many things failed.

**One thing per page** — Splitting a form so each screen asks one question. Lowers cognitive load and makes error recovery cheap. Costs page loads, which matters on a slow connection. That tradeoff is the whole of task P2.3.

**Progressive disclosure** — Showing only what is relevant now, revealing more as needed. Reduces perceived complexity. The risk is hiding something the user needed to see in order to decide.

---

## States

**States matrix** — A grid of screens against possible states, used to find the states you forgot. The number of empty cells is a more honest measure of a design's completeness than the number of screens.

**Empty state** — What a screen shows when there is no content. A good one says what belongs here, why it is not here, and what to do. "No data" is a failed empty state.

**Loading state** — What is shown while waiting. Chosen by expected duration: under 1s show nothing, 1–3s a skeleton or spinner, 3–10s progress with a message, over 10s do not make them wait at all.

**Skeleton screen** — A grey placeholder in the shape of the content that is coming. Better than a spinner when the layout is predictable, because it prevents layout shift and it sets an expectation.

**Partial state** — Some content loaded, some not. Common in real systems and almost never designed. It is not the same as loading, and it is not an error.

**Optimistic UI** — Showing the result as though the action succeeded, before the server confirms. Feels instant. Requires you to design what happens when it turns out to have failed, and that design is usually skipped.

**Idempotent** — An operation that produces the same result whether it runs once or five times. Matters in Sprint 1 at the moment a user submits, loses connection, and taps submit again. If submission is not idempotent, they may pay twice.

**Destructive confirm** — A confirmation step before something irreversible. It must name what will be lost, specifically. "Are you sure?" names nothing.

---

## Accessibility

**WCAG** — Web Content Accessibility Guidelines. Level A is the minimum, AA is the standard almost everyone commits to and the one this program uses, AAA is stricter and rarely required in full.

**Success criterion** — One numbered, testable requirement, e.g. 1.4.3 Contrast (Minimum). Cite these by number. "This is inaccessible" is an opinion; "this fails 1.4.3 at 2.85:1" is a finding.

**Focus** — Which element currently receives keyboard input. Only one at a time.

**Focus visible (2.4.7)** — You can see which element has focus. `outline: none` with no replacement is the single most common accessibility failure in shipped products.

**Focus order (2.4.3)** — The sequence Tab moves through. Must match the visual reading order, or the interface makes no sense to a keyboard user.

**Focus trap** — Keeping keyboard focus inside a modal while it is open. Correct behaviour for modals. It becomes a bug when there is no way out, so Escape must always work.

**Accessible name** — What a screen reader announces for an element. An icon button with no accessible name announces as "button", which is useless.

**ARIA** — Attributes that describe roles, states, and relationships to assistive technology. First rule of ARIA: do not use ARIA if a native HTML element already does the job. A `<button>` beats `<div role="button">` every time.

**Live region** — An area whose changes are announced without moving focus. How you tell a screen reader user that a search returned 12 results, or that a step changed.

**Target size (2.5.8)** — Minimum 24 × 24 px for anything tappable at AA level. 44 × 44 is the practical recommendation for phones.

**Screen reader** — Software that reads an interface aloud. VoiceOver on macOS and iOS, NVDA and JAWS on Windows, TalkBack on Android.

**Reduced motion** — A system-level user preference. Anything over 200ms needs an alternative that respects it. Vestibular disorders make large motion genuinely unpleasant, not merely disliked.

---

## Research

**Heuristic evaluation** — Reviewing an interface against a named set of principles, usually Nielsen's 10. Cheap, fast, and finds real problems. It cannot tell you what users will actually do, which is why Sprint 1 does both this and a usability test.

**Nielsen's 10 heuristics** — Visibility of system status · match between system and the real world · user control and freedom · consistency and standards · error prevention · recognition rather than recall · flexibility and efficiency · aesthetic and minimalist design · help users recognise, diagnose and recover from errors · help and documentation.

**Severity rating** — 1 cosmetic · 2 minor, users work around it · 3 major, users fail the task · 4 catastrophic, users lose data or money. Ratings exist so that fixing gets prioritised by consequence rather than by how annoying the problem felt to you.

**Moderated usability test** — You watch a person attempt a task and you mostly stay quiet. Your only reliable questions are "what are you trying to do?" and "what did you expect?".

**Think aloud** — Asking the participant to narrate their thinking. It slows them down slightly, which is a real cost, and it is still the highest-value thing you can ask for.

**Leading question** — A question that contains its own answer. "Did you see the Continue button?" is leading, and it destroys the finding you were about to get.

**Task, in a test** — A goal stated without a route. "Update your address" is a task. "Click Update Address then upload a bill" is a script, and it tests nothing.

---

## Product

**Problem statement** — `[user] cannot [job] because [obstacle], which costs [user cost] and [business cost].` No solution words allowed. If it names a screen or a feature, it is a solution.

**Primary metric** — The one number that decides whether the work succeeded.

**Input metric** — Something that moves before the primary metric does, so you learn earlier.

**Guardrail metric** — Something that must not get worse while you improve the primary metric. It exists because every metric can be gamed, and the guardrail is where the gaming shows up.

**Constraint** — Something you cannot change. Worth classifying into fixed policy, technical, and assumed. Most "constraints" in a legacy service turn out to be assumed, and those are the ones worth attacking.

**Decision record** — A one-page written record: context, options, decision, reason with evidence, consequences, and what would change your mind. It is what lets someone six months later understand why, instead of assuming you were careless.

---

## Systems and process

**Design system** — Tokens, components, patterns, and documentation, used together across products. Not a Figma file full of components. The documentation and the governance are what make it a system.

**Design token** — A named value. Three layers in mature systems: primitive (raw), semantic (role), component (specific). Layering is what allows theming without redesigning.

**Component API** — The properties a component exposes: variants, sizes, states, slots. Designing the API is deciding what other people are allowed to change.

**Governance** — Who decides what goes into the system, and how something gets rejected. A system with no governance becomes a folder.

**Handoff spec** — Everything an engineer needs, written down: layout, components, interactions, states, validation, error messages, accessibility, and the open questions. The test is whether they can build it without asking you anything.

**Critique** — Structured review against a rubric. Every comment names a principle and a user cost. "I don't like it" is not a critique comment.

**Failure injection** — A constraint deliberately changed mid-sprint by the admin. It exists because real projects change, and because knowing which of your earlier decisions made you fragile is a skill you can only learn by being broken once.

**Post mortem** — A written analysis after something went wrong. The valuable part is not what happened, it is which earlier decision would have made it cheaper.

**Defense** — The oral examination at the end of each sprint. Tests whether you can explain, justify, and rethink your own work without your files in front of you.

---

## Git

**Fork** — Your own copy of a repository, on your account.

**Clone** — A local copy on your machine.

**Upstream** — The original repository your fork came from. You pull from it to stay current.

**Branch** — A parallel line of work. One per task in this program.

**Commit** — A saved change with a message. Messages start with the task ID.

**Pull request** — A request to merge your branch, and the place review happens.

**Diff** — The line-by-line difference between two versions. The reason decisions live in Markdown and not in Figma is that Markdown can be diffed and argued with.
