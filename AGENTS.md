# AGENTS.md: Free plumber sample

You are building a local plumber homepage with this sample. Read `EVIDENCE.md` before changing the design. Use the included pieces as the opening of the homepage and ask the client for the rest of the page's real content.

## Included pieces

- `tokens/tokens.css`, `tokens/tokens.json`, and the Inter fonts in `tokens/fonts/` set colors, type, spacing and sizes.
- `components/01-header.html` and `components/02-hero.html` provide the header and call button hero. `components/pack.css` styles them; it is the full shared stylesheet.
- `copy/hero-headline.md` explains how to adapt the headline and lead.
- `preview.html` shows these two components with fictional details.
- `EVIDENCE.md` records the measurements and reasoning cited by these pieces.

## Build the opening in this order

1. `components/01-header.html` (tap_to_call.ohio_sample, visible_phone.ohio_sample)
2. `components/02-hero.html` (tap_to_call.ohio_sample, visible_phone.ohio_sample)

Link `tokens/tokens.css` first, then `components/pack.css`. Keep the `pk-` class names. If the target stack is React, Astro, Next or another framework, keep the component markup and classes when adapting it.

## Non-negotiables

1. Show a tap-to-call link (`href="tel:+1..."`) without scrolling on a 375px-wide phone, in both header and hero.
2. Every call button shows the phone number as text (`Call (614) 555-0142`), except the compact header button on phones, where the hero button shows it.
3. Use `--pk-color-call` only for tap-to-call links.
4. Serve the finished page over HTTPS and include `<meta name="viewport" content="width=device-width, initial-scale=1">`.
5. Keep tap targets at least `--pk-tap-min` (48px) tall.

## Fill the slots

Ask the client for each real value. Never invent one.

| Slot | What to ask for |
|---|---|
| `[[BUSINESS_NAME]]` | Trading name, exactly as on the Google Business Profile |
| `[[PHONE_DISPLAY]]` | The number as people read it, e.g. (614) 555-0142 |
| `[[PHONE_TEL]]` | The same number in E.164 for tel: links, e.g. +16145550142 |
| `[[CITY]]` | Home city |

Replace every `[[SLOT]]` marker. Remove an element if the client cannot provide a true value for it.

## Promises: they ship only if the user states them
Every promise in the components sits in a block:
`[[IF_FLAG]]promise text[[ELSE]]neutral text[[/IF]]` (the `[[ELSE]]` part is optional, and `[[IF_A|B]]` means A or B).
Blocks can nest; resolve the inner ones the same way.

- Keep a block's promise text ONLY if the user's brief or one of their answers states that promise for this
  client. "Emergency plumber" does not mean 24/7, and "professional" does not mean licensed.
- Otherwise keep the `[[ELSE]]` text, or delete the block if there is none. The neutral text promises nothing.
- Interactive session: ask the user about each promise that's still unresolved, using the questions below.
- Non-interactive run (no one to ask): use the neutral text for every promise the brief doesn't state, and
  list the ones you removed on ONE line of your final summary, using the flag names from the table below,
  exactly like `Removed promises: LICENSED, INSURED, OPEN_24_7`. The owner then knows what to add back.
- Remove every `[[IF_...]]`, `[[ELSE]]` and `[[/IF]]` marker from the finished page.
- The shut-off steps in the hero's "Water leaking right now?" panel are safety advice, not a promise. Keep them,
  and tell the user the client should agree with them.

| Flag | What it promises | Ask the user |
|---|---|---|
| `LICENSED` | "licensed plumber", the License cell and the footer license line | Is the business licensed? Give the exact issuer and number. |
| `INSURED` | "Insured" and the insurance line | Is the business insured? What can they show? |
| `OPEN_24_7` | "24/7", "a person answers day and night", "call any time", "on-call" | Does a person really answer the phone around the clock? |
| `PRICE_FIRST` | "price before any work starts", "no surprise bill" | Do they always give a price before starting work? |
| `CALLBACK_TIME` | "call back in about N minutes" | How fast do they really call back a web request? |
| `GUARANTEE` | the written guarantee in step 3 | Do they give a written guarantee? What exactly does it say? |
| `YEARS` | "N years in CITY" | How many years have they worked locally? |
| `HOURS` | the office hours line in the footer | What are the office hours? |
| `BOOKING` | the "Book online" link | Do they have an online booking tool? What is its link? |
| `COUNTY` | "On the road across COUNTY County" | Which county do they cover? |
| `FORM_HANDLER` | the request-a-callback form (it must reach a phone the client watches) | Where should web requests go? Give the form handler or CRM endpoint. |
| `TEXTS` | the "Text a photo" link (the number must take text messages) | Can the business number receive text messages? |
| `OWNER_FACT` | an owner fact from the brief in the trust strip, e.g. "Family-owned" | Is there one short fact about the owners they want shown (family-owned, veteran-owned)? |

## Use the evidence carefully

`EVIDENCE.md` measures how common a feature was among rendered Ohio plumber sites. It does not prove a feature causes more calls. Quote its sentences exactly if asked why a choice was made. The measurements date to 2026-09-25 (A rendered sample of Ohio homepages per trade, checksum-verified (cowerx ohio_identity)).

## Done means

On a 375px viewport, the first screen shows the business name, headline and a call button with the number. No `[[SLOT]]` or `[[IF_...]]`/`[[ELSE]]`/`[[/IF]]` markers remain. The page passes an HTML validator, and every `tel:` link dials the number displayed.
