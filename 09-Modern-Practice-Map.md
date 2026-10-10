# 09 — Modern Practice Map

**Last reviewed: 10 October 2026. Next review: before each cohort starts.**

This file answers one question: *is what we teach what working product designers actually use now?* It lists the current standards, theory and tools, says where each is practised in the program, and flags the parts that move fast.

Items marked **⚠ moves fast** change within months. Check the source before you rely on them, and tell the admin when something here is out of date. Claims in this file were checked against primary or well-regarded sources when written; where only vendor blogs said something, it is marked unverified.

---

## 1. Standards and regulation

| Topic | State of play | Where it appears |
|---|---|---|
| **WCAG 2.2, Level AA** | The current W3C Recommendation (October 2023) and the working reference for most national guidance. It added target size (2.5.8), focus not obscured (2.4.11), redundant entry (3.3.7), accessible authentication (3.3.8) and consistent help (3.2.6). | Sprint 1 gate and every gate after |
| **WCAG 3** | Still a W3C Working Draft (latest I found is March 2026). It will not replace WCAG 2 for years. **Do not design to it. Do read about it**, especially the shift from pass/fail to scored outcomes. ⚠ | Week 4 reading, week 20 |
| **APCA contrast** | A candidate model for WCAG 3 contrast, discussed widely. **Not a conformance method today**: 4.5:1 and 3:1 ratios are still what you are tested on. Use it as a second opinion, not a replacement. ⚠ | Week 1 colour work |
| **European Accessibility Act** | Enforceable across the EU since 28 June 2025 for covered consumer products and services, through national law and authorities. Early enforcement is mostly corrective-first; claims about fines come largely from vendors, so check national authorities. ⚠ | Week 4 and the portfolio: employers selling into the EU care |
| **India: dark patterns** | The Central Consumer Protection Authority issued guidelines in 2023 naming a list of dark patterns, including subscription traps, false urgency and confirm shaming. | Sprint 3 |
| **India: personal data** | The Digital Personal Data Protection Act, 2023. Check the current status of its rules and consent requirements before citing specifics. ⚠ | Sprints 2, 3, 5 |
| **India: payments** | RBI rules on recurring payments (pre-debit notification before each charge) and on digital lending (transparency, grievance handling). | Sprints 3 and 5 |
| **Design Tokens format** | The Design Tokens Community Group released the first stable version, **2025.10**, in October 2025: structured colour values, modern colour spaces, aliases, theming. Not on the W3C Standards Track; the group says it is still evolving. | Sprint 4, `Design-Sprint-4/06-token-architecture.md` |
| **Platform design languages** | Apple (iOS 26 "Liquid Glass") and Google (Material 3 Expressive) both changed their visual language in 2025. Compare current HIG and Material docs, not screenshots from old tutorials. ⚠ | L-PR1, platform conventions |

---

## 2. Theory, by area

The sources named in `02-Learning-Path.md` are the assigned core. This table says which *current ideas* sit on top of them.

| Area | Current thinking | Practised in |
|---|---|---|
| **Interaction and states** | Model UI as state machines and statecharts (the same model engineers use). Design every transition and guard. Treat latency as a design material: perceived speed, optimistic UI with safe rollback, and Interaction to Next Paint (INP, a Core Web Vital since 2024) as the field measure of responsiveness. | Week 3, week 9 |
| **Motion** | Purpose first; durations by distance and importance; reduced motion as a real alternative, not "instant". The View Transitions API is making page-level transitions possible in the browser (check support). ⚠ | Week 10 |
| **Colour** | Build ramps in perceptual spaces (OKLCH, with Leonardo or similar), test contrast in both themes, design for forced-colours/high-contrast modes, never rely on colour alone. | Week 1, week 13 |
| **Type** | Variable fonts, fluid type with `clamp()`, real Indic-script support, line height by script. | Week 1, L-PR3 |
| **Layout and responsiveness** | Components respond to their container (container queries, now widely supported), not only the viewport. Logical properties for writing direction. Dynamic viewport units. Name breakpoints by content. | L-PR1, L-PR3 |
| **Research** | Continuous discovery (weekly touchpoints, opportunity trees), jobs-to-be-done, mixed methods, unmoderated testing with a stated limit. AI can transcribe; synthesis stays human. AI-moderated interviews are not validated for research: use them, if at all, only for screening, and say so. | Sprint 2, L-AI2 |
| **Consent in research** | Recording, transcription services and AI tools are all *processing*. Participants consent to each, and you can name where their data went. | Week 5, L-AI2 |
| **Product and metrics** | Outcomes over outputs. A north-star with input metrics and a guardrail. Experiments with a stated minimum detectable effect. Feature flags. Privacy-respecting analytics. | P9.2, week 12, Sprint 5 |
| **Pricing and subscriptions** | The honest-cancellation argument is a commercial argument: fewer chargebacks, fewer support contacts, higher reactivation. Regulators now write the patterns down. | Sprint 3 |
| **Design systems** | Tokens in an interchange format, modes for brands, themes and density, documentation treated as a product, adoption measured, governance explicit. Design systems are now also *context for AI coding assistants*: a well-named token set and well-documented components produce better generated code. | Sprint 4 |
| **Accessibility depth** | Semantics before ARIA. Cognitive accessibility as a first-class criterion (3.3.7, 3.3.8, 3.2.6). Test with real assistive technology: VoiceOver, NVDA, TalkBack. Automated scans find roughly a third of issues at best. | Week 4, week 20 |
| **AI interfaces** | Trust calibration, not trust maximisation. Show provenance and uncertainty. Design failure, refusal, slow and wrong as first-class states. Human-in-the-loop with an audit trail. For features that *act*, define the autonomy level, the scope limit, the approval step and the undo. | Sprint 5, L-AI5 |
| **Design with AI** | AI as a source of options and a speed-up on checkable work. Prompting as a design skill. Keep a log. Disclose. Never let it invent evidence. | `07-AI-In-Design.md` |
| **Design engineering** | The boundary between design and front-end code is thinner. Designers who can read HTML/CSS, prototype with real code, and read a component's source move faster and are hired more readily. | Week 16, L-AI4 |
| **Hiring** | Portfolios are skimmed by people, filtered by systems, and checked for AI-generated sameness. Evidence of real process, honest failures and live craft beats polish. AI use is asked about directly. | `06-Job-Readiness-Track.md` |

