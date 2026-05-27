# TrustOS — trustos.missionctrl.agency

The measurement intelligence layer of the Brand Effect — MissionCTRL's methodology for turning purpose-led brands into movements.

A MissionCTRL product. © 2026 MissionCTRL Ltd.

---

## Site structure

```
.
├── index.html                          # Main landing page
├── results.html                        # Demo-form submission result page
├── netlify.toml                        # Netlify build config (publish from root)
│
├── insights/
│   └── index.html                      # Sector Insights hub — lists all POVs
│
├── energy-integrity-test/
│   ├── index.html                      # Energy sector POV — "When the Chair Falls"
│   ├── banner.png                      # Hero banner (1280×720, on-brand)
│   └── banner@2x.png                   # Retina banner (2560×1440)
│
└── mining-trust-window/
    ├── index.html                      # Mining sector POV — "Mining's Trust Window 2026–2030"
    ├── banner.png                      # Hero banner (1280×720, on-brand)
    └── banner@2x.png                   # Retina banner (2560×1440)
```

## What's new in this revision (May 2026)

### 1. New Energy sector POV
- Article: `/energy-integrity-test/index.html`
- Headline: *When the chair falls. Energy's Integrity test.*
- Trust diagnostic scores: Clarity 74, Connection 55, Confidence 54, Composite 61
- Anchored on the 26 May 2026 BP chair firing event
- Cites Brandpie's *Clarity through Complexity* energy report alongside Bloomberg, FT, McKinsey and IEA

### 2. Mining POV redesigned
- Article: `/mining-trust-window/index.html` (replaces previous version)
- Same design language as the new Energy POV — hero banner image, lede, diagnostic strip, pullquotes, related-POV card, sources
- Same trust diagnostic scores (Clarity 81, Connection 58, Confidence 62, Composite 65)
- All substantive content preserved from the previous version, presentation refreshed

### 3. Sector Insights hub
- New page: `/insights/index.html`
- Lists both Mining and Energy POVs with banner thumbnails, scores chips, and read-time meta
- Coming-soon strip flags Local Government, Healthcare, Higher Education, Financial Services, Social Housing

### 4. Main page updates
- `index.html` Sector Insights section now shows both POVs in a 2-column responsive grid (auto-fit, min 320px)
- Each card has a banner image at the top + scores chips + metadata
- "Browse all Sector POVs →" link added at the bottom of the section, pointing to `/insights/`

## Brand identity (canonical)

| Token            | Value          | Use                            |
|------------------|----------------|--------------------------------|
| `--deep`         | `#0a0f1a`      | Primary background             |
| `--trust-slate`  | `#2d3a4a`      | Secondary background / CTA     |
| `--trust-cool`   | `#5a8a9a`      | Primary accent / Clarity color |
| `--trust-ice`    | `#6da0b8`      | Gradient highlight             |
| `--trust-mid`    | `#8fb5c0`      | Light teal accent              |
| Clarity          | `#5a8a9a`      | Driver 1 (Intent↔Expectation)  |
| Connection       | `#7cc4a8`      | Driver 2 (Expectation↔Reality) |
| Confidence       | `#a78bdb`      | Driver 3 (Intent↔Reality)      |

Typography: **Sora** (weights 200, 300, 400, 500, 600, 700, 800), loaded from Google Fonts.

## Deploy

Netlify is configured to publish from the repo root (`publish = "."`).

Local preview:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

GitHub upload:

1. Initialise a git repo at the root of this folder (or push into your existing TrustOS repo).
2. The Netlify build picks up `netlify.toml` automatically.
3. No build step required — pure static HTML.

## Adding the next sector POV

When the next sector POV is ready:

1. Create a folder at the root, named for the POV slug (e.g. `/local-government-trust-test/`).
2. Copy `/energy-integrity-test/index.html` as the template.
3. Replace title, hero, lede, body, diagnostic scores, sources.
4. Drop the new banner.png + banner@2x.png into the same folder.
5. Add a new card on `/insights/index.html` (mirror the existing card markup, point at the new folder).
6. Add a new card on the main `index.html` Sector Insights grid (the grid auto-fits, no layout changes needed).
7. Update the "Related Sector POVs" card on each of the other sector POVs to cross-link.
8. Move the new sector from the "coming-soon" list on `/insights/index.html` into a published card.

## Methodology

The TrustOS methodology runs Intent / Expectation / Reality, plus the three trust enablers (Clarity / Connection / Confidence) on a foundation of Integrity. See the main `index.html` "How it works" and "What it measures" sections for the canonical model.

---

For questions: hello@missionctrl.agency
