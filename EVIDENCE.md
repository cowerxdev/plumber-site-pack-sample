# EVIDENCE: Plumber Site Pack

Each design choice in this pack, and why we made it. A **measured** choice cites how common the feature is
among Ohio plumber homepages we rendered in a real browser and checked. That is prevalence, not proof that the
feature brings more calls. A **reasoned** choice is our judgment and is labelled that way.

Source: A rendered sample of Ohio homepages per trade, checksum-verified (cowerx ohio_identity). Evidence generated 2026-09-27.

## Measured choices

### C1. A tap-to-call link in the header and hero

- **Tap-to-call link:** 67% of 30 sampled Ohio plumber homepages had a tap-to-call link when checked in rendered Chromium (2026-09-25).
  - 20 of 30 sites; 95% range 49% to 81%; rendered Chromium, 2026-09-25; claim `tap_to_call.ohio_sample`
  - Manifest SHA-256: `c766ba0a315fd1f42f00dae8ea0d1580e098f61c871a451125166a9b56356500`
  - Our reading: likely table stakes (most sampled sites have it, though the range dips below half). This is our reasoning, not a measured result.
- Where it's used: `components/01-header.html`, `components/02-hero.html`

### C2. The phone number written out as text wherever there is a call button, not just a 'Call' label

- **Visible phone number:** 80% of 30 sampled Ohio plumber homepages had a visible phone number when checked in rendered Chromium (2026-09-25).
  - 24 of 30 sites; 95% range 63% to 90%; rendered Chromium, 2026-09-25; claim `visible_phone.ohio_sample`
  - Manifest SHA-256: `c766ba0a315fd1f42f00dae8ea0d1580e098f61c871a451125166a9b56356500`
  - Our reading: table stakes (most sites here have it). This is our reasoning, not a measured result.
- Where it's used: `components/01-header.html`, `components/02-hero.html`

## Reasoned choices (our judgment, not measured)

- **r.one-action**: A site for an emergency trade has one job: to get a call. So the call color is used for tap-to-call and nothing else, which keeps the one action easy to find. Used in: `01-header`, `02-hero`.
- **r.emergency**: People search for a plumber when water is somewhere it shouldn't be. So the headline names the situation, and, only when the client really offers it, the first promise is that a person will answer. Used in: `02-hero`.
- **r.while-you-wait**: Someone with water on the floor needs the next thirty seconds of help before they need a sales pitch. The shut-off steps are useful on their own, and they end at the call button. Used in: `02-hero`.

## How to use these numbers

- Quote a sentence above exactly as written. Don't round it, and don't turn "X% of sites have it" into "X% more calls".
- "Table stakes" and "differentiator" are our reading of how common a feature is. They are not measurements.
- Where a range is wide (a small sample), say so, or quote the count ("20 of 30") instead of the percentage.
