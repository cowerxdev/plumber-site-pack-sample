---
name: plumber-site-pack-sample
description: "Plumber Site Pack (free sample) for Claude Code: a header and call button hero, one headline pattern and the Ohio homepage evidence behind them. Use when asked to build, redesign or restyle a website, homepage or landing page for a plumber or plumbing company."
---
# Plumber Site Pack (free sample)

This folder is a design pack for plumber websites: design tokens, page components, copy patterns, and
the evidence behind each choice. Use it whenever you are asked to build, redesign or restyle a site for a plumber or plumbing company.

1. Read `AGENTS.md` in this folder before you write any code. It holds the full rules, and they win over your
   own design habits. Then read `EVIDENCE.md`.
2. Copy `tokens/` (with its fonts) and `components/pack.css` into the site's own folder and link them from
   there. Never link into `.claude/`. Build the page from `components/*.html` in the order `AGENTS.md` gives.
3. Open `preview.html` to see the target.

## Non-negotiables
1. Show a tap-to-call link (`href="tel:+1..."`) without scrolling on a 375px-wide phone, in both header and hero.
2. Every call button shows the phone number as text (`Call (614) 555-0142`), except the compact header button on phones, where the hero button shows it.
3. Use `--pk-color-call` only for tap-to-call links.
4. Serve the finished page over HTTPS and include `<meta name="viewport" content="width=device-width, initial-scale=1">`.
5. Keep tap targets at least `--pk-tap-min` (48px) tall.

## Promises
A promise (licensed, insured, 24/7, pricing, guarantees and the rest listed in `AGENTS.md`) ships only if
the user states it. Ask about each one. When nobody can answer, use the neutral text and end your summary with
one line of flag names, for example `Removed promises: LICENSED, INSURED`.
