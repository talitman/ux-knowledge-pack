# UX · Motion · Web — agent-readable knowledge pack

**Purpose.** One file coding agents (Cursor, Claude Code, Codex) can load before designing or animating UI, marketing sites, or in-app polish for Dotan Talitman’s products. Durable knowledge only — not project status.

**Compiled.** 2026-11-06 (Asia/Jerusalem) by Saylo UX/UI Manager. English; Hebrew quotes kept where Dotan said them.

**Scope.** Web animations & effects, motion craft, UI/UX design craft, website/landing building, RTL/Hebrew. Saylo palettes and mockups are Saylo-only; reuse METHOD and motion rules elsewhere, not the lavender identity unless the brief is Saylo.

---

## TL;DR — non-negotiable rules for agents

1. **Live session decides.** Dotan steers the real UI (hot reload, tweak panel, variations gallery, checkpoints with rollback). Variant rounds and critic scores are prep only — never the decision. When he is at his Mac: open **localhost** (bring window front), not a tunnel. Tunnel = remote only; link previews consume single-use links.
2. **No A/B “pick one”.** Show directions **side by side on the same page**. He chooses. Do not pick for him.
3. **Fidelity.** Built screens must match selected mockups almost exactly (fonts, colors, spacing, buttons, copy) — not loosely.
4. **Bilingual.** Every surface: English + Hebrew RTL with a visible **EN | עב** switch. Mirror layout; directional icons; `bdi` for times/numbers.
5. **Quality bar.** Critic pass = **≥ 9.0** with **zero must-fix**. Consensus: 2 independent critic runs on pinned shots (mean if spread ≤ 0.3; else 3rd run → median). Implementers never self-score. Plateau rule: gain < 0.2 over two rounds after diagnosis → freeze with blockers and move on.
6. **Anti–AI-slop.** Ship with DESIGN.md / brand tokens. Run Impeccable detector (or equivalent) before claiming polish. Prefer real references over “make it clean/modern”.
7. **Motion discipline.** Prefer `transform` + `opacity`. Always honor `prefers-reduced-motion` (and `?motion=reduce` in previews). Do not hurt LCP/CLS. Things opened >100×/day usually get **no** enter animation. Continuity motion ≈ **180–300 ms**.
8. **Wow = content becoming good output**, not flashy transitions between settings screens. Animation explains state; it does not decorate.
9. **Web toolkit default (marketing/landing).** Install **GSAP Skills first** (~80% of site needs: scroll, fade-ins, stagger, page transitions), then Emil `animate` for easing/timing. Remotion / Rive / Lottie / Three.js when the brief needs them (see §3). Always reduced-motion + perf.
10. **Code-first motion graphics** for B-roll/explainers when possible (HyperFrames / Remotion / canvas `f(t)`), cheaper than paid video models. Video models for realism only. **Never** pad timing with freeze frames (`ffmpeg tpad`/clone) — he rejected that; dwell must be real timeline time with ambient motion still running.
11. **Nothing to Dotan before UX review.** EM/implementers send screenshots + branch head to UX first.
12. **Off-theme refs.** If a mock is flagged off-theme: **take the idea, not the look.**

---

## 1. Design principles & Dotan’s taste

### 1.1 How decisions get made
Source: `/home/box/company/ux-knowledge/motion-animation-graphics.md`

- Live session: nudge position/size, ask for more variations; checkpoints = rollback.
- He makes the design choices; agents prepare options and review.
- Accepted changes are committed so they can be rolled back.

### 1.2 Experience promise (Saylo product UX)
Sources: `/workspace/saylo/chats/saylo-ux-audit/summary.md`, `/workspace/saylo/chats/INDEX.md`

