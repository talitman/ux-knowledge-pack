# Motion, animation & graphics: Dotan's standing preferences (shared UX knowledge)
Maintained by Saylo UX/UI Manager. Last updated 2026-10-29. Applies across Dotan's products unless a product note says otherwise.

## How design decisions get made
- Every design decision is made in a LIVE session: Dotan watches the real UI and steers it in real time (nudge position and size, ask for more variations). The setup is hot reload, a tweak panel, a variations gallery, and checkpoints with rollback.
- No A/B "pick one" rounds. Variant rounds and critic scores are only prep for a session, never the decision.
- When he's at his Mac, the session opens locally (localhost, brought to the front), not through a tunnel link. Tunnel links are only for remote use, and link previews consume them.
- He makes the design choices himself. Show directions side by side; don't pick for him.
- Built screens must match his selected mockups almost exactly (fonts, colors, spacing, buttons, text), not loosely.
- Bilingual UI (English and Hebrew, RTL) with a visible EN | עב switch.

## Video / motion rules (learned from client films, Oct 2026)
- NEVER extend timing with freeze frames (ffmpeg tpad/clone). He rejected this because it broke the transitions and animation. Extra time has to be real dwell added to the renderer's scene timeline, with ambient motion still running.
- Text must stay on screen long enough to read. After the last text in a scene appears, leave about 1 s before the cut, and about 2 s on dense scenes like an email/contact card.
- End on a clean end page with the logo only. A corner badge is the symbol only, with no wordmark.
- Show him every rendered version raw and fast (minutes, not hours), before polishing checks.
- Desktop (16:9) versions must be native re-layouts, not letterboxed mobile: artwork on one side, a word column on the other, and wider wipe bands.
- Music: he makes his own tracks in Suno (no license check needed). Fade it out at the end, mixed to about -14 LUFS / -1 dBTP.
- Use the brand's exact logo palette for themed videos.
- Reels/cinematic style he liked: varied camera angles, drone shots, rising smoke/lift, speed changes.

## Source material on the box
- /workspace/ai-knowledge/ui-ux-upgrade.md: the UI/UX upgrade plan (KB items, top 10, phased plan).
- /workspace/ai-knowledge/kb/: the full UX/motion knowledge base (prepared by the Ai knowledge bot).
- /workspace/client-film-r2/: approved client film work (9:16 and 16:9 share copies, contact sheets), as examples of approved motion.
- /workspace/explainit-shell/original-refs/: Explainit's binding mockups (Saylo-specific; light lavender, plum serif headings, purple primary).
- /workspace/saylo/play/user-refs/: Dotan's favourite reference images for Saylo Play (Saylo-specific).
- Company compute policy: /home/box/company/policies/compute-routing.md

## Note for other products
Saylo palettes and mockups are Saylo-only. Reuse the METHOD and the motion rules above, not Saylo's visual identity.

## Web animation toolkit for AI-built sites (Dotan's tip, 2026-10-31)
Source: https://www.instagram.com/p/DfKwce8kuAV/ (theopenstack): 8 free, open-source Claude skills for animation. AI-built sites often feel static, with no scroll animation, hover effects or transitions.
- GSAP Skills: install first. Scroll triggers, fade-ins, staggered reveals, page transitions (about 80% of what sites need).
- Animate: easing and timing. Pair it with GSAP.
- Remotion: video rendering in code (e.g. kinetic typography intros). Relevant to Saylo/Explainit films.
- Rive: interactive UI animation.
- Lottie: vector animations. Three.js: 3D scenes in the browser.
- The post names only these. The full list of 8 links is in the post's comments (comment "ANIMATE"), and it hasn't been fetched yet.
Use for: marketing sites and landing pages (scroll reveals, hover, transitions), always with prefers-reduced-motion support and without hurting LCP/CLS.
