# UI UX Program Skeleton

**Version:** 1.0 | **Compiled:** 19 August 2026 | **Audience:** program designers, mentors, and any person entering product design from zero.

This is one document, not a curriculum yet. It answers four questions: what the job actually is in 2026, what a person must master and in what order, what tools and theory sit behind each stage, and how six months of sprint based project work delivers it. The curriculum map, sprint repos, and task lists come later and will be built on this skeleton.

Written after reading current product design job postings at Google, Apple, Meta, Microsoft, Stripe, Figma, Airbnb, Shopify, Atlassian, Uber, Swiggy, Zomato, CRED, Razorpay, Zerodha, PhonePe, Flipkart, and Postman, plus the published design system documentation of the same companies. What those postings ask for and what design courses teach are two different lists. This document follows the postings.

---

## 1. The honest picture of the job in 2026

### 1.1 The title is not "UI UX designer" at product companies

Search any top product company careers page and the roles are named: **Product Designer**, **Senior Product Designer**, **Interaction Designer**, **Design Technologist**, **UX Researcher**, **Content Designer**, **Design Systems Designer**. "UI UX designer" as a single title is common in agencies, service companies, and India's smaller startups, and it usually means one person doing research, flows, visuals, prototypes, and handoff.

This matters for curriculum design. A program that trains only screen decoration produces a candidate the product companies cannot place. A program that trains the product designer scope produces someone who can work anywhere, including agencies.

### 1.2 What actually gets evaluated in a product design interview loop

The loop at large product companies is consistently four to five parts:

| Round | What it tests | What a self taught candidate usually fails |
|---|---|---|
| Portfolio presentation (45 to 60 min) | Can you narrate a decision trail: problem, constraints, options rejected, evidence, outcome | Shows pretty screens, cannot explain why anything is the way it is |
| App critique (30 to 45 min) | Can you look at an existing product and reason about its choices out loud | Says "the spacing is off" instead of naming the user cost of a choice |
| Product or whiteboard exercise (45 to 60 min) | Can you go from a vague prompt to a defensible flow under time pressure | Jumps to UI, never states the user, the job, or the success metric |
| Craft or visual round | Typography, layout, hierarchy, states, motion, systems thinking | Only knows one aesthetic, cannot do density, cannot do accessibility |
| Behavioural and collaboration | Do you work with engineers, PMs, data, support, legal | Has never shipped with an engineer and cannot read a spec |

Every single item above is trainable through project work. None of it is trainable through tutorials alone. This is the argument for a sprint based program.

### 1.3 The skills product companies list that most UI UX courses skip

Taken directly from posting language, grouped:

1. **Metrics and measurement.** "Define success metrics", "partner with data science", "run and read experiments". Designers at product companies are expected to name the metric their design moves and to read an A/B test result without being lied to by it.
2. **Systems thinking.** "Contribute to and extend our design system", "design for scale across surfaces". Not screens, components with rules.
3. **Accessibility as a requirement, not a nicety.** WCAG 2.2 AA is contractual in enterprise and public sector work, and the European Accessibility Act obligations from June 2025 pushed it into every company selling into the EU. India's RPwD Act and GIGW guidelines cover government facing products.
4. **Writing.** "Strong written communication", "content design partnership". Interface text is design. Many loops include a writing sample.
5. **Working with engineering constraints.** Reading a component API, understanding what a rebuild costs, knowing why the platform pattern exists. Postings say "partner closely with engineering" in almost every case.
6. **Research literacy without being a researcher.** Running usability tests, writing a non leading question, knowing what sample size buys you, knowing when analytics answers the question faster than an interview.
7. **AI fluency in the craft.** 2026 postings increasingly ask for experience designing AI features (not just using AI tools): prompt surfaces, streaming and latency states, confidence and uncertainty display, correction and undo paths, model failure states. This is a genuine new design domain and it is where the least competition exists.
8. **Business framing.** "Understand the commercial impact of design decisions". Pricing pages, onboarding funnels, churn surfaces, trust and compliance flows.

### 1.4 The three specialisations and when to choose

Do not choose at the start. Build the generalist base first, then choose in month five based on which sprint felt like play.

| Track | Core strength | Where demand sits in 2026 |
|---|---|---|
| Product design generalist | Flow, judgement, systems, shipping | Broadest market, safest first job |
| Design systems and design engineering | Tokens, components, code, documentation, contribution governance | Highest scarcity, strong salaries, needs code comfort |
| UX research | Study design, synthesis, evidence, stakeholder influence | Fewer junior seats, usually needs a generalist year first |

Adjacent roles worth knowing exist: content design, service design, design ops, growth design, accessibility specialist.

---

## 2. The foundations that are not software

Tools change. These do not. A designer who skips this layer plateaus in about eighteen months and cannot explain their own work.

### 2.1 Visual and perceptual foundations