- Dotan (problem): «אין flow מסודר… דברים לא מתחברים… המסכים לא מספיק נקיים» — disconnected flow, screens not clean enough; concept/timing/colors/atmosphere “quite good”.
- Wanted: Apple-like **wow + efficiency** (not Apple branding); automation prominent; user can still edit/fix; wizard for each step of a chosen path.
- Feeling: **«One project the system advances for me, and I step in where I want.»**
- Principle: **system proposes a complete result; user opens the decisions they care about.** Do not walk the user through the mechanism (transcribe → verify → moments → …).
- No single mandatory brand→revenue mega-path. Connect via shared objects: Brand, Project, Output (versions), Publication, Campaign. «Services stay independent; the work stays shared.»
- Hierarchy of attention: **the work itself → the current decision → details on demand.**
- Intent entry (generative): «מה היית רוצה שנעשה עבורך?» / “What would you like to make happen?” — field never moves; completions are suggestions (Tab / tap); UI changes by **meaning after a pause**, not per keystroke.
- Processing must show **content being built**, not empty spinners/skeletons. Costs in human language, not vendor/dev units. No pipeline jargon in UI.

### 1.3 Visual language (Saylo on-theme)
Sources: chats INDEX §visual language; ux-design-system REPORT; Explainit mockups note in motion-animation-graphics.md

| Token area | Taste |
|---|---|
| Surfaces | White → pale lavender gradients; lavender-tinted cards |
| Primary | Deep plum / aubergine CTAs; purple accents |
| Type | Serif display headlines (Frank Ruhl Libre used for Hebrew serif in design-system install); one accent word often stressed |
| Bots | Glassy iridescent lavender “jelly” creatures, two glossy black eyes, pearly pastel |
| Logo | Saylo ✦ |
| Dark | Explicit dark-plum mode exists in approved audit screens (`__10`, `__13`, `__16`) — keep as first-class theme, not afterthought |
| Off-theme | Dark navy/neon music UI; Sep 24 Play exploration (orange/teal/neon); generic saturated purple editors — idea only |

**Explainit binding look (product-specific):** light lavender; plum serif headings; purple primary; EN|עב. Binding mockups: packages under explainit shell-stage / original-refs (see Sources).

### 1.4 Video / film motion taste (client films, Oct 2026)
Source: motion-animation-graphics.md

- Text readable: ~1 s after last text appears before cut; ~2 s on dense cards (email/contact).
- End on clean end page: logo only; corner badge = symbol only (no wordmark).
- Show every render **raw and fast** (minutes, not hours) before polish checks.
- Desktop 16:9 = **native re-layout**, not letterboxed mobile (artwork one side, word column other, wider wipe bands).
- Music: his Suno tracks; fade out; ~−14 LUFS / −1 dBTP.
- Brand’s exact logo palette for themed videos.
- Reels style he liked: varied angles, drone, rising smoke/lift, speed changes.

### 1.5 Product UI cross-cutting gaps (targets for any service)
Source: `/workspace/saylo-product/UX-GAPS-SECTION7.md`

- One token set; shared components (cards, sheets, chips, stepper, player, waveform).
- Full i18n/RTL; SVG icons only (no icon-font name leakage).
- Every screen: empty / loading / progress / error-with-retry / gate-fail-with-reason; mock data labelled.
- Mobile **390 first**, desktop 1440; ≥44 pt targets; AA contrast; sheets ≤40% height; player never pushed off.
- Creator controls over raw ms fields; exact values behind Advanced.
- Style/options = **live gallery**, never A/B pick cards alone.
- Shared player pattern; one stepper: Intake › Plan › Approve › Generate › Review › Export. Default = automation with “let me adjust”.

---

## 2. UI/UX patterns & critic rubric

### 2.1 Concept patterns (three end-to-end directions)
Source: `/workspace/saylo/ux-design-system/CONCEPTS-README.md`

| Concept | Idea | When it fits |
|---|---|---|
| **A · Guided path** | Calm, learnable; persistent path; Home / My work / My apps; side companion | First visit, clarity |
| **B · Living studio** | Prepare / Create / Manage; bots on the content; Pause / Take over; most canvas | Repeat power users |
| **C · Conversation-led** | Growing thread; composer pinned; approval cards in thread; dark plum first | Phone / human feel; harder to scan |

Shared: 11 steps (`entry…publish`), `?theme=`, `?lang=`, `?motion=reduce`, Mix (`?mix=step:concept`), 300 ms step fade (off under reduced motion).

