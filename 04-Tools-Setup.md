# 04 — Tools Setup

Do all of this before Week 1 starts. It takes about an hour.

**The rule:** after Sprint 1, at most two new working tools per sprint. Tool count is the easiest thing to inflate and the least valuable thing to own. Learn the job, not the logo; the current stack and why is in `09-Modern-Practice-Map.md`.

---

## 1. Before the start — install and sign up

### Figma — free account
1. Sign up at figma.com with the email you gave the admin
2. Accept the cohort team invite
3. Create your practice file, named exactly: `SPRINT-1 Practice UX{n}` (use your own code)
4. Install the Figma desktop app. The browser version is slower for real work.

**Before Week 1, complete these Figma Learn lessons:**
- Auto layout (about 20 min)
- Components and instances (about 15 min)
- Variants (about 10 min)
- Styles and variables (about 15 min)

If auto layout is new to you, that hour is the highest-value hour of your week.

### Accessibility checker — pick one, free
- **Stark** — Figma plugin. Easier to start with.
- **axe DevTools** — browser extension. Better for auditing live sites, which week 1 needs.

Install both if you can. You use axe on the live service in week 1 and Stark inside Figma from week 2.

### Screen reader — already on your machine
- **macOS and iPhone:** VoiceOver. Turn on with `Cmd + F5` on a Mac.
- **Windows:** NVDA, free at nvaccess.org.
- **Android:** TalkBack, built in. Most of your users are on Android, so test there too.

**Do this before the start:** turn it on and navigate one website you know for five minutes. Then turn it off. The point is that it is not new to you the first time it is graded, in week 4.