**What to learn**
- Gestalt principles: proximity, similarity, closure, continuity, common region, figure and ground. These are the mechanics behind every grouping decision.
- Visual hierarchy: size, weight, colour, contrast, position, whitespace, and the order the eye actually takes.
- Typography: type anatomy, x height, measure and line length, leading, tracking, optical alignment, type scale construction, pairing, variable fonts, rendering differences across platforms.
- Colour: hue, saturation, lightness, perceptual colour spaces (OKLCH and why it beats HSL for palette generation), contrast ratios, colour blindness, semantic colour roles, dark mode as a separate design problem, not an inversion.
- Layout: grids, columns and gutters, baseline rhythm, spacing scales, optical balance, density modes, responsive breakpoints, fluid type.
- Iconography: metaphor, consistency, stroke weight, optical sizing, when a label beats an icon.

**Resources**
- Refactoring UI, Adam Wathan and Steve Schoger. The fastest path from "looks amateur" to "looks intentional".
- Practical Typography, Matthew Butterick. Free online at practicaltypography.com.
- Thinking with Type, Ellen Lupton.
- Grid Systems in Graphic Design, Josef Müller-Brockmann. Old, still the reference.
- The Elements of Typographic Style, Robert Bringhurst. Reference, not a read-through.
- Better Web Type (free course) and Type Scale for scale building.
- Interaction Design Foundation article sets on Gestalt and visual hierarchy.

### 2.2 Psychology and human behaviour

This is the section most courses reduce to a Hick's Law poster. It deserves real time because it is what interviewers probe when they ask "why".

**Cognition and perception**
- Working memory limits and chunking. The real finding is roughly four items, not seven.
- Attention, change blindness, inattentional blindness, banner blindness.
- Recognition over recall. Why menus beat commands for novices and the reverse for experts.
- Cognitive load: intrinsic, extraneous, germane. Reducing extraneous load is most of interface design.
- Mental models and the gulf of execution and evaluation. Norman's framing.
- Affordances and signifiers. The distinction matters and is regularly asked.
- Fitts's Law, Hick's Law, the Doherty Threshold, and the honest limits of each.
- Progressive disclosure and staged information.

**Decision making and behavioural economics**
- Anchoring, framing, loss aversion, endowment effect, decoy effect. Where they appear in pricing and plan pages.
- Choice overload and its real conditions (it is not universal).
- Defaults as the most powerful design lever that exists.
- Present bias, friction, and the goal gradient effect. Why progress bars work.
- Peak end rule and the psychology of waiting. Why perceived speed differs from measured speed.
- Zeigarnik effect, endowed progress, and completion pressure.
- Social proof, scarcity, reciprocity, commitment. Cialdini's set, used honestly.

**Motivation and habit**
- Fogg Behaviour Model: motivation, ability, prompt.
- Hook model (trigger, action, variable reward, investment) and the ethical objections to it.
- Self Determination Theory: autonomy, competence, relatedness. The better frame for long term product engagement.
- Jobs to be Done and the progress making forces diagram.

**Ethics and dark patterns**
- The named pattern catalogue: confirmshaming, roach motel, forced continuity, privacy zuckering, sneak into basket, nagging, obstruction, hidden costs.
- Regulation is now real: EU Digital Services Act deceptive design provisions, the EU Data Act and consent requirements, FTC enforcement on negative option and click to cancel rules in the US, India's DPDP Act consent standards. A designer in 2026 who cannot recognise a dark pattern is a legal liability.
- Deceptive design taxonomy at deceptive.design (Harry Brignull).

**Trust, privacy, and safety**
- Consent surfaces that are honest and still convert.
- Designing for edge cases: harassment, coercion, shared devices, low trust contexts.
- Data minimisation shown in the interface.

**Resources**
- The Design of Everyday Things, Don Norman. Non negotiable.
- Thinking, Fast and Slow, Daniel Kahneman. Read chapters, not cover to cover.
- Hooked, Nir Eyal, paired with Indistractable by the same author for the counterweight.
- Laws of UX, Jon Yablonski (lawsofux.com, free) and the accompanying book.
- 100 Things Every Designer Needs to Know About People, Susan Weinschenk.
- Nielsen Norman Group articles, specifically the 10 usability heuristics and the mental models set. nngroup.com.
- Deceptive Design pattern library, deceptive.design.
- Behavioural Economics guide, behavioraleconomics.com (free annual guides).

### 2.3 Interaction and information architecture