---

## 3. The working tool stack

Teach the *job*, not the logo. Where two tools do the same job, learn one and know the other exists.

| Job | Primary | Also worth knowing | Notes |
|---|---|---|---|
| Interface design | **Figma** (Auto Layout, components, variables and modes, Dev Mode) | Penpot (open source) | ⚠ Figma adds features constantly; read release notes monthly |
| AI-assisted prototyping | **Figma Make**, v0 | Lovable, Bolt, Claude artifacts | Throwaway scaffolds to react against, never deliverables |
| Prototyping with logic | Figma prototyping with variables and conditionals | ProtoPie, Rive (motion with state machines), code | L-PR2 |
| Diagrams | Mermaid in Markdown, FigJam | Excalidraw | Mermaid lives in git |
| Colour and type | Leonardo, typescale.com | Realtime Colors, Fontsource | OKLCH |
| Tokens | Figma variables, **Tokens Studio**, **Style Dictionary** | Figma's native variable import and export, where available ⚠ | Source of truth in git, format per the DTCG spec |
| Components in code | **Storybook** | Chromatic for visual regression | Sprint 4 |
| Accessible primitives (reading, not building) | Radix, React Aria, GOV.UK Frontend | Headless UI | Read how they handle focus and keyboard |
| Design to code | Figma Dev Mode, and the Dev Mode **MCP server** for connecting design context to AI coding tools ⚠ | Cursor, GitHub Copilot, Claude Code | L-AI4, week 16 |
| Browser tooling | DevTools: accessibility tree, device mode, Lighthouse, prefers-reduced-motion emulation | Playwright for scripted checks | Week 4 and Sprint 4 |
| Accessibility testing | axe DevTools, Stark, WebAIM checker, **VoiceOver, NVDA, TalkBack** | Accessibility Insights | Real assistive tech is not optional |
| Research | Maze or Lyssna (unmoderated), FigJam or Dovetail (synthesis), Whisper-class transcription | Optimal Workshop (card sort, tree test) | Synthesis is yours |
| Product analytics | **PostHog**, Microsoft Clarity | GA4, Mixpanel | Sprint 6 and P9.2 |
| AI assistants | Claude, ChatGPT, Gemini | Perplexity for sourced lookups | Disclosure footer on everything they touch |
| Portfolio | Hand-coded or Framer/Webflow/GitHub Pages | Notion for drafts | Must pass its own accessibility check |
| Recording and sharing | Loom or the OS screen recorder | | For mock interviews and prototype clips |

Cost: everything above has a free tier that covers what the program asks for. The exceptions are Refactoring UI and, optionally, ProtoPie.

---

## 4. What we deliberately do not teach

| Not taught | Why |
|---|---|
| Any single AI tool's prompt tricks | They expire in months. We teach verification, which does not. |
| Photoshop/Illustrator/After Effects workflows | Not needed for product work. Covered in `04-Tools-Setup.md` section 4. |
| WCAG 3 conformance | It is a draft |
| Personas as a deliverable | Rarely used in practice. Evidence and jobs-to-be-done carry the weight. |
| "Design thinking" workshops | The program practises the underlying methods without the ritual |

---

## 5. Review log

| Date | Reviewer | What changed |
|---|---|---|
| 2026-10-10 | Initial map | Created. Checked against the DTCG 2025.10 announcement and format pages, the W3C WCAG 3 status, and EAA enforcement reporting. |

At every review: re-check each ⚠ item against its primary source; add what practitioners now expect; delete what has died.
