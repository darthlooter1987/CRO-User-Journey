# CRO User Journey — Project Instructions

> **For the colleague taking this over:** paste the contents of this file into the "Project instructions" field of your Cowork project (the same field where the original instructions live). Everything Claude needs to continue the work coherently is in here. The rest of the project lives as files in this folder.

---

## 1. What this project is

Revmatics is building a CRO (Conversion Rate Optimization) tool. The flagship user journey is:

> *"Give us your product URL, and we'll generate a complete set of fit-for-purpose landing pages — one for each stage of the buying funnel: Awareness, Differentiation, Conversion, and Loyalty."*

The work in this folder is the product design surface for that pitch — PRDs, clickable HTML mockups, and supporting decks. It started as a single PRD ask and has grown into four parallel workstreams (see Section 4).

## 2. The user we are designing for

**Persona:** Small business owner running a Shopify store. They have a product, a budget for ads, and no marketing team. They do **not** understand purchase funnels and don't know why a social-media ad should go to a different landing page than a retargeting ad.

**Core user story:**
> *As a small business owner with a Shopify account, I need to be educated on marketing activities in order to see the value in using the CRO tool. I need to understand what the stages of a purchase funnel are and why I am using different landing pages to facilitate different outcomes in different campaigns.*

This persona drives two non-negotiable product principles:
- **Education happens inside the product**, never in a help doc.
- **Zero friction at the front door** — one URL input, no signup, no questionnaire.

## 3. How we work together (read this before generating anything)

These are the feedback rules I've already established with Claude. Carry them forward.

**3.1 — Always update the index when delivering new versions.**
Whenever you ship a new version of a screen or PRD, update **both** the summary cards **and** the version tables inside `index.html`. The index is the canonical entry point — if a version isn't on the index, it doesn't exist as far as the team is concerned.

**3.2 — Stripe Dashboard is the north star for CRO Reporting.**
V1 of the reporting screens was dropped because it was too cluttered, didn't feel like a modern SaaS product, and the screens felt disconnected from each other. V2 (the current direction) takes its cues from the Stripe Dashboard: clean, spacious, data-dense but not noisy, with strong typography hierarchy and confident decision-orientation. When in doubt, ask "would Stripe ship this?"

**3.3 — Build to feel like premium 2026 B2B SaaS.**
Card-based layouts, sticky top bar, left sidebar nav, soft dividers, subtle shadows, rounded corners. Desktop-first but responsive. Decision clarity over metric overload — use progressive disclosure rather than dumping every number on screen.

**3.4 — Respect the analytical logic in the reporting brief.**
A single landing page with no tested alternative must **never** be labeled a "winner" — only pages that beat another page in a structured comparison can be winners. Single pages get a *Performance Status* (Strong / Average / Weak / Needs data). A/B tested pages get an *Experiment Status* (Winner / Losing / Inconclusive / Not enough data). Every page also carries a *Traffic Context* tag (Paid / Organic / Mixed), and traffic context influences which metrics get visual prominence.

**3.5 — Versioning convention.**
- Mockup files: `<workstream>-v<major>.<minor>.html` (e.g., `cro-reporting-v2.2.html`).
- PRD files for a workstream: `prd-<workstream>-v<major>.<minor>.html`.
- Suffix variants with a letter (e.g., `v1.3m` for a Marie variant, `v1.0a` for an Alex variant) when exploring divergent directions.
- Don't delete old versions — archive them on the index with the `status-archived` badge.

## 4. The workstreams (what's actually in this folder)

The project has four active workstreams. They share the same persona and design system but solve different stages of the product experience.

**4.1 — Fit-for-Purpose Landing Pages (the original ask).**
The eight-screen end-to-end concept: URL entry → brand extraction → brand review → funnel education → dashboard with four funnel cards → page editor → guided walkthrough → paywall. The full narrative lives in `CRO Page Concept - Boss Pitch Speech.md` — read this first to understand the product intent. PRD: `Fit-for-Purpose CRO Landing Pages PRD.docx` (full) and `... - Lean.docx` (trimmed). Mockup versions: `v1.0.html`, `v2.0.html`, `v3.0.html`, `v3.1.html` plus the matching `prd-vX.html` files.

