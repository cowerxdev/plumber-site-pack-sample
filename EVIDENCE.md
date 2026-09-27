# EVIDENCE: Plumber Site Pack

Each design choice in this pack, and why we made it. A **measured** choice cites how common the feature is
among Ohio plumber homepages we rendered in a real browser and checked. That is prevalence, not proof that the
feature brings more calls. A **reasoned** choice is our judgment and is labelled that way.

Source: Rendered homepages in all nine Ohio study counties and a rendered sample of Ohio homepages per trade, checksum-verified (cowerx ohio_identity). Evidence generated 2026-09-27.

## Measured choices

### C1. A tap-to-call link in the header and hero

- **Tap-to-call link:** 74% of 377 plumber homepages in nine Ohio counties had a tap-to-call link (95% range 69% to 78%), checked in rendered Chromium on 2026-09-25.
  - 279 of 377 sites; 95% range 69% to 78%; rendered Chromium, 2026-09-25; claim `tap_to_call.ohio9`
  - Manifest SHA-256: `18ed0bb4584ff83b4b16d2f9d98d7c091e200d5d7f388a59c60a840286352738`, `f354a8862a9d4d15ef14227a2d0cf40d19644a5006c0133bcfb27d9d8f678c1c`, `286d221dfc81e0e9919a1f8c9144cf4244a8fe9382ebdb0b773daf98f3f17372`, `c51a1d90ee0beedbfe933a7a0e348516ceb2d9a267c5db9804539962f393bd00`, `915b222ebe100a50368ec9970b41777d68dfac117300e51055150cc49657832e`, `7a8955f7e0283d406ba839f8098a834f3a7d7b276d9dc97cb71a2f91afeb9bfd`, `c8ff58c50c37ea2c0289c8fa30e021312e983250f46861bb13e70c0ae0ccc654`, `0d692019d5ecc264bab7ecbb3d9957a8cab300e34d1d29d5d5c9318bcf40acd4`, `a15351b2c61aa7c3a6f5ee75c6a0f2e77737d23a389ba5afd246873d8ce25282`
  - Our reading: table stakes (most sites here have it). This is our reasoning, not a measured result.
- Where it's used: `components/01-header.html`, `components/02-hero.html`

### C2. The phone number written out as text wherever there is a call button, not just a 'Call' label

- **Visible phone number:** 87% of 377 plumber homepages in nine Ohio counties had a visible phone number (95% range 83% to 90%), checked in rendered Chromium on 2026-09-25.
  - 328 of 377 sites; 95% range 83% to 90%; rendered Chromium, 2026-09-25; claim `visible_phone.ohio9`
  - Manifest SHA-256: `18ed0bb4584ff83b4b16d2f9d98d7c091e200d5d7f388a59c60a840286352738`, `f354a8862a9d4d15ef14227a2d0cf40d19644a5006c0133bcfb27d9d8f678c1c`, `286d221dfc81e0e9919a1f8c9144cf4244a8fe9382ebdb0b773daf98f3f17372`, `c51a1d90ee0beedbfe933a7a0e348516ceb2d9a267c5db9804539962f393bd00`, `915b222ebe100a50368ec9970b41777d68dfac117300e51055150cc49657832e`, `7a8955f7e0283d406ba839f8098a834f3a7d7b276d9dc97cb71a2f91afeb9bfd`, `c8ff58c50c37ea2c0289c8fa30e021312e983250f46861bb13e70c0ae0ccc654`, `0d692019d5ecc264bab7ecbb3d9957a8cab300e34d1d29d5d5c9318bcf40acd4`, `a15351b2c61aa7c3a6f5ee75c6a0f2e77737d23a389ba5afd246873d8ce25282`
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