### 2.2 Critic loop (how to score work)
Sources: REPORT.md, PLATEAUS.md, SCORES.md

- **Pass:** ≥ 9.0, no must-fix.
- **Consensus:** 2 independent runs on **pinned** evidence; mean if spread ≤ 0.3; else median of 3. Must-fix = max across runs.
- **Variance warning:** run 1 that also carries detector/a11y context often scores **0.3–0.7 higher** than blind reruns — do not trust single-run peaks.
- **Plateau:** flat (<0.2 gain / two rounds post-diagnosis) → freeze with blockers (usually **real art/media** or product decisions, not more CSS).
- **Tools installed in design-system worktree (for agents):** Impeccable; emilkowalski/skills; vercel-labs web-design-guidelines; Leonxlnx taste-skill; ui-ux-pro-max (skill); greensock/gsap-skills; gsap + @gsap/react; lenis; Playwright shot broker; a11y probe (`prefers-reduced-motion`, EN/HE × 1440/390).

### 2.3 Critic checklist (durable criteria)
Use these dimensions when reviewing screenshots or live UI:

| Axis | Ask |
|---|---|
| Spec / ref fidelity | Matches approved mock almost exactly? |
| Hierarchy | Work → decision → details? One primary next action fixed? |
| Readability | Type ≥ ~13 px for meta; contrast AA; Hebrew glyph quality |
| States | Empty / loading (content building) / error+retry / success |
| Continuity | Stable shell; player doesn’t jump; step count doesn’t thrash |
| Motion evidence | Real motion or only stills? Reduced-motion path? |
| RTL parity | HE layout mirrored; no EN leaks; times with `bdi` |
| Phone 390 | Content first; chrome doesn’t eat the canvas; no dead bands |
| Identity | On-theme palette/type — or correctly flagged off-theme idea |
| Cost honesty | Human wording; no contradicting “no charge” lines |
| Detector | Impeccable AI-tells cleared (beige, italic serif spam, pulsing dots, side-tabs, purple gradient + three rounded cards…) |

**Play kinetic / caption craft notes (from R7 critiques):** stressed Hebrew glyphs need clean stroke/shadow (no corner stepping); accent progress = thin gold bar (no times on feed card); captions as Saylo layer over video; identity legible over full-bleed speaker.

### 2.4 Anti–AI-slop stack (install order for agents)
Sources: ui-ux-upgrade.md; KB items A0823, A1000, A0995, A0793, A0794, A1113

```bash
# Design vocabulary + detector
npx impeccable install && npx impeccable init
# Commands: audit | polish | critique | shape | document | extract | live | generate

# Animation + polish craft (Emil Kowalski)
npx skills@latest add emilkowalski/skills
# Notable: animate, review-animations, improve-animations, find-animation-opportunities,
# mobile-native, break-ui, ask-sonner, prototype, pick-ui-library, animate-expo

# Official GSAP patterns for agents
npx skills add https://github.com/greensock/gsap-skills
# Modules: core, timeline, ScrollTrigger, plugins, utils, react (useGSAP/cleanup/SSR), performance, frameworks

# Taste / landing art direction
npx skills add https://github.com/Leonxlnx/taste-skill --skill "design-taste-frontend"

# Audit vs Vercel Web Interface Guidelines (forms, a11y, animation, UX)
npx skills add vercel-labs/agent-skills --skill web-design-guidelines

# Optional: UI UX Pro Max (design-system generator, GSAP presets)
# npm i -g ui-ux-pro-max-cli && uipro init --ai claude|cursor|codex

# Optional: Figma → code
npx skills add figma/mcp-server-guide --skill implement-design
```

**Impeccable polish prompt (verbatim from KB):**
```text
/impeccable polish the pricing page. Keep our sharp corners and sober palette. Remove the AI tells.
```

**DESIGN.md** = contract between design system and coding agents (Google pattern A0765): YAML tokens + markdown “why”. Also: awesome-design.md / getdesign.md brand files as starting points — then rewrite to **this** product’s taste.

**Security:** installing a third-party skill = trust. Read SKILL.md first; avoid anonymous fresh repos with broad permissions (A0827).

