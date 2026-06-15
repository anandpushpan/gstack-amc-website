# AnalyzeMyCar — Homepage Draft (g-stack-developed)

**Date:** 2026-06-13 (updated)  ·  **Status:** Draft for review. Not production.
**Built on:** the AnalyzeMyCar design system (Onest / Manrope / IBM Plex Mono).

> **New here? Read [STATUS.md](STATUS.md) first** — it covers what's done, what's
> planned, what's on hold, and how the local-first versioning + Vercel deploy work.

This is a strategy-driven, mobile-first homepage draft. Open `index.html` in a
browser to preview.

---

## How this folder works (read this first)

`index.html` is always the **live, latest** working copy. Every milestone is frozen and documented
so anyone opening this folder can see what exists, what changed, and what's still to fix.

```
g-stack-developed-website/
├─ index.html        ← LIVE working copy (always the latest)
├─ assets/           ← images (logo, etc.)
├─ versions/         ← frozen snapshots, one per version
├─ audits/           ← reviews of a version (findings + fixes to make)
├─ changes/          ← changelog per version (what changed and why)
└─ README.md         ← this file (overview + version history)
```

**Naming convention:** `[file]-[date]-[version]` (or `-audit-NN`).
- Snapshot:  `versions/index-2026-06-11-v1.0.html`
- Audit:     `audits/index-2026-06-11-audit-01.md`
- Changelog: `changes/index-2026-06-11-v1.0-changes.md`

**Workflow:** audit the live file → apply fixes → freeze a new `versions/` snapshot → write its
`changes/` doc → bump the version here. Audits that haven't been actioned stay listed as Open.

## Version history

