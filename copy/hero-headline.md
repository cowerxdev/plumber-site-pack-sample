---
pattern: hero-headline
evidence: tap_to_call.ohio_sample visible_phone.ohio_sample
reasoning: r.emergency
used_in: 02-hero
---
# Hero headline and lead

**Shape:** `[The situation, in the visitor's words]? [Who answers] [when].` Then one lead line that removes the two
fears: that no one will answer, and that the bill will be a surprise.

**Fill-ins**
- Situation: `Water where it shouldn't be?` · `No hot water?` · `Drain backing up?`
- Who and when: `Call a plumber now.` (neutral) · `Talk to a licensed plumber now.` (only if LICENSED is stated)
- Lead: neutral `Leaks, clogs, drains and water heaters in [CITY] and nearby.` · or, only if stated,
  `A person answers day and night.` (OPEN_24_7) and `You get the price before any work starts.` (PRICE_FIRST)

**Variants**
1. Neutral, which promises nothing: *Water where it shouldn't be? Call a plumber now.*
2. Licensed and 24/7, both stated by the client: *Water where it shouldn't be? Talk to a licensed plumber now.*
3. Office hours, stated by the client: *Plumbing problem? Call a plumber today.* Lead: *Calls answered [HOURS].*
4. Drain-first client: *Drain backing up? Call to get it cleared.*

**Rules**
- A promise (licensed, insured, 24/7, price first, a callback time, a guarantee) goes in only if the user stated it
  for this client. See "Promises" in `AGENTS.md`. With nothing stated, use variant 1.
- Keep it under 12 words, so it fits on three lines at 375px.
- The call button under it always shows the number.

**Why:** 67% of 30 sampled Ohio plumber homepages had a tap-to-call link when checked in rendered Chromium (2026-09-25). That makes tap-to-call likely table stakes (most sampled sites have it, though the range dips below half) for
plumber sites here. The headline's only job is to send people to that button.
