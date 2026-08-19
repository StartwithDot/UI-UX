# 04 — Tools Setup

Do all of this before week 1 day 1. It takes about an hour.

**The rule:** at most two new tools per sprint. Tool count is the easiest thing to inflate and the least valuable thing to own.

---

## 1. Before day one — install and sign up

### Figma — free account
1. Sign up at figma.com with the email you gave the admin
2. Accept the cohort team invite
3. Create your practice file, named exactly: `SPRINT-1 Practice UX{n}` (use your own code)
4. Install the Figma desktop app. The browser version is slower for real work.

**Before week 1 day 1, complete these Figma Learn lessons:**
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
- **macOS:** VoiceOver. Turn on with `Cmd + F5`.
- **Windows:** NVDA, free at nvaccess.org.

**Do this before day one:** turn it on and navigate one website you know for five minutes. Then turn it off. The point is that it is not new to you the first time it is graded, in week 4.

### Git and GitHub — free
1. GitHub account, if you do not already have one
2. Install git: `git --version` in a terminal to check
3. Set your identity so commits attribute to you:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "you@example.com"
   ```
4. Fork the Sprint 1 repository, clone your fork, add the upstream remote:
   ```bash
   git clone https://github.com/{your-username}/Design-Sprint-1.git
   cd Design-Sprint-1
   git remote add upstream https://github.com/StartwithDot/Design-Sprint-1.git
   git remote -v
   ```

If git is genuinely new to you, read **Pro Git chapters 1–3** (free at git-scm.com/book) before week 1. You need four commands: `clone`, `branch`, `commit`, `push`. Nothing more, for now.

### A markdown editor
VS Code (free) or Obsidian (free). You write more markdown than you expect. Anything that previews markdown and previews Mermaid diagrams is fine.

### Free web tools — bookmark, no install
- typescale.com — build a type scale
- leonardocolor.io — perceptually even colour ramps
- contrast-ratio.com or the WebAIM contrast checker
- mermaid.live — write and preview flow diagrams

---

## 2. Tools by sprint

Two new tools maximum per sprint. Everything before it carries forward.

| Sprint | New | Carried forward |
|---|---|---|
| 1 | Figma · Stark or axe DevTools · VoiceOver/NVDA · git | — |
| 2 | Maze **or** Lyssna · Dovetail **or** Notion | Figma, git |
| 3 | FigJam · Optimal Workshop | everything above |
| 4 | Tokens Studio · Storybook | everything above |
| 5 | ProtoPie (optional) · one AI product studied as material | everything above |
| 6 | PostHog · Microsoft Clarity | everything above |

Everything on this list has a free tier that covers what the program asks for.

---

## 3. What to actually learn in each tool

Not the whole tool. These parts.

| Tool | Learn this, and stop |
|---|---|
| **Figma** | Auto layout, components, variants and properties, variables and modes, libraries, branching, dev mode |
| **FigJam** | Flow diagrams, affinity mapping, running a session |
| **Stark / axe** | Contrast checking, focus order, running an automated scan and reading the result |
| **VoiceOver / NVDA** | Navigate by heading, navigate by form control, hear what a button announces |
| **Maze / Lyssna** | Build an unmoderated test, read task success, read a misclick heatmap |
| **Optimal Workshop** | Card sort, tree test, read the result |
| **Dovetail / Notion** | Tag a transcript, produce a finding that survives the sprint |
| **Tokens Studio** | Figma variables → JSON → code |
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
| Tokens | Figma variables mirror it | **source of truth**, `system/tokens/*.json` |
| Flows and IA | optional in FigJam | **source of truth**, Mermaid in markdown |
| Decisions and rationale | never | **always**, markdown |
| Specs and annotations | dev mode | markdown spec next to the link |

Reason: Figma cannot be diffed or reviewed line by line. Anything that needs to be argued with lives in git.

---

## 7. Setup checklist

- [ ] Figma account, team invite accepted, practice file created and named
- [ ] Four Figma Learn lessons completed
- [ ] Stark or axe DevTools installed
- [ ] VoiceOver or NVDA turned on once, five minutes on a real site
- [ ] GitHub account, git installed, identity configured
- [ ] Sprint 1 repo forked, cloned, upstream remote added
- [ ] Markdown editor installed
- [ ] typescale.com, leonardocolor.io, contrast checker, mermaid.live bookmarked
- [ ] Refactoring UI purchased and downloaded

Next: `05-The-Six-Sprints.md`, then `Design-Sprint-1/00-READ-FIRST.md`.