| Version | Date | Snapshot | Changes | Audit | Notes |
|---------|------|----------|---------|-------|-------|
| **v2.8** | 2026-06-13 | [snapshot](versions/index-2026-06-13-v2.8.html) | [changes](changes/index-2026-06-13-v2.8-changes.md) | (trust copy) | **Current.** Removed the "Real reviews only / newly launched in the UK" placeholder from the trust section. Flagging newness gave visitors a reason to hesitate without adding trust. The section now ends on its four verifiable cards (official data, OEM, UK company, secure payment). A dev comment marks where a Trustpilot embed goes once a real profile exists. |
| v2.7 | 2026-06-13 | [snapshot](versions/index-2026-06-13-v2.7.html) | [changes](changes/index-2026-06-13-v2.7-changes.md) | (mobile fix) | Fixed the module-card credit chip overflowing the right edge on mobile after the v2.6 redesign. On phones the icon and credit chip now stack (icon above, chip below, left-aligned) so the longer labels never get clipped. Verified 0px overflow at 320/360/390px. Desktop unchanged. |
| v2.6 | 2026-06-13 | [snapshot](versions/index-2026-06-13-v2.6.html) | [changes](changes/index-2026-06-13-v2.6-changes.md) | (card redesign) | Redesigned the "Everything in one valuation report" module cards. They used to crop a tall report screenshot into a thin strip with the credit pill floating over it, which read as broken. Now each card is a clean icon tile + credit chip in a top row, then title and description. The full screenshots still live in the deep-dive section below. Desktop and mobile both verified. |
| v2.5 | 2026-06-13 | [snapshot](versions/index-2026-06-13-v2.5.html) | [changes](changes/index-2026-06-13-v2.5-changes.md) | (mobile polish) | Removed the top "Check a car" CTA on mobile (logo + menu only), centred all section-header overlines for consistency, and made the sticky bottom CTA appear only after the hero fully scrolls past. Desktop unchanged. |
| v2.4 | 2026-06-13 | [snapshot](versions/index-2026-06-13-v2.4.html) | [changes](changes/index-2026-06-13-v2.4-changes.md) | (mobile fix) | Fixed the hero card and source strip running edge-to-edge on mobile: restored 24px side padding (a `.hero-in` padding shorthand was zeroing it) and set the mobile hero flex to stretch (an inherited `align-items:center` was letting the card overflow). |
| v2.3 | 2026-06-13 | [snapshot](versions/index-2026-06-13-v2.3.html) | [changes](changes/index-2026-06-13-v2.3-changes.md) | (mobile fix) | Fixed the three deep-dive comparison sections that didn't collapse on mobile: the six image+content blocks now stack image-above-content on phones (were cramped side by side). Desktop unchanged. |
| v2.2 | 2026-06-13 | (legal pages updated) | [changes](changes/index-2026-06-13-v2.2-changes.md) | (live comparison) | Reconciled the legal pages against the live site: filled company number, retention periods, liability cap and dispute resolution; added definitions, data-usage, sanctions, automated-decision and children's-privacy sections; switched to support@ and 14-day refunds. Kept 180-day expiry and the no-finance-data position. Snapshots: [privacy v1.1](versions/privacy-2026-06-13-v1.1.html) · [terms v1.1](versions/terms-2026-06-13-v1.1.html) · [refund v1.1](versions/refund-2026-06-13-v1.1.html). |
| v2.1 | 2026-06-13 | [snapshot](versions/index-2026-06-13-v2.1.html) | [changes](changes/index-2026-06-13-v2.1-changes.md) | (legal pages) | Added Privacy, Terms and Refund pages (drafts, pending legal review) on a shared `assets/legal.css`, and wired the homepage footer links. Each page carries a draft banner and `[TO CONFIRM]` markers for unverified items. Snapshots: [privacy](versions/privacy-2026-06-13-v1.0.html) · [terms](versions/terms-2026-06-13-v1.0.html) · [refund](versions/refund-2026-06-13-v1.0.html). |
| v2.0 | 2026-06-13 | [snapshot](versions/index-2026-06-13-v2.0.html) | [changes](changes/index-2026-06-13-v2.0-changes.md) | (mobile-first) | Mobile-first overhaul for the dealer-forecourt scenario: action-first hero (reg input first on phones), one-tap free report (picker collapses behind "Customize"), sticky thumb-zone CTA, input ergonomics + 44px touch targets, dealer band pushed below the consumer flow on mobile, 4G performance tuning. Desktop unchanged. |
| v1.7 | 2026-06-13 | [snapshot](versions/index-2026-06-13-v1.7.html) | [changes](changes/index-2026-06-13-v1.7-changes.md) | (product IA) | Brought the module picker into the hero (Option A): four tappable module rows under the reg/VIN input, pre-ticked free modules + AI Visual as a paid add-on, with a live "your free report" summary. Mirrors the real product; makes "free" tangible. Deeper module section reframed as the "checking more cars" credit story. |
| v1.6 | 2026-06-13 | [snapshot](versions/index-2026-06-13-v1.6.html) | [changes](changes/index-2026-06-13-v1.6-changes.md) | gstack /design-review | Design-review pass: restored white/soft section alternation (the new v1.4 sections had created two white-on-white seams), tightened the H3 type scale from 5 sizes to 4. Design Score A-, AI Slop Score A. |
| v1.5 | 2026-06-12 | [snapshot](versions/index-2026-06-12-v1.5.html) | [changes](changes/index-2026-06-12-v1.5-changes.md) | (fact-check vs live site) | Credit pricing corrected everywhere to match the live product's module picker: Basic Info (1cr), Build Sheet + Valuation (2cr), DSB + MOT (3cr), AI Visual (4cr, excluded from free report). Fake tier section replaced with a picker replica + "spend credits efficiently" guide. FAQ + JSON-LD + feature badges fixed. |
| v1.4 | 2026-06-12 | [snapshot](versions/index-2026-06-12-v1.4.html) | [changes](changes/index-2026-06-12-v1.4-changes.md) | (visual QA) | Added four **deep-dive sections with real report screenshots** so users see exactly what they're paying for: "What's inside" (comparison), "Factory data" (service + build sheet), "MOT & valuation" (trends), and "Credit value" (tier breakdown). All alternating layouts, mobile-responsive, verified by Playwright. NOTE: the credit tiers in this version were wrong; corrected in v1.5. |
| v1.3 | 2026-06-11 | [snapshot](versions/index-2026-06-11-v1.3.html) | [changes](changes/index-2026-06-11-v1.3-changes.md) | (visual QA) | Feature cards now **screenshot-led** (each module shows its real report section + credit cost in `assets/report/features/`). Report gallery simplified to one featured page. |
| v1.2 | 2026-06-11 | [snapshot](versions/index-2026-06-11-v1.2.html) | [changes](changes/index-2026-06-11-v1.2-changes.md) | (visual QA) | Mobile hero optimised (verified by Playwright screenshots; fixed a headline-spacing bug). Report-preview switched to **real sample-report screenshots** instead of a CSS mockup. |
| v1.1 | 2026-06-11 | [snapshot](versions/index-2026-06-11-v1.1.html) | [changes](changes/index-2026-06-11-v1.1-changes.md) | (addressed audit 01) | Applied all Audit 01 findings: mobile nav, focus states, contrast, real social links, realistic dealer numbers, report-preview visual, differentiated cards, honest JSON-LD, pinned icons, trimmed fonts, reduced-motion, favicon, heading hierarchy. |
| v1.0 | 2026-06-11 | [snapshot](versions/index-2026-06-11-v1.0.html) | [changes](changes/index-2026-06-11-v1.0-changes.md) | [audit 01](audits/index-2026-06-11-audit-01.md) | First documented baseline. Built on the design system + owner feedback round (Presentation1.pdf). |