### Git and GitHub — free
1. GitHub account, if you do not already have one
2. Install git: `git --version` in a terminal to check
3. Set your identity so commits attribute to you:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "you@example.com"
   ```
4. Fork the program repository **once**, clone your fork, add the upstream remote. You work inside the folder for the current sprint:
   ```bash
   git clone https://github.com/{your-username}/UI-UX.git
   cd UI-UX
   git remote add upstream https://github.com/StartwithDot/UI-UX.git
   git remote -v
   ```

If git is genuinely new to you, read **Pro Git chapters 1–3** (free at git-scm.com/book) before week 1. You need four commands: `clone`, `branch`, `commit`, `push`. Nothing more, for now.

### An AI assistant — pick one, free tier is enough
Claude, ChatGPT or Gemini. You will use one in the AI labs (`07-AI-In-Design.md`) and keep a log of every use. Create the account now and read the provider's data policy: you must not paste participant data into a tool whose policy you have not read.

### Browser developer tools
Chrome or Firefox DevTools. In week 1 you need the **Accessibility** pane (the accessibility tree), **device mode** and the **Lighthouse** panel. From week 3 you use "emulate prefers-reduced-motion". Open DevTools once on a site you know and find each.

### A markdown editor
VS Code (free) or Obsidian (free). You write more markdown than you expect. Anything that previews markdown and previews Mermaid diagrams is fine.

### Free web tools — bookmark, no install
- typescale.com — build a type scale
- leonardocolor.io — perceptually even colour ramps
- contrast-ratio.com or the WebAIM contrast checker
- mermaid.live — write and preview flow diagrams
- Loom or your operating system's screen recorder — for prototype clips and mock interviews (from week 10)

---

## 2. Tools by sprint

After Sprint 1, two new working tools maximum per sprint. Everything before it carries forward.

| Sprint | New | Carried forward |
|---|---|---|
| 1 | Figma · Stark or axe DevTools · VoiceOver/NVDA/TalkBack · git · browser DevTools · one AI assistant | — |
| 2 | Maze **or** Lyssna · Dovetail **or** Notion (and a transcription tool, with consent) | Figma, git, AI assistant |
| 3 | FigJam · Figma prototyping with variables · an AI prototyping tool (Figma Make or v0) for L-AI3 only | everything above |
| 4 | Tokens Studio · Style Dictionary · Storybook · Figma Dev Mode | everything above |
| 5 | Rive or ProtoPie (optional) · your project's own tools | everything above |
| 6 | PostHog · Microsoft Clarity · a portfolio platform (Framer, Webflow, GitHub Pages or hand-coded) | everything above |

Everything on this list has a free tier that covers what the program asks for.

---

## 3. What to actually learn in each tool

Not the whole tool. These parts.

| Tool | Learn this, and stop |
|---|---|
| **Figma** | Auto layout, components, variants and properties, **variables and modes**, libraries, branching, **Dev Mode**, prototyping with variables and conditionals |
| **Figma Make / v0** | Prompt a throwaway prototype and compare it with your spec. Never ship the output. |
| **FigJam** | Flow diagrams, affinity mapping, running a session |
| **Stark / axe** | Contrast checking, focus order, running an automated scan and reading the result |
| **VoiceOver / NVDA / TalkBack** | Navigate by heading, navigate by form control, hear what a button announces |
| **AI assistant** | Draft options to react against, read unfamiliar code, summarise what you already read. Verify everything; keep the log. |
| **Maze / Lyssna** | Build an unmoderated test, read task success, read a misclick heatmap |
| **Optimal Workshop** | Card sort, tree test, read the result |
| **Dovetail / Notion** | Tag a transcript, produce a finding that survives the sprint. AI summaries are a first pass for you to check, never the finding. |
| **Tokens Studio** | Figma variables → token JSON |
| **Style Dictionary** | Token JSON (Design Tokens format 2025.10) → CSS custom properties |
| **Figma Dev Mode** | Inspect a spec, see which tokens a component uses. The Dev Mode MCP server connects design context to AI coding tools; know it exists. |
| **Browser DevTools** | Accessibility tree, device mode, Lighthouse, reduced-motion emulation, inspecting computed values |
| **Storybook** | Read a story, document a component |
| **git** | branch, commit, push, open a pull request, read a diff |
| **PostHog** | Define an event, build a funnel, read a session replay, run a feature flag |
| **Clarity** | Heatmap and replay, nothing else |

---

## 4. Tools you do not need. Asked often, answered honestly.

None of these are required. Each has one narrow case where it is right.

| Tool | Genuinely needed when | Not needed for |
|---|---|---|
| **Adobe Photoshop** | Real photo retouching, complex masking, print prep | Any UI work. Figma covers interface design entirely. |
| **Adobe Illustrator** | Custom icon sets, logo work, complex vector illustration | Product icons, if an icon library covers them |
| **After Effects** | Marketing video, brand animation | In-product motion. Figma smart animate plus Rive covers shipped UI motion. |
| **Blender** | 3D renders, spatial and AR concepts | Standard product design |
| **Spline** | Interactive 3D on a marketing page | Product interfaces |
| **Rive** | Shipped interactive animation with state machines | Static prototypes |
| **Framer** | Shipping a portfolio or marketing site fast | Product design files |
| **Webflow** | Marketing site with a CMS | Product design |
| **Sketch** | Joining a Mac-only team that never migrated | New work |
| **Adobe XD** | Nothing. It is discontinued. | Everything |
| **Canva** | An internal deck in ten minutes | Any product work |
| **Miro** | Workshops with a client who already uses it | Anything, if you have FigJam |
| **Excalidraw** | A throwaway diagram during a call | Deliverables |
| **Penpot** | A team that cannot use Figma for licensing reasons | Nothing else. Just know it exists. |

**For this cohort:** Photoshop and Illustrator are optional and only assigned if a task genuinely needs retouching or custom vector icons. Rive appears once in Sprint 5 for a motion handoff task. After Effects, Blender, and Spline stay optional throughout.

---

## 5. Figma file naming

One team. Three files per sprint. Same names every sprint.

| File | Who edits | What is in it |
|---|---|---|
| `SPRINT-N Practice UX{n}` | you only | your own work |
| `SPRINT-N System` | system owner merges | the shared design system |
| `SPRINT-N Delivery` | whoever is assigned | shared client-facing output |

Use Figma branching for system contributions so the system owner reviews a branch instead of live edits.

---

## 6. What lives where

| Thing | Figma | Git |
|---|---|---|
| Screens and components | source of truth | link + exported PNG of the final state |
| Tokens | Figma variables mirror it | **source of truth**, `system/tokens/*.tokens.json` |
| Flows and IA | optional in FigJam | **source of truth**, Mermaid in markdown |
| Decisions and rationale | never | **always**, markdown |
| Specs and annotations | dev mode | markdown spec next to the link |

Reason: Figma cannot be diffed or reviewed line by line. Anything that needs to be argued with lives in git.

---

## 7. Setup checklist

- [ ] Figma account, team invite accepted, practice file created and named
- [ ] Four Figma Learn lessons completed
- [ ] Stark or axe DevTools installed, and the DevTools accessibility pane found
- [ ] VoiceOver, NVDA or TalkBack turned on once, five minutes on a real site
- [ ] GitHub account, git installed, identity configured
- [ ] Program repo forked, cloned, upstream remote added
- [ ] An AI assistant account, and its data policy read
- [ ] Markdown editor installed
- [ ] typescale.com, leonardocolor.io, contrast checker, mermaid.live bookmarked
- [ ] Refactoring UI purchased and downloaded
- [ ] `09-Modern-Practice-Map.md` skimmed, so you know what is current

Next: `05-The-Six-Sprints.md`, then `Design-Sprint-1/00-READ-FIRST.md`.
