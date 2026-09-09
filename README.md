# Lavenderbuddy®

A redesign of [lavenderbuddy.co.uk](https://www.lavenderbuddy.co.uk) plus **Buddy's Den**, a digital
companion web app for the Lavenderbuddy sensory bear.

Lavenderbuddy® is a sensory support tool shaped like a best friend — it helps children soothe big
feelings through scent (real lavender flowers), touch (tactile sensory fabric), breath (five stitched
circles down the bear's tummy) and connection (a social story and affirmation cards).

## What's here

| File | What it is |
| --- | --- |
| [`index.html`](index.html) | The website — hero, how it works, the science, a six-step getting-started guide, shop, reviews, our story, and the newsletter sign-up |
| [`buddys-den.html`](buddys-den.html) | Buddy's Den — the companion web app |

Both are single self-contained HTML files. No build step, no dependencies, no tracking. Open either
one directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Buddy's Den

The app practises the same skills as the physical bear, so the two reinforce each other.

- **Name your bear** — on first visit the child names their Buddy, and the app uses that name throughout
- **Breathe with Buddy** — a guided *physiological sigh* (two sniffs in, one long blow out) where the
  five tummy circles glow in sequence while the bear inflates and settles; 3, 4 or 5 rounds by age
- **Feelings weather** — sunny / breezy / cloudy / rainy / stormy check-in, with an empathetic reply
  from Buddy and a quiet week-of-weather strip for grown-ups to glance at
- **Affirmation cards** — flip cards drawn from Buddy's tummy pocket
- **Goodnight den** — tuck Buddy in under the moon, with optional gentle rain synthesised on-device
  with the Web Audio API (nothing plays until it's switched on)
- **Paw prints** — earned for each completed breathing session
- **For grown-ups** — a parent corner covering the science of the sigh, the vagus nerve ("Gus"), and
  how to introduce the real bear

### Privacy

Everything the app remembers — the bear's name, paw prints, weather check-ins — is stored in the
browser's `localStorage` on that device. There is no account, no server, no analytics, and nothing is
uploaded anywhere.

### Accessibility

- Full keyboard navigation with visible focus states
- ARIA live regions announce breathing cues and Buddy's replies
- Honours `prefers-reduced-motion` (animations off, breathing exercise still usable)
- Colours meet contrast requirements against the den's dark ground

## Design notes

The site uses a warm storybook serif over a humanist sans, on a lavender / sage / honey palette with a
full dark mode. Buddy, the mother-and-cub story illustration, and every product icon are hand-authored
SVG — no stock imagery, no external fonts, no CDN requests. The hero bear breathes on a 5.6-second
cycle and blinks; the "try it now" widget on the site runs the same physiological sigh the bear teaches.

---

© Lavenderbuddy®. Made in the UK.