---

## What this is
A single self-contained `index.html` (design tokens + component CSS inlined) plus the brand
logo in `assets/`. It uses the design system exactly: **Onest** (headings), **Manrope** (body),
**IBM Plex Mono** (plates/VINs/figures), and the **blue → teal → lime** brand gradient, with the
system's header, lookup card, feature grid, pricing cards and navy footer.

To ship into the real codebase: lift the `<style>` block back into the system's
`colors_and_type.css` + `kit.css` (most of it is copied verbatim from there), and wire the
reg/VIN form + buttons to your live endpoints.

## Design system review (you asked)
The exported system is strong and I used it as-is. Notable strengths:
- Honest, valuation-led positioning already baked into the kit's own copy ("Everything in one
  valuation report") — it does **not** overclaim finance/write-off. That matches our reframe.
- Proper data typography (mono, tabular figures) — right for a numbers product.
- UK plate component with reg/VIN toggle that mirrors the real product flow.

Two small suggestions (not blockers):
1. The kit had no **differentiator** section for the refurb-adjusted valuation (your moat). I added
   one — consider promoting it into the system as a reusable "valuation card" component.
2. The kit had no **trust** section. I added an honest one; the system should ship a trust block so
   nobody re-adds fabricated stats later.

## Key decisions (all from the audit)
1. **Lead with the moat, not a mood.** Hero = "Know what a used car is *really worth* before you
   buy." The dedicated "Most checks tell you the past. We tell you the price." section shows the
   refurb-adjusted valuation (£3,950 − £1,759 = £2,191) — the thing no competitor does.
2. **Free first report is the hook** (owner-confirmed real), featured in the hero badge + widget,
   with the credit model for subsequent checks.
3. **Dedicated dealer band** ("Know your margin before you buy the stock") — the trade-first wedge,
   with a margin worked-example. Not buried in a footer link.
4. **Honest trust only.** Removed "50,000+ users" and "4.9/5" (owner-confirmed false) and all
   fabricated testimonials. Replaced with real signals (official data, UK company, secure/refund)
   and a confident "newly launched, real reviews only" placeholder.
5. **No provenance overclaim.** Finance / write-off / stolen are **not** claimed anywhere, because
   the sample report doesn't show them and the team is unsure they're delivered.
6. **Reg + VIN toggle** matches the actual product flow you described.

## ⚠️ Flags to resolve BEFORE shipping (do not deploy with these open)
- [ ] **Provenance checks (CRITICAL):** confirm whether finance / write-off / stolen are delivered.
  If yes, enable the commented "OPTIONAL PROVENANCE BLOCK" in the features section. If no, ensure
  the live site stops advertising "finance databases" (current mis-sell / legal exposure).
- [ ] **Trust claims:** the fabricated "50,000+ / 4.9" must come off the *live* site too, not just
  this draft (see `../g-stack-research/AnalyzeMyCar-LiveSite-Audit.md`, finding #6 — legal liability).
- [ ] **Reviews:** only add ratings/testimonials once a real Trustpilot profile exists; paste the
  official embed where the placeholder is marked.
- [ ] **Dealer numbers:** the margin example is illustrative — replace with a real worked example or
  mark clearly as indicative (already labelled).
- [ ] **Wire it up:** reg/VIN form → lookup endpoint; "Get my free report" → signup/report flow;
  "Buy credits" → checkout; Privacy/Terms/Refund links → real pages.
- [ ] **Assets:** add favicon + a 1200×630 OG share image.

## What's intentionally NOT here
- No modal pop-up on load (the live site's pop-up blocks the primary CTA and stacks with the cookie
  banner — the free offer is in the hero instead).
- No finance/write-off/theft claims.
- No fabricated social proof.

## Files
- `index.html` — the homepage draft (self-contained)
- `assets/logo-full.png` — brand logo (from the design system)
- `README.md` — this file
