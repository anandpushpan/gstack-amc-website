# v1.4 New Sections Summary

## Four New Showcase Sections Added

### 1. "What's inside every report" (DEEP-DIVE COMPARISON)
**Position:** After the main moat/valuation card section  
**Purpose:** Show users exactly what separates AnalyzeMyCar from competitors  
**Visual:** Side-by-side layouts with real screenshots

- **Left side:** Text comparison of what competitors offer
  - Generic MOT history only
  - No condition assessment
  - Generic valuation (ignores repairs)
  - No OEM spec detail
  
- **Right side:** Real screenshot showing AnalyzeMyCar vehicle overview with Grade A-C

- **Second comparison:** AI assessment
  - Shows real feat-ai.jpg screenshot with itemized repairs
  - Explains how AI scans photos and prices repairs
  - Three value signals: automated, itemized, real costs

**Layout:** Alternating grid (text left, image right | image left, text right)  
**Mobile:** Stacks vertically  

---

### 2. "Factory data others can't access" (OEM ADVANTAGE)
**Position:** Before the "For Dealers" section  
**Purpose:** Build trust by highlighting OEM data access  

- **Service book deep-dive**
  - Real screenshot: feat-dsb.jpg showing OEM service records
  - Explains why main dealer records are trustworthy
  - Three benefits: OEM only, timeline view, trust signal
  
- **Build sheet detail**
  - Real screenshot: feat-buildsheet.jpg with factory equipment
  - Explains insurance group, emissions, spec verification
  - Three benefits: confirm insurance, check emissions, verify spec

**Layout:** Two alternating grids (image right, image left)  
**Mobile:** Stacks vertically  

---

### 3. "From history to numbers" (MOT + VALUATION)
**Position:** Before pricing section  
**Purpose:** Show how historical data becomes actionable insights

- **MOT history with clocking detection**
  - Real screenshot: feat-mot.jpg with mileage trend chart
  - Explains why mileage spikes matter
  - Three benefits: full test log, clocking flags, repair patterns
  
- **Valuation trends**
  - Real screenshot: report-trend.jpg showing market projections
  - Explains three-grade pricing model
  - Three benefits: three grades shown, live market data, future projections

**Layout:** Two alternating grids (image left, image right)  
**Mobile:** Stacks vertically  

---

### 4. "Flexible credit system" (PRICING TIER DETAIL)
**Position:** Right before the main pricing cards section  
**Purpose:** Help users understand which check to buy

Three side-by-side cards:

| Quick Check | Full Report | Premium |
|-------------|-------------|---------|
| 3 credits (~30-50p) | **10 credits (~£1.00)** | 14 credits (~£1.40) |
| Overview + valuation | Everything but AI | Full suite + AI |
| For quick price check | **FREE on first** | For dealers/high-value |
| 4 bullet points included | 5 bullet points included | 4 bullet points included |
| 2 bullet points missing | All included | All included |

**Visual highlights:**
- Full Report has blue border + "FIRST ONE FREE" banner
- Each card shows cost per check
- "Best for" guidance at bottom

**Layout:** 3-column grid with equal height cards  
**Mobile:** Stacks to 1 column  

---

## Layout Patterns Used

All four sections use **alternating grid layouts** with screenshots on one side and explanatory text on the other:

```html
<div style="display:grid;grid-template-columns:1fr 1fr;gap:32px;align-items:center">
  <div>Text content</div>
  <figure>Screenshot with caption</figure>
</div>
```

Mobile responsiveness handled via media query (existing breakpoints used).

---

## Visual Verification

✅ Desktop (1280px): All layouts render cleanly, images display at proper size  
✅ Mobile (390px): Sections stack vertically, images are full-width, text is readable  

Screenshots saved:
- `screenshot-desktop.jpg` – full page at 1280px
- `screenshot-mobile.jpg` – full page at 390px

---

## Assets Used

All screenshots are **reused from existing report assets**:
- `assets/report/features/feat-overview.jpg`
- `assets/report/features/feat-ai.jpg`
- `assets/report/features/feat-dsb.jpg`
- `assets/report/features/feat-buildsheet.jpg`
- `assets/report/features/feat-mot.jpg`
- `assets/report/report-trend.jpg`

No new assets needed.

---

## Key Messages Communicated

Users now understand:

1. **What makes us different**
   - AI condition assessment (not just MOT)
   - Real repair costs (not generic valuation)
   - OEM data access (not public scraping)

2. **What's in each report section**
   - Vehicle overview with grading
   - Service history stamped by dealers
   - Build sheet with equipment
   - MOT trend with clocking detection
   - Valuation with market projections
   - AI visual assessment with itemized repairs

3. **Why each credit tier exists**
   - Quick check = price only
   - Full report = comprehensive (and free first time)
   - Premium = full + AI condition

4. **Value proposition clarity**
   - Not just "we check cars" but "we tell you what they're worth"
   - Not generic but specific (repair lists, market grades, dealer stamps)
   - Not gambling but data-driven (refurb-adjusted, projected, graded)