---

## 3. Motion & animation

### 3.1 Web animation toolkit (Dotan tip, 2026-10-31)
Source: motion-animation-graphics.md · Instagram https://www.instagram.com/p/DfKwce8kuAV/ (theopenstack)

Problem called out: AI-built sites feel static — no scroll animation, hover, or transitions.

| Skill / lib | Role | Notes |
|---|---|---|
| **GSAP Skills** | Install first | ScrollTrigger, fade-ins, staggered reveals, page transitions (~80% of site needs) |
| **Animate** (Emil) | Easing & timing | Pair with GSAP; ask “do we need to animate?”; transform/opacity only; reduced-motion |
| **Remotion** | Video in code | Kinetic typography intros; company license if ≥4 people / SaaS automator pricing |
| **Rive** | Interactive UI animation | Named in post; full install links gated in comments (“ANIMATE”) — **not captured** |
| **Lottie** | Vector animations | Named; details not in post body |
| **Three.js** | 3D in browser | Named; details not in post body |

Use for marketing sites and landings; always `prefers-reduced-motion`; protect LCP/CLS.

**Related official GSAP skills reel (WhatsApp KB):** A0794 — https://www.instagram.com/reel/DXKJ4NxDekW/ — 8 modules including React helpers and performance.

### 3.2 Library chooser (web UI)

| Need | Prefer | Avoid / caution |
|---|---|---|
| Scroll reveals, timelines, stagger | **GSAP + ScrollTrigger** (+ @gsap/react `useGSAP`) | DIY rAF without cleanup |
| Smooth scroll feel | **Lenis** (A1008) | Fighting native scroll accessibility blindly |
| Micro UI / copy-paste React bits | **React Bits**, Magic UI (named in prompts), 21st.dev | Over-animating work surfaces |
| WebGL hero backgrounds | **Vanta.js** (~5 lines), **Unicorn Studio** (75+ effects + MCP), **vgpu** (Vercel shaders, agent-visible) | Heavy WebGL on every route |
| Interactive 3D object | **Spline** (+ MCP), Three.js | 3D on dense editor chrome |
| Scroll-scrubbed product object | Image/video → frame sequence + **GSAP ScrollTrigger** (A0629 AirPods pattern) | Autoplaying huge MP4 without poster/LCP plan |
| App toasts | Sonner (`ask-sonner`) | Custom toast stacks per screen |
| Code → MP4 explainers | **HyperFrames** (Apache-2.0) or Remotion (license!) | Paid i2v for abstract B-roll |
| Interactive UI motion files | Rive (named; capture incomplete) | — |
| Icon/vector loops | Lottie (named; capture incomplete) | Giant JSON on critical path |

**GSAP license note (from Motionit / web-research):** free for commercial use including plugins since Webflow acquisition; **do not** embed GSAP inside a no-code animation builder that competes with Webflow. For an in-product freeform animation editor, prefer Anime.js / WAAPI / CSS until legal clears.

### 3.3 Recipes (from captured sources)

**A. Scroll-scrubbed 3D-ish object (landing “how it works”)** — A0629  
1. Generate source still (structured JSON prompt: camera, lens, focal length, light).  
2. Image→video (e.g. Veo).  
3. Agent extracts frames.  
4. GSAP ScrollTrigger maps scroll progress → frame index (AirPods-style).

**B. Villa / space tour scroll video** — A0940  
Room stills → video between keyframes → image sequence → scrub on scroll (Claude build).

**C. Continuity motion in product shell** — saylo-ux-audit summary  
- Home episode image expands into workspace.  
- Reel selection moves in strip; tool panel swaps briefly; content stays.  
- Finished job replaces progress with real output **in the same card**.  
- Duration **180–300 ms**; reduced-motion = instant swap / fade none.

**D. Emil `animate` defaults** — A1000 / skills list  
- Skip animation if control is used constantly.  
- Animate only transform/opacity.  
- Always gate with `prefers-reduced-motion`.

