# Dynamic Asset Groups — OP Prototype

Interactive prototype for the **Dynamic Asset Groups** initiative in Rokt One Platform.

## Background

> Rokt's 1:1 creative-to-format architecture has become a scale wall. Dynamic Asset Groups introduce a component-based creative model — one object groups all advertiser-provided assets (headlines, images, CTAs) and Rokt Brain assembles and optimises combinations across formats at the impression level.

📄 **[Read the full strategy doc →](https://docs.google.com/document/d/1auMEDsDX6My-1OVxfXKWDBHZ29EyZLpsD9E_OchwE1s/edit)**

## Prototype

| File | Description |
|------|-------------|
| [`asset-groups-op-platform.html`](asset-groups-op-platform.html) | Full OP shell prototype — open locally in any browser |

> **To run:** clone the repo and open `asset-groups-op-platform.html` directly in your browser. No build step needed.

## Key features shown

### Campaign structure
- **Campaign list** — table with status, metrics (Spend, Impressions, Referrals, Acquisitions, CoPI), sparkline trends
- **Campaign detail** — header with date range + status badge, metric strip, trend chart (current vs previous period), budget utilisation bar, schedule card; tabs for Overview / Ad Sets / Creatives / Offers

### Creative type choice
- **Dynamic vs Manual** — Ad Set-level choice with clear explanation of trade-offs (scale + Brain optimisation vs strict brand control)
- **New vs Refine modal** — when editing an existing Asset Group, prompts whether you're refining the same strategy (preserves learning track) or starting a new one (clean track)

### Asset Group editor
- **Required assets** — Titles (multi-variant with Best/Good/Low/Pending performance pills), Short description (≤50 chars), Long description (≤175 chars), CTAs, Brand name, Destination URL, Negative CTA, Disclaimer
- **Format expanders** — Benefits (chips, unlocks Benefits + Benefits Hero), Promotion (unlocks Savings), Callout tags
- **Visual assets** — ratio tabs for Product Landscape (1.91:1), Product Square (1:1), Product Portrait (4:5), Brand Logo (1:1 + 1.91:1 slots), and Carousel (2–10 images, unlocks Product Carousel format); each tab has drag-drop upload, thumbnail grid with performance pills, and Asset Library side-panel picker
- **Offer & distribution** — linked offer, coupon, nurture sequence with View → link, CCE toggle, impression cap toggle
- **Format Eligibility panel** — live sidebar showing which of 7 formats are eligible based on current assets
- **Network Reach meter** — % of inventory covered + target guidance
- **Combinations counter** — live formula (T × D × CTA × Img) showing Brain's optimisation surface
- **Preview by format** — 6 format tabs (Text, Text Hero, Benefits, Benefits Hero, Savings, Compact) with accurate CSS-rendered ad mockups; cycle through all combinations
- **Asset Strength card** — Good/Excellent scoring with per-component checklist
- **AI Suggest (Rokt Brain)** — one-click fill of all fields with AI-generated copy + assets

### Manual creative editor
- Format selector (Text, Benefits, Savings, Text Hero, Compact)
- Copy fields (Title, Body, Benefits/Promo, CTA, Destination URL)
- Image upload with **Required to render** toggle (creative won't serve if image missing/rejected)
- Live preview panel + format eligibility warning with "Switch to Asset Group" prompt

### Asset Groups list & reporting
- **AG list** — table with Strength badge, formats eligible count, combinations, CVR, Acquisitions
- **AG reporting** — stat strip (CVR, Acquisitions, Impressions, Combinations, Strength); three tabs:
  - **Asset Intelligence** — per-asset CVR table (Titles, Short/Long Desc, CTAs, Images) with impressions, CVR vs avg delta, acquisitions
  - **Format Performance** — per-format cards (impressions, CVR, share of serve) including ineligible format with unlock CTA
  - **Combination Insights** — top combinations ranked by CVR
- **Rokt Brain recommendations** — 4 priority-ranked actions (High/Medium) with estimated lift and one-click apply

### Experimentation
- Experiment list with status and type badges
- Setup flow with three experiment types: **AG vs Manual**, **AG vs AG**, **Format Holdout**

### Resources & other views
- **Asset Library** — slide-in right drawer with ratio tabs and multi-select, opens from any image upload zone
- **Custom Audiences**, **Coupons**, **Nurture**, **Insights** — stub views wired to sidebar navigation

---

## Archive

Older prototype iterations are in [`/archive`](archive/):
- `asset-groups-prototype.html` — original single-page proof of concept
- `asset-groups-full-flow.html` — intermediate multi-page flow

These are kept for reference only. All active development is on `asset-groups-op-platform.html`.