**4.2 — CRO Reporting.**
The post-publish analytics surface. V1 was scrapped (see rule 3.2). V2 is the current direction and is split across three screens:
- `cro-reporting-v2-screen1.html` — all-pages portfolio view
- `cro-reporting-v2-screen2.html` — single-page deep dive
- `cro-reporting-v2-screen3.html` — experiment / A/B test view
Plus consolidated versions `cro-reporting-v2.1.html` and `v2.2.html`. The design brief lives in `CRO Reporting Brief.md` — that file is the source of truth for the analytical logic.

**4.3 — A/B Testing.**
Live experiment setup and management. Multiple parallel explorations: `cro-ab-testing-v1.0.html` through `v1.5m.html`, with `m` and `a` suffixes denoting different design directions. PRD lives in `revmatics_ab_testing_prd (1).docx`.

**4.4 — 3rd-Party Setup.**
Onboarding for users coming from outside the Shopify ecosystem (or wiring up external tools). `cro-3rd-party-setup-v1.0.html` and `prd-cro-3rd-party-setup-v1.0.html`.

**`index.html`** ties all four workstreams together as a design library. It's the file to open first to see what currently exists and which version is "current" for each workstream.

## 5. Source materials worth reading before generating

In rough order of usefulness for picking up the work:

1. `CRO Page Concept - Boss Pitch Speech.md` — the 3-minute pitch that explains the *why* behind every screen of the flagship flow. Start here.
2. `CRO Reporting Brief.md` — the analytical logic and design brief for the reporting workstream. Treat this as a spec, not a suggestion.
3. `Wednesday PRD Review - 2026_04_01 09_55 EDT - Notes by Gemini.docx` — the original notes that kicked off the project. Useful for understanding the original ask before it expanded into four workstreams.
4. `index.html` — open in a browser to see the current state of every deliverable.
5. The most recent versioned mockup of whichever workstream you're working on.

## 6. Visual system (so new screens stay coherent)

Pulled from the existing CSS in `index.html` and the V3 mockups — match these unless you have a deliberate reason not to:

- Primary: `#2E5090` (with light `#4A7BC7` and dark `#1E3A6E`)
- Accent: `#00B4D8` · Success: `#06D6A0` · Warning: `#F77F00` · Loyalty: `#9B5DE5`
- Background: `#F0F4FA` · Card: `#FFFFFF` · Border: `#E2E8F0`
- Text: `#1E293B` (primary) / `#64748B` (light)
- Radius: 12px · Font: Segoe UI / system stack
- Shadow: `0 2px 16px rgba(0,0,0,0.07)` (default), `0 8px 40px rgba(0,0,0,0.12)` (elevated)

## 7. Where things stand (as of 2026-05-14)

- Flagship landing-pages flow is at v3.1, with a matching PRD.
- CRO Reporting is at v2.2 after the V1 reset. The Stripe Dashboard direction is working — keep going.
- A/B Testing is in active exploration with parallel `m` and `a` variants; no version has been "blessed" yet.
- 3rd-Party Setup is at v1.0 — earliest stage of the four workstreams.

The next likely asks are: continued iteration on A/B Testing toward a single chosen direction, and tightening the link between the Reporting screens and the Landing-Pages dashboard so the two products feel like one.

## 8. Operating defaults for Claude

When working in this project, default to:
- **Output as HTML mockups** for any screen design — single-file, inline CSS, no build step, ready to open in a browser.
- **PRDs as `.docx`** (use the `docx` skill) when the user asks for a written spec, or as standalone `.html` when the user wants something inspectable in a browser alongside the mockup.
- **Always update `index.html`** when delivering a new version (rule 3.1).
- **Ask before starting** if a request is underspecified — especially "which workstream" and "is this a new version or an edit to an existing one."
- **Don't invent metrics or copy** for the small-business persona — flag placeholder text clearly so it's obvious what still needs the user's judgment.

---

*Last updated by Alex on 2026-05-14 as a handoff. If you (the colleague) change direction on anything in Section 3, update this file so future-Claude inherits the new rules.*