**E. Code-drawn film / explainer (Motionit)** — `/workspace/saylo-brain-pkg/kb/motionit.md`  
- Pipeline thesis: HTML/CSS/JS/Canvas/Three → HyperFrames/Remotion → MP4.  
- `frame = f(t)` single-file canvas (Avi Levi 55 styles pattern) for deterministic headless render.  
- Voice first; visuals timed to words (exposure sheets).  
- Revise by **timecode** (“second 20 too busy”).  
- Self-check / frame QA loop before export (Dana Akerman / Mortiflix architecture — learn pattern; respect licenses).  
- Style decode: moodboard → Claude “decode colors, motion, texture” → locked style block.  
- Vox-style ads: paper bg + cutouts + kinetic callout arrows in **code**; photoreal product shot only where needed.

**F. Film timing (client)** — motion-animation-graphics.md  
Real dwell on timeline; no freeze-frame padding; readable text hold; clean logo end card.

### 3.4 Performance & reduced-motion

- Critical path: defer non-hero motion; no layout-thrashing properties in loops.  
- GSAP performance skill: avoid animating `top/left/width/height`; batch reads/writes; kill tweens on unmount (`useGSAP` context).  
- Image sequences: size for DPR, lazy below fold, poster for LCP.  
- Unicorn/Spline/Vanta: one hero instance, destroy on route leave.  
- Always provide:
  ```css
  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
      animation-duration: 0.01ms !important;
      animation-iteration-count: 1 !important;
      transition-duration: 0.01ms !important;
      scroll-behavior: auto !important;
    }
  }
  ```
  Plus JS early-exit when `matchMedia('(prefers-reduced-motion: reduce)').matches`. Preview flag `?motion=reduce` in Saylo UX previews.

### 3.5 Motion graphics engines (when the deliverable is video, not live DOM)

| Engine | License snapshot | Use |
|---|---|---|
| HyperFrames | Apache-2.0; cloud render ~$0.10/min 1080p30 | Default code→MP4 |
| Remotion | Free solo; company license 4+; SaaS automators $ | Strong React ecosystem; check license before productize |
| Claude Motion | Artifact beta; **no API / no Code skill** | Inspiration only |
| Seedance / Kling / Veo | Paid | Realism, clay, live-action look |

Hebrew RTL proof case: HyperFrames + GSAP Pac-Man explainer (Max Gomberg) cited in motionit.md.

---

## 4. Effects for websites

| Effect class | How | Source |
|---|---|---|
| Fade / slide / stagger on scroll | GSAP ScrollTrigger | toolkit, A0794 |
| Page transitions | GSAP timelines | toolkit |
| Hover / press micro | CSS or Emil animate; keep short | Emil skills |
| Smooth scroll | Lenis | A1008 |
| Kinetic / split text | GSAP SplitText (free now) or CSS | GSAP skills |
| WebGL ambient bg | Vanta / Unicorn / vgpu | A1008, A0586, A1073 |
| Parallax layers | GSAP or CSS; respect reduced-motion | general |
| Scroll-driven video/sequence | Frame scrub (A0629, A0940) | KB |
| 3D embed | Spline / Three | A0722 |
| Shader on real DOM | HTML-in-canvas / Remotion experiments (flagged APIs) | A0801 — experimental |
| Component libraries with motion | React Bits, Animaster Live, Skiper UI, Vengeance UI, 21st.dev | A1012, A0172 |
| “AI sites look static” fix pack | Unicorn 64–75 effects + MCP | A0611, A0586 |

**Landing / SiteIt product intent** (workflow, not visual system):  
Source: `/workspace/saylo/chats/landing-page-creation/`  
Promise: «from your content to a page ready to publish» — not a broad site editor. Start with **campaign pages**. Needs: mobile, **Hebrew/RTL**, URL/domain, basic analytics. Names: Landit (LP-focused) / SiteIt (full sites later).

---

## 5. Website building workflow (agent recipe)

Sources: ui-ux-upgrade.md §1–7, A0609, A0959, A0765, landing-page-creation, design-ui synthesis

