# Portfolio — Alessandro Demichelis

## Purpose
Career fair portfolio page. Single file (index.html).
Hosted on GitHub Pages at https://alessandro25-art.github.io

## File structure
```
Portfolio/
├── index.html               — main portfolio page (self-contained HTML/CSS/JS)
├── CV/
│   └── CV_Alessandro_Demichelis_26.pdf
├── Lavori/
│   ├── ILLY_Social_Impact_Assessment.pdf
│   ├── EY_Rigoni_ESG_Strategy.pdf
│   ├── Ferri_Sustainable_Operations.pdf
│   └── Exon_Circular_Business_Model.pdf   (converted from .docx via docx2pdf)
└── scripts/ralph/           — Ralph autonomous agent loop
```

## Deploy
Git repo: https://github.com/alessandro25-art/alessandro25-art.github.io
Push command: `git add -A && git commit -m "..." && git push`
GitHub Pages auto-deploys from main branch root. Live in ~2 min.

## Design reference
Minimal, editorial, typographic. No templates, no gradients.
White background (#FAFAFA), Playfair Display 700 for H1, DM Sans 300/400/500 for everything else.
Max-width 720px, padding 24px, generous whitespace between sections.

## Writing style
All copy must use the Humanizer skill (/humanizer).
Alessandro's voice: direct, honest, concise. No AI puffery, no significance inflation.
Do NOT use: "passionate about", "driven professional", "merit scholarship recipient",
"significant contribution", "pivotal", "testament", or any AI vocabulary words.

## Layout
- Hero: two-column flex (hero-left: name/title/bio/meta+LinkedIn, hero-right: CV label/note/download)
  - section-hero: align-items: stretch so hero-right matches hero-left height
  - hero-right: justify-content: center to vertically center CV block
  - Mobile (<600px): flex-direction: column
- Selected Work: 4 static cards in a scrollable flex row (work-carousel)
  - No auto-scroll, no clones — just overflow-x: auto, manual swipe
  - Cards: flex: 0 0 616px (desktop), flex: 0 0 75vw (mobile)
  - Click on card image or "Read more" expands card detail
  - Click snaps card to center of carousel via scrollTo
- Skills: flex-wrap badges with inline detail panel, wave animation on click
- QR: points to https://alessandro25-art.github.io, label shows "AlessandroPortfolio.com"
- Footer: "Alessandro Demichelis · 2026"
- Easter egg: small text below footer "Thank you for scrolling all the way here!"

## Sections order
Nav → Hero (name + CV) → Selected Work → Skills → QR → Footer

## Cards (Selected Work)
1. ILLY, Social Impact Assessment — coffee communities, SDGs 4/8/10
2. EY × Rigoni di Asiago, ESG Strategy — disability hiring + waste-to-energy
3. Ferri S.R.L, Sustainable Operations — Italian SME, Northern Europe expansion
4. Exon, Circular Business Model Design — printer ecosystem, 5 business model patterns

Each card: thumb image (Pexels), tags, title, short description, "Read more" toggle, PDF link.
PDF links use `download` attribute with clean filename matching the work title.

## Ralph loop
Usage: `CLAUDE_PATH="/c/Users/aless/AppData/Local/Packages/Claude_pzs8sxrjxfjjc/LocalCache/Roaming/Claude/claude-code/2.1.78" PATH="$CLAUDE_PATH:$PATH" bash scripts/ralph/ralph.sh --tool claude`
Write user stories to scripts/ralph/prd.json with `passes: false`, Ralph fixes them autonomously.

## QR code
Generated client-side via qrcode.js CDN. Script must NOT be inside DOMContentLoaded wrapper
(fires after body parse, event already fired — call new QRCode() directly).

## Known decisions
- overflow-x: hidden on html, body prevents carousel from causing horizontal scrollbar
- scroll-snap removed from carousel (was causing cards to stop at last snap point)
- Exon .docx converted to PDF with: `python -m docx2pdf` (already installed)
- LinkedIn URL: https://www.linkedin.com/in/alessandro-demichelis-18b17a238
