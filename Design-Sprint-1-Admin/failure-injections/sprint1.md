# Sprint 1 Failure Injection

**Sealed until week 3, the start of the week, 10:00. Do not preview. Do not soften. Do not delay.**

---

## The injection

Delivered by the core admin, in the cohort channel, in the department's voice. Not framed as an exercise.

> **From: State Digital Services Unit**
>
> Two changes, effective immediately.
>
> 1. Legal has reviewed the flow. The ₹50 fee is now collected **before** document upload, not after. Treasury requires payment confirmation before any document enters the system.
>
> 2. The Secretary saw a demo and wants the regional language option available on every screen, not only at entry.
>
> We present to the Secretary in ten days. Please confirm by end of day.

Then stop talking. Do not explain. Do not answer "is this real". The correct admin response to that question is "the department has asked, what is your answer".

## Why these two

Chosen because each breaks something structural, not cosmetic.

**Payment before upload** inverts the risk model every designer built their flow around. The whole document guidance argument was that the citizen must not pay before learning their document is invalid. That reasoning is now void. A designer who simply reorders two screens has not noticed. A designer who realises that document validation must now happen before payment, or that the refund question has become unavoidable, has understood.

**Language on every screen** breaks layout, not logic. It adds a persistent control to a 390px screen where there is no room, and it invalidates the header of every frame already built. It also exposes whether the type scale from week 1 actually survives Devanagari at every step, which is what C1.1 asked them to test and most will have skipped.

Together they hit the two axes: one attacks the reasoning, one attacks the craft.

## What a good response looks like

| Signal | What it shows |
|---|---|
| Asks what happens to the ₹50 on rejection before touching a screen | Understood the real consequence |
| Names which earlier decisions are now invalid, in writing, before redesigning | Traceability |
| Proposes moving validation earlier rather than just reordering payment | Structural thinking |
| Raises the language control as a system component change, not a per screen fix | System instinct |
| States what they will not finish in ten days, and why that item is the right one to drop | Scope honesty |
| Post mortem names the earlier decision that would have made this cheaper | The actual learning |

## What a weak response looks like

| Signal | What it shows |
|---|---|
| Swaps the two screens, changes nothing else | Did not read the consequence |
| Adds a language dropdown to every frame by hand | No system instinct, and 40 frames of manual work |
| Argues the change is unreasonable | True and irrelevant. Note it, do not agree. |
| Silently drops the states matrix to make time | Cut the wrong thing. This is the one to catch. |
| Post mortem says "the client changed their mind" | Blames the input rather than examining the design's fragility |

The fifth one is the most important. Under pressure, designers cut states and evidence first because craft is what gets looked at. The whole point of the injection is to see what they protect.

## Admin conduct during the injection week

1. **Do not confirm it is an exercise**, even privately, even if asked directly. It stops being one the moment you confirm.
2. **Do not extend the deadline.** The ten days is inside the sprint on purpose.
3. **Answer only what a real department would answer.** "Can we keep the fee after upload?" gets "Treasury requires payment first." Nothing more.
4. **Say nothing about the refund question.** If nobody asks, that is the finding, and it goes in the ledger.
5. **Watch what they cut.** Note it mid week. It is the single most informative observation of the sprint.
6. **Debrief on the end of the week**, after post mortems are committed. Reveal it was designed, explain why these two changes, and read out what the cohort collectively protected and what it dropped.

## The debrief script

> "Both changes were written before the sprint started. The fee change was chosen because it invalidates the reasoning behind your document guidance screen, which most of you defended in week 2 critique. The language change was chosen because it tests whether your type scale actually survives Devanagari, which C1.1 asked you to check and three of you did not.
>
> Here is what this cohort cut when time got short: [read the list]. Four of five cut the states matrix. Nobody cut a high fidelity screen. That ordering is what a real team does under deadline pressure, and it is the wrong order, because the states are where the failures live and the polish is what gets noticed.
>
> The post mortems that named an earlier decision are the ones worth re-reading. The ones that named the department are not."

## Log

| Designer | First reaction | Raised the refund question | What they cut | Post mortem quality | Time cost claimed |
|---|---|---|---|---|---|
| UX1 | | | | | |
| UX2 | | | | | |
| UX3 | | | | | |
| UX4 | | | | | |
| UX5 | | | | | |

## Injections for later sprints, sealed

| Sprint | Injection | What it attacks |
|---|---|---|
| 2 | Two of five research participants withdraw consent after the sessions. Their data must be removed from every finding. | Whether findings were traceable to participants or invented |
| 3 | The primary metric is replaced mid sprint. What was activation is now retention. | Whether the design was reasoned from the metric or decorated after it |
| 4 | Engineering rejects the token structure and requires a different naming format, two weeks in. | Whether the system was designed for one consumer or for change |
| 5 | The model latency triples and the confidence score becomes unavailable. | Whether the AI surface was designed around a capability or a promise |
| 6 | The measured result contradicts the design hypothesis. Ship it anyway or roll back, with a written recommendation. | Whether they can read a number honestly against their own work |