1. **Lock taste first.** Write or load `DESIGN.md` (colors, type, spacing, motion verbs, do/don’t). Without this, agents default to purple-gradient AI slop (A0959: “taste file is the whole trick”).
2. **References before pixels.** Refero / real product screens / Dotan’s approved mocks. Prompt pattern: *“design X; research how Linear and Notion handle theirs first”* (A0957).
3. **Structure.** Sitemap → wire → high-fi. Relume-style for IA if greenfield (A0197). For Saylo marketing: content → page → CTA loop with PushIt later.
4. **Build in code with skills loaded** (§2.4). Prefer one stack (e.g. React/Vite or Next + scoped CSS or Tailwind — match the host repo; Saylo editor historically avoided shadcn preflight on the shipping app).
5. **Motion pass.** GSAP Skills + Emil `find-animation-opportunities` / `improve-animations`. Marketing: scroll + hover. App chrome: continuity only.
6. **RTL pass.** See §6. Screenshot EN and HE at 1440 and 390.
7. **Audit loop.** Impeccable detect → polish → web-design-guidelines → Playwright screenshots → (optional) cloud critic ≥9.
8. **Live session with Dotan.** Localhost; variations on page; no A/B pick; commit accepted state.
9. **Perf.** LCP image, CLS from fonts/motion, reduced-motion, kill WebGL on leave.

**Clone-as-inspiration workflow (A0609):** pick vibe template → copy Inspect HTML/CSS → give agent link + HTML/CSS + screenshot → ~90% clone → iterate on “ugly parts” with cropped screenshots. Use as inspiration; respect copyright.

**Cursor tip (A0851):** attach reference image — *“make the top artists page look closer to the image with artist photos”*.

---

## 6. RTL / Hebrew

Sources: UX-GAPS U2; motion-animation-graphics; INDEX; Play R7 critiques; frank-ruhl-libre install in REPORT

