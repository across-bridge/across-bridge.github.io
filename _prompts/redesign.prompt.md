# Codex task: LIGHT premium redesign of the Across Bridge landing page (style of Across Protocol)

Rebuild this static one-page site IN PLACE (your -C workdir): overwrite `index.html` + `style.css`, keep
every other file. No frameworks, no build, no external JS/libraries; tiny inline JS only. Premium and
polished -- NOT dry, NOT minimal, NOT oversized.

IMAGES ARE FROZEN: never create, overwrite, download, replace, rename, or delete any image
(`favicon.png`, any `*.png`/`*.svg`/`*.ico`, `og-cover.png`). Use ONLY the images already in the folder,
byte-unchanged. Keep `<link rel="icon">` and the topbar brand `<img>` on the existing `favicon.png` (no
inline `<svg>`, no data-URI). Need an icon you do not have? Use a styled text chip.

PRESERVE from the current `index.html` (read it first): the exact keyword `Across Bridge` (as `<h1>` and in
`<title>`), the existing value sentence (deck `<p>` = `<meta description>`, word-for-word, light polish
only), the `<link rel=canonical>`, the money CTA target href, AND the existing authority reference links in
the topbar (Etherscan, Ethereum bridges, L2BEAT) -- keep all three, never drop them.

## THEME: LIGHT premium, in the real style of Across Protocol (across.to)
- This keyword is the Across cross-chain bridge. Render it in the spirit of Across's REAL light brand: a
  clean LIGHT base, ONE confident accent derived from `favicon.png` + your knowledge of Across, soft WHITE
  cards with GENEROUS rounded corners (~16-22px radius), gentle soft shadows, hairline neutral borders,
  airy whitespace. If unsure of the exact Across palette, use a fresh, friendly LIGHT premium scheme. ONE
  accent only, neutral borders, no rainbow.
- `<meta name="theme-color">` = the light base background.
- Quiet premium motion only (soft pulse on the Preview dot, gentle hover lift on the CTA). Respect
  `prefers-reduced-motion`.

## Layout (desktop ONE screen, mobile CLEAN short scroll)
Inside `<main>`: a split hero, then a thin bottom texture band, then the footer.
- **Topbar:** brand mark (`favicon.png`) + `Across Bridge` wordmark LEFT; flexible spacer; the AUTHORITY
  NAV right (Etherscan / Ethereum bridges / L2BEAT, plain text,
  `target="_blank" rel="nofollow noopener noreferrer"`) -- MUST stay present and in source HTML. No topbar button.
- **Left column (basic):** `<h1>Across Bridge</h1>` (refined hero ~78-84px, NOT a giant 120px+) -> the deck
  `<p>` value sentence (keyword in `<strong>`) -> EXACTLY THREE qualitative trust chips (e.g.
  `Cross-chain bridging`, `Fast settlement`, `Non-custodial`) -> ONE prominent, comfortably large primary
  CTA `Enter App`. NO `<h2>` -- hero copy is only the H1 and its deck `<p>`.
- **Right column (the star -- a RICH bridge preview, light soft card):** light chrome with a small selector
  pill + a pulsing `Preview` pill; a From-chain -> To-chain route using the REAL token/chain icons present
  in the folder, in two rounded panels with a SMALL GAP so the circular switch sits in a clean notch on the
  seam; the switch swaps the two; an abstract `Best route` micro-row (faint hop dots, NEVER fabricated
  numbers); a faint number-free hint (e.g. `Live quote in app`); and the `Start Bridge` CTA at the bottom.
  Non-interactive preview: only the switch toggles icons. No wallet connect, no fake amounts/quote.
- ONE tasteful bottom texture band (a light decorative strip or subtle pattern) -- brand-true, number-free,
  restrained; no invented filler phrases, no clutter.

## SEO spine (LOCKED)
- `<title>` = `Across Bridge &mdash; <short hook>` (em-dash entity, keyword first, <=60 chars, no weak suffix).
- Exactly one `<h1>` = `Across Bridge`. NO `<h2>` anywhere.
- Deck `<p>` wraps `<strong>Across Bridge</strong>` and equals `<meta description>` word-for-word.
- Schema `@graph` = WebSite + WebApplication + Organization, truthful, no FAQ/HowTo. SEO text in source HTML.

## Claims (light, crypto-friendly)
- Confident, premium marketing copy is welcome. Two floors only: (1) invent NO specific numbers (stats,
  TVL, fees, dates, audits, partnerships) -- qualitative only; (2) no "guaranteed / risk-free / 100%" and
  no fake wallet-connect / deposit flow.
- One small footer line: `Information on this page is for educational purposes only and is not financial advice.`

## CTAs + footer
- Exactly TWO, distinct, both -> the preserved target href, `rel="noopener noreferrer"`: hero `Enter App` +
  card `Start Bridge`. No third CTA, no topbar button.
- Footer: a `Across Bridge &mdash; 2026` brand line + the one educational line. Small and quiet.

## Technical / mobile
- SEO content in SOURCE HTML; tiny INLINE `<script>` for the switch only; every `<img>` has width+height.
- Desktop ONE screen: `body{min-height:100vh;min-height:100dvh}` + desktop media
  `{height:100vh;height:100dvh;overflow:hidden}` (vh BEFORE dvh); add a `max-height` desktop query to
  compress on short screens.
- MOBILE MUST BE CLEAN: single column; the bridge card full-width; the route stacks neatly (switch rotates
  vertical between the stacked panels); comfortable spacing and large tap targets; topbar collapses tidily
  (brand left; authority nav may hide visually but STAYS in source); short vertical scroll; ABSOLUTELY no
  horizontal overflow (`overflow-x:hidden` on html/body + `overflow:hidden` on the band).
- Keep `lang="en"`; keep favicon/og/manifest/robots/sitemap referenced. Glyphs via HTML entities
  (`&mdash;`, `&rsaquo;`, `&darr;`), not literal non-ASCII.

## Self-QC
- [ ] LIGHT premium, Across spirit; ONE accent; soft rounded cards; NOT dry/minimal.
- [ ] Authority links (Etherscan / Ethereum bridges / L2BEAT) present in topbar + source HTML.
- [ ] One `<h1>` = `Across Bridge`; NO `<h2>`; deck `<p>` == meta description; H1 ~80px not oversized.
- [ ] Split hero; desktop one screen no-scroll; MOBILE clean, no horizontal overflow.
- [ ] Rich number-free From->To bridge preview; real icons; switch in a clean notch.
- [ ] Exactly TWO CTAs (`Enter App` + `Start Bridge`) -> target; no topbar button.
- [ ] IMAGES byte-untouched; favicon still the icon + brand mark; footer brand line + one educational line.

Make it genuinely premium and Across-light. Then stop.
