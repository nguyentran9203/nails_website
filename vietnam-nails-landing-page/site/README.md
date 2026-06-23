# Vietnam Nails — production landing page

A real, deployable build of the `Vietnam Nails.dc.html` design handoff
(`../project/`). Single self-contained `index.html` (inline CSS/JS) + `images/`.
No build step — open `index.html` or serve the folder statically
(e.g. GitHub Pages, Netlify, `python3 -m http.server`).

## What's here
- **All sections** from the design: header, hero, gallery strip, styles,
  story, services & pricing, reviews, booking CTA, visit, Instagram feed, footer.
- **Trilingual** (EN / ES / CA) with a working language switcher. Choice is
  remembered (`localStorage`) and falls back to the browser language.
- **Components added** beyond the static prototype:
  - Instagram feed strip — image tiles that link to the profile with a hover overlay.
  - Embedded map of the studio (OpenStreetMap iframe) in the *Visit* section.
  - Mobile hamburger nav, scroll-reveal animations, click-to-call button.

## Images
Every image slot is filled with the salon's own photos, extracted from the
design bundle's saved state (`../project/.image-slots.state.json`) — these are
the photos that were dropped into the mockup, several straight from the
salon's feed (one still carries the "VIETNAMNAILS · SALON DE UÑAS" watermark).
Files live in `images/`.

### Note on live Instagram images
The page links to **@vietnamnails_sabadell** throughout, and the Instagram feed
uses the salon's real photos. Pulling *live/latest* posts automatically was not
possible here: instagram.com returns HTTP 403 to any non-logged-in request, so
the feed can't be scraped without authentication. To make the feed
auto-update, use one of:
- the official **Instagram Basic Display / Graph API** (requires a Meta app + token), or
- a hosted widget (EmbedSocial, Elfsight, LightWidget, etc.).
Until then, swap tiles by dropping new images in `images/` and updating the
`<section class="igsec">` block.

## Studio details (from the salon's business card in the photos)
- Av. de la Concòrdia, 5 — 08201 Sabadell · Barcelona
- Mon–Sat 9:30–21:00 · walk-ins welcome (sense cita prèvia)
- Tel. 632 672 273 · [@vietnamnails_sabadell](https://www.instagram.com/vietnamnails_sabadell/)