- Visible **EN | עב** (or EN | HE) switch on every surface; `lang` + `dir` on root.
- Mirror layout: start/end not left/right; flip directional icons (chevrons, back).
- Numbers and times: wrap in `<bdi>` / `dir="ltr"` isolates so `0:45 / 3:20` and `פרק 184` don’t scramble.
- Fonts: pair Latin + Hebrew; Frank Ruhl Libre used as self-hosted Hebrew serif in design-system work. Stress glyphs (e.g. «לא») need clean outline/shadow — test crops at 3×.
- No mixed-language UI (English icon names, “Idea 1”, etc. leaking into HE).
- Content language vs UI language may differ (settings gap U2) — label both.
- Captions / kinetic type: RTL line-breaking; page direction follows spoken language.
- Marketing pages and SiteIt/Landit: Hebrew/RTL required from v1 (landing-page-creation).
- Proof that code-drawn motion works in Hebrew: HyperFrames+GSAP Pac-Man (motionit #73).

---

## 7. Sources index

### Canonical short docs
| Path | What |
|---|---|
| `/home/box/company/ux-knowledge/motion-animation-graphics.md` | Standing preferences + web toolkit tip |
| `/home/box/company/ux-knowledge/UX-MOTION-WEB-KNOWLEDGE.md` | **This file** |
| `/workspace/ai-knowledge/ui-ux-upgrade.md` | Full KB distillation for UI polish (117 items) |
| `/workspace/ai-knowledge/kb/README.md` | WhatsApp AI groups KB (1060 items) |
| `/workspace/ai-knowledge/kb/categories/visual/design-ui.md` | UI/sites synthesis |
| `/workspace/ai-knowledge/kb/categories/visual/animation.md` | Web/3D animation synthesis |
| `/workspace/saylo-brain-pkg/kb/motionit.md` | Code→video MG playbook from WA/IG |
| `/workspace/saylo/chats/INDEX.md` | 33 ChatGPT export chats synthesis |
| `/workspace/saylo/chats/saylo-ux-audit/` | Whole-product UX audit + generative entry |
| `/workspace/saylo/chats/landing-page-creation/` | SiteIt/Landit intent |
| `/workspace/saylo/ux-design-system/REPORT.md` | Critic-to-9 loop, installs, scores |
| `/workspace/saylo/ux-design-system/PLATEAUS.md` | Freeze rules + blockers |
| `/workspace/saylo/ux-design-system/CONCEPTS-README.md` | A/B/C concept patterns |
| `/workspace/saylo-product/UX-GAPS-SECTION7.md` | Cross-cutting UI targets |
| `/workspace/saylo/play/SAYLO-PLAY-VISION.md` | Play vision (consumer) |
| `/workspace/saylo/play/r7-merged/CRITIQUE*.md` | Kinetic/caption craft reviews |
| `/workspace/saylo-wa/` | Raw WhatsApp crawl catalogs + repos notes |

### Key external links (captured)
- GSAP skills reel: https://www.instagram.com/reel/DXKJ4NxDekW/ (A0794)
- Web toolkit post: https://www.instagram.com/p/DfKwce8kuAV/ (theopenstack)
- Lenis/GSAP/Vanta/React Bits: https://www.instagram.com/reel/Da3O00jpo3R/ (A1008) — Dotan tagged “For website”
- Impeccable: https://impeccable.style/ (A0823)
- Emil skills: github.com/emilkowalski/skills
- greensock/gsap-skills · heygen-com/hyperframes
- Unicorn Studio, Spline, Refero, DESIGN.md / awesome-design.md — see KB item files under `/workspace/ai-knowledge/kb/items/`

### WhatsApp corpus note
The durable **extracted** knowledge from Dotan’s WhatsApp groups (**סדנת AI**, **הרצאת AI לא רק למפתחים**) lives in `/workspace/ai-knowledge/kb/` (1060 cataloged items) and the Motionit/brain distillations under `/workspace/saylo-brain-pkg/` and `/workspace/saylo-wa/`. This file is the **coding-agent slice** of that corpus (design + web motion). For a single tool or reel, open `items/Axxxx.md` or `motionit.md`.

---

## Referenced, content not captured

Agents must not invent these; fetch or ask Dotan to re-share if needed.

| Reference | Why missing |
|---|---|
| Instagram DfKwce8kuAV comment gate **“ANIMATE”** → full list of 8 skill install links | Post body names GSAP, Animate, Remotion, Rive, Lottie, Three.js only; comment pack never fetched (noted 2026-10-29 in motion-animation-graphics.md) |
| Rive / Lottie concrete recipes, repos, install commands | Named in toolkit tip only; no WA item distilled into step-by-step in the sources read for this pack |
| Framer Motion / Motion, Aceternity, Magic UI (beyond one mention), dedicated form-library guides | Explicit KB gap in ui-ux-upgrade.md intro |
| animation-principles skill (#10 DeHGxXnolMn) | Gated; not received |
| Web Lab AI / STYLES / Editor / FILM comment gates; AiKAMI PDF skill; framelab Notion full text | Behind IG/Drive gates; partial notes only in motionit.md |
| Mortiflix OSS | AGPL — architecture learn-only; do not vendor code |
| Avi Levi 55 MG styles full prompts | Copy under saylo-wa `prompts-verbatim/`; **no clear commercial license** — rewrite or get permission before shipping |
| Full-content-service ChatGPT “really really cool” video-in-UI mockup series | ~64 mockups claimed in conversation history; only 27 images in export (dark/off-theme) — gap still open |
| Raw WhatsApp export folders as a single zip for handoff | Knowledge is in KB markdown, not one “WhatsApp dump” file beside this pack |
| Managed agent skills under `/home/box/agent-data/workflows` | Only EM ops skills present; UX/motion skills live as **project installs** (Impeccable, Emil, GSAP) and in the WhatsApp KB, not as box managed-skills |

---

## Quick agent prompt (paste when starting work)

```text
Read /home/box/company/ux-knowledge/UX-MOTION-WEB-KNOWLEDGE.md.
Follow TL;DR rules. Match Dotan’s taste and METHOD.
For marketing/landing: GSAP Skills + Emil animate + DESIGN.md; reduced-motion; EN|עב.
For product UI: continuity 180–300ms; no A/B picks; galleries side-by-side; critic bar 9.0.
Do not invent gated Instagram comment packs. Cite source paths when you claim a rule.
Ship screenshots EN+HE × 1440+390 before review.
```

_End of pack._
