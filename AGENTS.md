# AGENTS.md — uniscene-prototypes

> **Single source of truth for all AI tools.** Edit rules HERE. Claude reads via `CLAUDE.md` → `@AGENTS.md`.

## What
Static, self-contained HTML prototypes for **UniScene** — the visual/UX exploration layer that feeds the real app in `student-portal`. Decide design direction here cheaply, then port the winner into `student-portal`'s design tokens.

## Product proposition
- **UniScene** — Pakistani student discount platform, Lahore launch first. Tagline **"On hai"**
- Core loop: onboard → sign in → verify (once) → browse offers → reveal a single-use code → checkout → saved
- Pakistan only. **Monetization parked** — never prototype payments/pricing/affiliate flows

## Design standard — POP / FIESTA
Neo-brutalist, loud, friendly. **FIESTA** (`fiesta.html`) is the lead; **POP MINI** (`popmini.html`) same energy with small square cards.

When editing: reuse existing tokens/classes — don't invent new ones:
- **Onboarding = yellow** (`var(--sun)` `#FFC233`)
- Display: `Bricolage Grotesque` (800); body: `Hanken Grotesk`; ink: `#221A3B`
- Signatures: chunky headlines, marker highlights (`.hl` in berry/grape/mint/mango), 3D emoji badges, `.btn` with 5–6px hard shadows
- Mobile-first inside `.phone` frame (max 440px). Add screen: new `<section class="scr" id="s-x">` + `data-go="x"` — no JS change needed

## Practices
- Iterate locally; push only once screen/direction is agreed between collaborators (Waqar + Shaheer)
- Keep prototypes standalone — no frameworks, no shared assets, no network deps beyond fonts/placeholder images
- Don't break existing journeys: every `data-go` must resolve to a real `#s-` section
- Match surrounding file's style exactly (tokens, class names, shadow weights)

## Identity
- Personal repo (`shaheermahaar/uniscene-prototypes`) → commits as `Muhammad Waqar Iqbal <waqarmahar1989@gmail.com>`. No AI attribution.

## Memory
Long-term history and past decisions live in **MemPalace** (wing: `uniscene`). Query: `mempalace_search(query="...", wing="uniscene")`.