- State design: empty, loading, partial, error, success, offline, permission denied, rate limited, zero results, first run. Most junior portfolios show only the happy path. This single habit separates hireable from not.
- Feedback and system status. Optimistic UI and when it lies to the user.
- Navigation models: hierarchy, hub and spoke, tabs, drill down, modal stacks, deep linking, back behaviour on each platform.
- Information architecture: taxonomy, labelling, faceted navigation, search versus browse, card sorting and tree testing as the two IA validation methods.
- Forms: single column defaults, input types, inline validation timing, error message writing, autofill, keyboard types on mobile, multi step versus single page, save and resume.
- Tables and data density: sorting, filtering, pagination versus infinite scroll, bulk actions, column management, responsive strategies for tables. Enterprise work lives here.
- Search: query input, suggestions, zero results recovery, filters, ranking transparency.
- Motion: duration and easing conventions, choreography, shared element transitions, motion as spatial explanation, reduced motion preferences.
- Microinteractions: trigger, rules, feedback, loops and modes (Dan Saffer's model).

**Resources**
- About Face, Alan Cooper. The interaction design reference.
- Designing Interfaces, Jenifer Tidwell. Pattern encyclopedia.
- Information Architecture (the polar bear book), Rosenfeld, Morville, Arango.
- Form Design Patterns, Adam Silver. Accessible forms, done properly.
- Microinteractions, Dan Saffer.
- Material Design 3 motion guidelines and Apple HIG motion section, read as reference, not gospel.

### 2.4 Accessibility and inclusive design

Treated as its own foundation because in 2026 it is a legal requirement in most markets a product company sells into.

- WCAG 2.2 AA in practice: contrast minimums, target size, focus appearance, focus not obscured, dragging alternatives, consistent help, redundant entry, accessible authentication.
- POUR principles: perceivable, operable, understandable, robust.
- Keyboard operability: tab order, focus management in modals and drawers, skip links, focus visible.
- Screen reader mental model: headings structure, landmarks, names roles and values, live regions, accessible names for icon buttons.
- ARIA basics and the first rule of ARIA (do not use ARIA if native HTML does the job).
- Motor, cognitive, low vision, colour vision, hearing, temporary and situational impairments.
- Testing: keyboard only pass, VoiceOver and NVDA basics, axe DevTools, contrast checkers, and why automated tools catch only around a third of issues.

**Resources**
- WCAG 2.2 quick reference, w3.org/WAI/WCAG22/quickref.
- Inclusive Components, Heydon Pickering (inclusive-components.design).
- Accessibility for Everyone, Laura Kalbag.
- A11y Project checklist, a11yproject.com.
- Deque University free courses and axe DevTools.
- Apple accessibility HIG and Android accessibility guidelines.

### 2.5 Research and evidence

- Research question framing. Turning a stakeholder wish into an answerable question.
- Method selection: when to interview, when to survey, when to test, when to read analytics, when to do nothing.
- Generative methods: semi structured interviews, contextual inquiry, diary studies, JTBD interviews.
- Evaluative methods: moderated usability testing, unmoderated testing, benchmark studies, heuristic evaluation, cognitive walkthrough, accessibility audit.
- Quantitative methods: SUS, UMUX Lite, SEQ, task success and time on task, funnel analysis, cohort retention, A/B and multivariate testing, statistical significance and the common ways it is misread.
- Non leading question writing. The most testable research skill.
- Sample size reality: five users find most severe usability issues in a single flow, five users tell you nothing about preference or magnitude.
- Synthesis: affinity mapping, thematic coding, journey mapping, service blueprints, opportunity solution trees, personas (and their honest limits), scenarios, jobs statements.
- Research ops: participant recruiting, screeners, incentives, consent, PII handling, a research repository so findings survive.
- Analytics literacy: event taxonomy, funnels, retention curves, session replay, heatmaps and their misuse, survivorship bias in product data.

**Resources**
- Just Enough Research, Erika Hall.
- Interviewing Users, Steve Portigal.
- Rocket Surgery Made Easy and Don't Make Me Think, Steve Krug.
- Measuring the User Experience, Tullis and Albert, for the quantitative side.
- Continuous Discovery Habits, Teresa Torres, for opportunity solution trees.
- Nielsen Norman Group research method articles and the "how many test users" set.
- Trustworthy Online Controlled Experiments, Kohavi, Tang, Xu, for experiment literacy.
- Maze, Lyssna, UserTesting free tiers, Optimal Workshop for card sorting and tree testing.

### 2.6 Product and business thinking

- Product strategy basics: positioning, target segment, value proposition, competitive alternative.
- Metrics: north star metric, input metrics, guardrail metrics, HEART framework, counter metrics. Why a designer must propose a guardrail.
- Funnels, activation, retention, monetisation, referral. Where design leverage sits in each.
- Prioritisation frameworks and their tradeoffs: RICE, impact and effort, opportunity scoring, Kano.
- Roadmaps, quarterly planning, scoping, cutting scope without lying about it.
- Writing a design brief, a one pager, a decision record.
- Working with pricing, trust, legal, and compliance surfaces.
- Unit economics vocabulary: CAC, LTV, churn, ARPU. Enough to hold a conversation.

**Resources**
- Inspired, Marty Cagan. And Empowered for the org side.
- Escaping the Build Trap, Melissa Perri.
- Lean Analytics, Croll and Yoskovitz.
- Google HEART framework paper (search "HEART framework Google research paper").
- Shape Up, Basecamp (free online) for scoping and appetite thinking.
- Reforge free articles and Lenny's Newsletter free posts for current practice.

### 2.7 Systems, tokens, and platform literacy

- Atomic design as a mental model, not a folder structure religion.
- Component anatomy: variants, states, slots, composition, boundaries, when to make a new component versus extend one.
- Design tokens: primitive, semantic, component layers. Naming conventions. Theming and multi brand. Dark mode through tokens. The W3C Design Tokens format work.
- Documentation: usage guidance, do and do not, accessibility notes, content guidance, code links, changelog.
- Governance: contribution model, review, versioning, deprecation, adoption tracking. Systems fail on governance far more than on craft.
- Platform conventions: iOS Human Interface Guidelines, Material Design 3, web platform norms, and knowing when to deviate deliberately.
- Reading a real design system: Material 3, Apple HIG, IBM Carbon, Atlassian Design System, Shopify Polaris, Adobe Spectrum, GitHub Primer, Salesforce Lightning. Carbon and Polaris are the best study material because their documentation explains reasoning.

**Resources**
- Design Systems, Alla Kholmatova.
- Design That Scales, Dan Mall.
- Expressive Design Systems, Yesenia Perez-Cruz.
- Carbon, Polaris, Primer, and Spectrum public documentation.
- Design Tokens Community Group spec, tr.designtokens.org.
- Tokens Studio documentation and Figma variables documentation.

### 2.8 Technical literacy for designers

Not "learn to code to be a designer". Learn enough that engineers stop discounting your work.

- HTML semantics and why the element choice is an accessibility decision.
- CSS layout model: box model, flexbox, grid, container queries, logical properties, cascade layers, custom properties.
- Responsive and adaptive strategy, fluid type with clamp, breakpoints as a last resort.
- Component thinking in code: props map to variants, state maps to state, composition maps to slots.
- Basic React or Vue reading ability. Ability to open a component file and see which props exist.
- Design to code pipelines: tokens as JSON, Style Dictionary, Storybook, visual regression testing.
- Version control: git basics, branches, pull requests, reviewing a diff, commenting on a PR.
- Performance as a design constraint: Core Web Vitals (LCP, INP, CLS), image formats and sizes, font loading strategy, skeleton versus spinner decisions, perceived performance.
- Platform limits: what a native transition can do that the web cannot, safe areas, notches, keyboard avoidance, offline behaviour.
- API and data shape awareness: pagination, loading in chunks, optimistic updates, error codes surfacing as user facing messages.

**Resources**
- MDN Web Docs for HTML, CSS, and accessibility.
- web.dev Learn CSS and Learn Accessibility, free courses by Google.
- Josh Comeau's CSS for JavaScript Developers (paid) or his free blog articles.
- Storybook documentation, Style Dictionary documentation.
- Every Layout, Heydon Pickering and Andy Bell, for layout reasoning.
- freeCodeCamp responsive web design certification, free, for absolute beginners.

### 2.9 Designing for AI products

This is the newest genuine skill area and the least saturated. Product companies in 2026 ship AI features constantly and most designers have never designed one properly.

- Choosing the surface: chat is usually the wrong answer. Inline suggestion, command palette, background automation, side panel, review queue.
- Setting expectations before output: what the system can and cannot do, in the interface.
- Latency design: streaming output, progressive rendering, skeleton states, cancel, background completion, why a 4 second wait needs different design from a 400 millisecond wait.
- Uncertainty and confidence: how to show that a result may be wrong without destroying usefulness.
- Citation and provenance surfaces.
- Correction paths: edit, regenerate, undo, thumbs feedback, teach the system.
- Error and refusal design: model failure, empty retrieval, safety refusal, rate limits, quota.
- Human in the loop patterns: approval queues, confidence thresholds routing to review, audit trails.
- Prompt as an interface element: templates, examples, constraints, and why a blank text box is a usability failure.
- Cost and quota as design constraints. Token cost has interface consequences.
- Evaluation literacy: how a designer contributes to eval sets and reads model quality reports.
- Agent patterns: showing plan and progress, permission gates, reversibility.

**Resources**
- Google People and AI Guidebook (PAIR), pair.withgoogle.com/guidebook.
- Microsoft HAX Toolkit and Guidelines for Human AI Interaction, aka.ms/haxtoolkit.
- IBM Design for AI, ibm.com/design/ai.
- Apple HIG Machine Learning section.
- Shape of AI pattern library, shapeof.ai.
- Anthropic and OpenAI product documentation, read as design case material for streaming, tool use, and refusal behaviour.

### 2.10 Communication and craft of persuasion

- Case study structure: context, constraint, hypothesis, exploration, decision, evidence, outcome, learning. Outcome without evidence is decoration.
- Presenting to non designers. Leading with the user problem and the metric, never with the tool.
- Critique: giving feedback on the decision, not the taste. Receiving feedback without defending.
- Written design decisions: a one page decision record beats a Slack thread and survives reorgs.
- Facilitation: workshops, design reviews, kickoff sessions, affinity mapping sessions with strong opinions in the room.
- Stakeholder management: saying no with an alternative, escalating with evidence, negotiating scope.
- Portfolio as a product: three to five deep cases, not twelve shallow ones. Password free, fast loading, readable on a phone, with a two minute version and a twenty minute version of each case.

**Resources**
- Articulating Design Decisions, Tom Greever.
- Discussing Design, Connor and Irizarry, for critique structure.
- Storytelling with Data, Cole Nussbaumer Knaflic.
- Case study examples worth studying: the public case studies on the portfolios of designers currently at Stripe, Figma, and Linear. Study structure, not visuals.

---

## 3. Tooling map for 2026

Tools are the shallowest layer. Learn the primary column deeply, know the secondary column exists.

| Job | Primary | Also know | Notes |
|---|---|---|---|
| Interface design | Figma | Penpot (open source), Sketch (legacy Mac shops) | Figma is the market default. Variables, auto layout, components, variants, modes are the parts that matter. |
| Prototyping, low fidelity | Figma | FigJam, paper | Speed over polish. |
| Prototyping, high fidelity | Figma prototyping, ProtoPie | Framer, Rive for motion | ProtoPie for sensor and logic heavy interaction. Rive for shipped animation assets. |
| Wireframing and whiteboard | FigJam | Miro, Excalidraw | Interviews use exactly this. |
| Design systems | Figma libraries and variables | Tokens Studio, Style Dictionary, Storybook | Tokens Studio is the bridge from Figma to code. |
| Handoff and documentation | Figma dev mode | Storybook, Zeroheight, Supernova | Dev mode plus a written spec beats either alone. |
| Research, unmoderated | Maze | Lyssna, UserTesting, PlaybookUX | Free tiers are enough for a program. |
| Research, IA validation | Optimal Workshop | UXtweak | Card sorting and tree testing. |
| Research repository | Dovetail | Notion, Airtable, Condens | Any structured store beats none. |
| Analytics | PostHog (open source, generous free tier) | Amplitude, Mixpanel, GA4 | PostHog gives funnels, replay, flags, and experiments in one free tool. Ideal for a program. |
| Session replay and heatmaps | PostHog, Microsoft Clarity (free) | Hotjar | Clarity is fully free with no volume cap. |
| Accessibility testing | axe DevTools, VoiceOver, NVDA | Lighthouse, Stark, Polypane | Manual keyboard pass is mandatory regardless of tool. |
| Contrast and colour | Figma plugins, Leonardo (Adobe, free) | Coolors, Realtime Colors | Leonardo for perceptually even ramps. |
| Motion | Figma smart animate, Rive | After Effects, Lottie, Framer Motion | Rive and Lottie are what ships. |
| Diagrams and flows | FigJam, Whimsical | Mermaid (text based, versionable) | Mermaid diagrams live in git and never rot. |
| Illustration and asset work | Figma, Illustrator | Blender for 3D, Spline for web 3D | Optional, only if the specialisation calls for it. |
| Code and handoff reading | VS Code, git, GitHub | Storybook, CodeSandbox, v0, Cursor | Enough to read a component and open a PR comment. |
| AI in the workflow | Figma AI features, Claude, ChatGPT, Cursor | v0, Lovable, Uizard | Use for divergence, boilerplate, copy variants, and code reading. Never for the decision. Disclose usage on artefacts. |
| Writing and specs | Notion, Markdown in git | Google Docs | Program artefacts should be Markdown so they can be reviewed as diffs. |

**On AI tools honestly.** In 2026 they compress production time and do not compress judgement. A candidate who ships fast and cannot defend a decision is filtered in round one. Program stance: AI use is allowed, must be disclosed in one line on the artefact, and the verified part is what gets graded.

---

## 4. Progression: what "good" looks like at each level

Useful because it tells a learner what they are aiming at, and tells a mentor where to set the bar.

| Level | Scope | Evidence they can show |
|---|---|---|
| Absolute beginner | One screen | Can copy a pattern and explain the grid and type scale used |
| Foundation | One flow | Ships all states, keyboard operable, contrast passing, writes their own microcopy |
| Junior product designer | One feature | Frames the problem, runs a small usability test, names a metric, hands off cleanly to engineering |
| Mid product designer | One product area | Owns discovery to ship, negotiates scope, contributes components to the system, defends decisions with evidence |
| Senior product designer | Multiple areas or a hard domain | Sets direction, mentors, influences roadmap, handles ambiguity with no brief, writes the strategy doc |
| Staff and beyond | Org level | Design systems and standards, cross team patterns, hiring bar, design ops |

Six months of serious project work targets the junior bar with parts of mid. It does not target senior. Any program claiming otherwise is selling.

---

## 5. The six month sprint based learning path

Same operating model as the data engineering program: sprints, real briefs, weekly problem statements, individual practice zone plus one shared build zone, rotating roles, committed artefacts, milestone checkpoints, an injected failure, and an oral defense per sprint.

**Shape:** six sprints of four weeks each, 24 weeks total. Roughly 12 to 15 hours per week: 8 to 10 on the sprint project, 4 to 5 on the fundamentals spine.

**Rules that hold across all sprints**
1. Real product, real users, real constraints. No dribbble redesigns of Spotify. Every sprint ships something a stranger can use.
2. Every deliverable is a committed artefact in a repo, reviewed as a pull request. Figma files are linked, decisions are written in Markdown.
3. Every screen ships all states or it is not done: empty, loading, error, success, offline, permission, zero results.
4. Every sprint has an accessibility gate: keyboard only pass, contrast pass, screen reader pass on the primary flow. Failing the gate blocks sign off.
5. Every sprint names one metric and one guardrail metric before design starts.
6. Every claim needs evidence. "Users prefer this" without a test result fails review.
7. One injected failure per sprint (a constraint change, a hostile stakeholder note, a research finding that kills the concept) and a written post mortem.
8. Oral defense at sprint end. Vocabulary, decision trail, alternative design under a changed constraint, one honest "I do not know yet, here is how I would find out".

### Sprint 1 (weeks 1 to 4): Craft foundations and the single flow

**Project:** rebuild one real, boring, high stakes flow end to end. Suggested: a government or utility service flow in the learner's own city, or an insurance claim, or a bank KYC step. Boring flows teach more than social apps because the constraints are real and the existing version is genuinely bad.

**Learn:** Figma fundamentals (auto layout, components, variants, variables, modes), type scale and spacing system construction, colour ramps and semantic roles, Gestalt and hierarchy applied, form design patterns, all interface states, WCAG 2.2 AA basics, keyboard operability, writing interface text.

**Ship:** a system starter (tokens, type scale, spacing, colour, four base components), the full flow at desktop and mobile, all states documented, an accessibility audit of the original flow and of your version, a one page decision record.

**Fundamentals spine:** Gestalt, hierarchy, typography, cognitive load, Norman's affordances and signifiers, POUR.

**Defense questions:** why this type scale, what does your spacing scale prevent, which state did you almost forget and why does it matter, what breaks for a keyboard only user in the original.

### Sprint 2 (weeks 5 to 8): Research and problem framing

**Project:** take a real small product or a real local business's digital experience, and run actual discovery. Five interviews, one survey, one usability test on the current experience, analytics if available. Produce a problem definition that contradicts at least one assumption you started with.

**Learn:** research question framing, non leading interview questions, screeners and recruiting, moderated usability testing, task success and SEQ measurement, thematic synthesis, journey mapping, service blueprint, opportunity solution tree, JTBD framing, research ethics and consent, PII handling, analytics basics (funnels, retention), heuristic evaluation.

**Ship:** research plan, discussion guide, five interview summaries, usability test report with severity ratings, synthesis map, journey map, opportunity solution tree, a problem statement with evidence, and a written "what I believed and what the evidence changed" section.

**Fundamentals spine:** sample size reality, leading question failure modes, survivorship and selection bias, qualitative versus quantitative fit, mental models.

**Defense questions:** which question in your guide was leading and how did you fix it, what would five more participants have told you and what would they not, which finding is weak evidence and how do you say so honestly.

### Sprint 3 (weeks 9 to 12): Product thinking and the end to end feature

**Project:** design a new feature for an existing real product with a stated business goal. The brief is deliberately vague, like a real one. Include a competitive teardown, three concept directions, a chosen direction with rationale, and a scoped v1 versus later.

**Learn:** product strategy basics, metrics (north star, input, guardrail, HEART), funnels and activation, prioritisation (RICE, impact and effort, Kano), scoping and appetite, information architecture, navigation models, card sorting and tree testing, high fidelity prototyping, usability testing on your own prototype, iteration logs.

**Ship:** product brief, competitive teardown, IA and flow diagrams, three concepts with a decision record, a tested high fidelity prototype, a metric definition doc with guardrails, a scope cut document explaining what is not in v1 and why.

**Fundamentals spine:** behavioural economics in product surfaces, defaults, friction, choice architecture, dark pattern boundary and where regulation sits, ethics.

**Defense questions:** what metric moves and what metric could get worse, what did you cut and what breaks because you cut it, which behavioural lever are you using and is it honest.

### Sprint 4 (weeks 13 to 16): Design systems and engineering handoff

**Project:** build a real design system for the shared cohort product, and get one component actually implemented in code with an engineer or by yourself. Multi brand or multi theme is required so tokens have to earn their existence.

**Learn:** token architecture (primitive, semantic, component), naming conventions, Figma variables and modes, Tokens Studio to code pipeline, Style Dictionary, component API design, variants and slots, documentation standards, accessibility annotations, contribution and governance model, versioning and deprecation, Storybook, git and pull request workflow, reading component code, visual regression basics.

**Ship:** token set in JSON and in Figma, ten to fifteen documented components with states and accessibility notes, a governance and contribution doc, one component implemented in code in Storybook, an adoption checklist, a changelog.

**Fundamentals spine:** systems thinking, abstraction cost, when not to abstract, HTML semantics, CSS layout model, performance basics, Core Web Vitals as design constraints.

**Defense questions:** why is this token semantic and not primitive, what happens to your system when a third brand arrives, which component should not exist, what did the engineer push back on and who was right.

### Sprint 5 (weeks 17 to 20): AI product design and complex or enterprise surfaces

**Project:** two parts. First, design an AI feature inside a real product context with genuine failure modes (not a chatbot wrapper). Second, design one dense data surface: a table heavy admin, dashboard, or workflow queue. Both are where 2026 hiring demand actually sits and where portfolios are thinnest.

**Learn:** AI surface selection, expectation setting, streaming and latency design, uncertainty and confidence display, citation and provenance, correction and regeneration paths, refusal and safety states, human in the loop and approval queues, cost and quota as constraints, eval literacy. For the dense surface: data density modes, table patterns, bulk actions, filtering and saved views, permissions and roles, audit trails, keyboard first workflows, error recovery in destructive actions.

**Ship:** an AI feature spec covering every failure state, a prototype demonstrating streaming and correction, a confidence and provenance pattern, a dense workflow surface with three density modes and full keyboard operation, a permissions matrix, and a written analysis of what happens when the model is wrong.

**Fundamentals spine:** probabilistic systems versus deterministic ones, trust calibration, automation bias, error cost asymmetry, privacy and consent for AI features (DPDP and GDPR relevant parts).

**Defense questions:** what does the user see when the model is confidently wrong, how does the user undo, why is this not a chat interface, what does one operation cost and does the interface reflect that.

### Sprint 6 (weeks 21 to 24): Ship, measure, and portfolio

**Project:** take the strongest work from sprints 1 to 5 to actual shipped state with real users, instrument it, run one experiment or one measured before and after, and build the portfolio and interview readiness on top of real outcomes.

**Learn:** analytics instrumentation and event taxonomy, funnel and retention reading, A/B testing basics and misreading traps, post launch iteration, case study structure, portfolio site build, presentation practice, app critique practice, whiteboard exercise practice, behavioural interview stories built from the injected failures, negotiation basics.

**Ship:** a live shipped surface with instrumentation, an experiment or before and after report with honest interpretation, three deep case studies, a portfolio site, a two minute and a twenty minute version of each case, five practised app critiques, three timed whiteboard exercises recorded and reviewed.

**Fundamentals spine:** experiment literacy, statistical significance and its abuse, novelty effect, Simpson's paradox in product data, communicating uncertainty.

**Defense questions:** full mock loop. Portfolio presentation, live app critique, timed product exercise, craft round, and the alternative design question under a changed constraint.

---

## 6. The fundamentals spine

Same principle as the data engineering program. Tools change every sprint, the spine does not. Roughly four to five hours a week, running under all six sprints, with its own artefacts and its own grading.

**Weekly ritual**

| Slot | Time | What happens | Output |
|---|---|---|---|
| Why session | 60 to 90 min | One concept, presented by a rotating learner, mentor only interrogates | `why-sessions/weekNN.md` |
| Teardown lab | 60 min | Critique one real product surface against named principles, with the user cost of each flaw stated | `teardowns/NN-product.md` |
| Craft drill | 20 min daily | One component, one type scale, one state set, one copy rewrite | one line per day in `drills/log.md` |
| Decision record | as needed | Any design decision worth arguing gets a one page record | `adr/ADR-NNN-title.md` |

**Artefact standards**
- **Explainer:** plain definition, the problem it solves, an example from our own project, what breaks if you get it wrong, and one thing still confusing. Honesty graded, bluffing not.
- **Teardown:** the flaw, the principle it violates, the user cost, the fix, and what the fix costs. "It looks bad" fails.
- **Decision record:** context, at least two options considered, decision, consequences including the bad ones, revisit trigger.
- **Post mortem:** what broke, how it was found, root cause, what should have caught it, prevention. One per sprint minimum.

**AI stance**
AI use is allowed and must be disclosed in a one line footer on each artefact. The verified part is graded. An explainer that says "the model claimed X, I tested with three users and found Y" scores highest. Oral defense is the equaliser because it cannot be outsourced.

---

## 7. Assessment

**Weekly:** artefact exists and is non trivial. Every case artefact needs one peer review with at least one substantive comment. Rubber stamp approvals are called out.

**Mid sprint (week 3 of 4): the whiteboard why.** Fifteen minutes, no notes. Draw the current flow from memory, answer three questions drawn at random from the question bank. Needs work is normal and schedules a re-run.

**Sprint end: the defense.** Six parts.
1. Flow walk from the learner's own diagram, 10 min
2. Terminology and tradeoff interrogation, 10 min
3. Failure story with evidence, 10 min
4. Business framing: who reads this, what decision changes, 5 min
5. Evidence defense: defend your test results, your metric, your sample, 10 min
6. Alternative design: redo it with one constraint changed (no colour, 2G network, screen reader only, half the engineering budget, ten times the data, offline first), 10 min

**Pass bar:** correct vocabulary, plus one defended piece of evidence, plus one coherent alternative design, plus one honest "I do not know yet, here is how I would find out".

**Program level:** one ledger file per learner, appended each sprint. Concepts covered, teardowns authored, tests run, components shipped, defenses passed, accessibility gates cleared. By month six the ledger is the portfolio narrative.

---

## 8. Question bank starter

Never publish answers to learners.

**Craft:** why this type scale and not a linear one · what does your spacing system prevent · why is this contrast ratio acceptable · what makes this hierarchy work without colour · which state is missing and what does the user experience when it happens.

**Interaction:** why a modal and not a page · what happens on back · where does focus go when this drawer closes · why inline validation on blur and not on keystroke · what does this optimistic update lie about.

**Research:** which of your questions was leading · what does five participants buy you and what does it not · which finding is weak and how do you say so · when would analytics have been faster than an interview.

**Product:** what metric does this move and what could get worse · what did you cut and what breaks · who disagreed and what did you do · what would you ship if you had one week.

**Systems:** why is this a variant and not a new component · what breaks when a third theme arrives · which token is misnamed and why does that matter in a year · what did the engineer push back on.

**Accessibility:** what is the keyboard path through this · what does a screen reader announce here · which WCAG 2.2 criterion does this fail · what is the situational impairment case for this screen.

**AI:** why is this not a chat interface · what does the user see when the model is confidently wrong · how does the user correct it · what does one operation cost and does the interface show it · what is the human in the loop gate.

**Ethics:** where is the dark pattern boundary in this flow · what consent are you actually getting · what happens on a shared device · which regulation applies to this surface.

---

## 9. What this program deliberately does not do

Stated openly so nobody is surprised.

- **No graphic design, branding, or illustration depth.** Adjacent field, different craft. One session on brand as constraint, nothing more.
- **No 3D, motion graphics, or game UI.** Optional self study for whoever wants it.
- **No front end engineering depth.** Enough to read, annotate, and ship one component. Not enough to build a product alone.
- **No senior level strategy or org design.** Six months does not buy that and pretending otherwise wastes the learner's time.
- **No tool certification chasing.** Figma certificates do not clear interview loops. Shipped work with defended decisions does.
- **No dribbble portfolio aesthetic.** Redesigns without users, metrics, or constraints are filtered out at product companies.

---

## 10. Reference library, consolidated

**Books, in order of usefulness for a beginner**
1. Refactoring UI, Wathan and Schoger
2. The Design of Everyday Things, Norman
3. Don't Make Me Think, Krug
4. Just Enough Research, Hall
5. About Face, Cooper
6. Form Design Patterns, Silver
7. Design Systems, Kholmatova
8. Articulating Design Decisions, Greever
9. Laws of UX, Yablonski
10. Inspired, Cagan
11. Thinking with Type, Lupton
12. Accessibility for Everyone, Kalbag
13. Measuring the User Experience, Tullis and Albert
14. Design That Scales, Mall
15. Continuous Discovery Habits, Torres

**Free web references worth reading fully**
Nielsen Norman Group (nngroup.com) · Laws of UX (lawsofux.com) · Practical Typography (practicaltypography.com) · Inclusive Components (inclusive-components.design) · WCAG 2.2 quick reference (w3.org/WAI/WCAG22/quickref) · web.dev Learn courses · MDN Web Docs · Material Design 3 (m3.material.io) · Apple HIG (developer.apple.com/design) · IBM Carbon (carbondesignsystem.com) · Shopify Polaris (polaris.shopify.com) · Atlassian Design System · GitHub Primer · Google PAIR Guidebook (pair.withgoogle.com/guidebook) · Microsoft HAX Toolkit · Shape of AI (shapeof.ai) · Deceptive Design (deceptive.design) · A11y Project (a11yproject.com) · Every Layout (every-layout.dev) · Design Tokens spec (tr.designtokens.org) · Shape Up (basecamp.com/shapeup)

**Courses and structured programs**
Google UX Design Certificate on Coursera, for structure only, weak on craft and systems · Interaction Design Foundation, cheap membership, strong on theory breadth · Refactoring UI, paid, best value for craft · Learn UI Design and Learn UX Design (Erik Kennedy), paid, strong on visual craft · Design Systems for Figma (Molly Hellmuth), paid · freeCodeCamp responsive web design, free, for the technical layer · Deque University free accessibility courses

**Communities and current practice**
Figma community files and Config talks · Design Systems Slack · Friends of Figma local chapters · Lenny's Newsletter free posts · Smashing Magazine · UX Collective on Medium · Reddit r/UXDesign for market reality checks, filtered heavily

**Practice sources for real briefs**
Government service flows in your own city · local business digital experiences · open source project interfaces that need help · nonprofit and civic tech briefs · your own daily friction, documented for a week

---

## 11. Next steps to turn this into a curriculum

1. Decide cohort size, and whether the shared build zone is one product for the whole cohort or one per small team.
2. Pick the six sprint projects concretely, with real briefs and named users, following the data engineering three document pattern per sprint: project brief, task list without answers, admin task list with answers.
3. Build the repo skeleton: `students/UX{n}/week{n}/`, `system/` for the shared design system, `delivery/` for research, design, prototype, and presentation artefacts, `fundamentals/` for the spine.
4. Write the station map. Four tracks in parallel, same as the metro map model: **Craft and Interface**, **Research and Evidence**, **Product and Business**, **Systems and Technical**. AI product design runs as the fifth track from sprint 5, and accessibility runs as a gate on every station rather than a track of its own.
5. Write the question bank and the failure injection list for the admin repo. Never publish either.
6. Define the accessibility gate as a CI style checklist so sign off is objective, not a matter of taste.
7. Set the tool budget: two new tools per sprint maximum, everything else reuse or a one session comparison with a written verdict.
