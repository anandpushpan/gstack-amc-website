# Project Status — AnalyzeMyCar homepage

**This is the pick-up document.** If you are new to this project, read this first,
then `README.md` for the full version history. It tells you what is done, what is
planned, and what is deliberately on hold.

**Current version: v2.8** (2026-06-13) · Status: draft, not yet wired to a backend.

---

## How this project works (read before editing)

- **Local-first.** All work happens on local files. Only finished versions are
  pushed to GitHub, which auto-deploys to Vercel. Do not edit live on the server.
- **Every change is versioned.** When you finish a round of work:
  1. Freeze a snapshot: copy `index.html` to `versions/index-YYYY-MM-DD-vX.Y.html`
  2. Write a changelog: `changes/index-YYYY-MM-DD-vX.Y-changes.md`
  3. Add a row to the version table in `README.md`
  4. Update the "Current version" line and the Done list in this file
- **Naming:** `index-[date]-[version]` for snapshots and changes; `index-[date]-audit-NN` for audits.
- **Folders:** `versions/` (frozen snapshots), `changes/` (per-version changelogs),
  `audits/` (design/content reviews). `index.html` is always the live, latest copy.
- **Honesty guardrails (do not break):** no fabricated stats or reviews; no
  finance / write-off / stolen claims until confirmed; first report free is real;
  credits expire after 180 days. Match all credit pricing to the live product model below.

## Deploy (Vercel)

Static site, `index.html` at the repo root. Vercel auto-detects it, no build step.
Push to `main` and Vercel deploys. No framework, no `vercel.json` needed.

## Credit model (owner-confirmed, must stay accurate everywhere)

The product uses a module picker. Each module costs credits:

| Module | Credits | In the free first report? |
|--------|---------|---------------------------|
| Basic Info | 1 | Yes |
| Build Sheet + Valuation | 2 | Yes |
| DSB + MOT | 3 | Yes |
| AI Visual Assessment | 4 | No — paid add-on, even on the first report |
| Full report (all four) | 10 | n/a |

Credits expire 180 days after purchase. First report free for everything except AI Visual.

---

## DONE (shipped through v2.0)

| Version | What shipped |
|---------|--------------|
| v1.0 | First documented baseline on the AnalyzeMyCar design system. |
| v1.1 | Applied Audit 01: mobile nav, focus states, contrast, real social links, realistic dealer numbers, honest JSON-LD, pinned icons, reduced-motion, favicon. |
| v1.2 | Mobile hero optimised; report preview switched to real sample-report screenshots. |
| v1.3 | Feature cards became screenshot-led (each module shows its real report section + credit cost). |
| v1.4 | Added deep-dive sections with real screenshots (comparison, factory data, MOT/valuation, credit value). |
| v1.5 | Credit pricing corrected everywhere to match the live module picker; FAQ + JSON-LD + badges fixed. |
| v1.6 | Design-review pass: restored white/soft section alternation; tightened the H3 type scale. |
| v1.7 | Module picker moved into the hero (interactive, with a live "your free report" summary). |
| v2.0 | Mobile-first overhaul: action-first hero, one-tap free report, sticky thumb-zone CTA, input ergonomics + 44px touch targets, dealer band below the consumer flow on mobile, 4G perf. Desktop unchanged. |
| v2.1 | Added Privacy, Terms and Refund pages (drafts) on a shared `assets/legal.css`; wired the homepage footer links. |

**Where the site stands:** a complete, honest, mobile-first marketing homepage plus
draft legal pages. Visuals, copy, structured data, responsive behaviour and the
credit model are all in place. The legal pages are drafted but NOT yet reviewed (see below).

## NEEDS REVIEW (drafted, not cleared for launch)

The Privacy / Terms / Refund pages were reconciled against the live site in v2.2,
which closed most open items. Each still shows a "Draft, pending legal review"
banner. **A qualified adviser must sign off before launch.** Remaining open items:
- **Privacy (7 `[TO CONFIRM]`):** ICO registration number, named payment
  processor, named hosting / sub-processors, full cookie list.
- **Terms:** no open markers; have an adviser confirm the liability cap and
  data-usage clauses fit your licences.
- **Refund:** no open markers; have an adviser confirm the statutory cancellation wording.

**Decisions locked in v2.2** (so nobody re-litigates them):
- Credits expire **180 days** after purchase (our position; the live Terms say
  no-expiry and are out of date, they should be updated to match us).
- We deliberately do **not** claim finance / write-off / stolen data until the
  product is confirmed to deliver it.
- Legal pages use **support@analyzemycar.com** and **14 business days** for refunds.

**Cross-page mismatch to fix:** the homepage FAQ/footer still use
info@analyzemycar.com and "5 to 10 business days"; the legal pages use support@
and 14 business days. Align the homepage once the canonical contact is confirmed.

## PLANNED (next, not started)

- **Wire up the backend.** All CTAs are placeholders (`href="#"`). Needed: reg/VIN
  lookup endpoint, free-account signup + report flow, "Buy credits" checkout.
  (Privacy / Terms / Refund pages now exist as drafts, see NEEDS REVIEW above.)
- **Other footer pages still missing:** Sample report, About, Contact, Blog.
- **OG share image** (1200x630) for link previews before launch.
- **v2.1: dealer-band placement on mobile.** It currently lands after the final
  CTA (via CSS flex order). Revisit whether it belongs higher in the mobile flow.
- **Info icons on the hero picker** (optional). Per-module `i` tooltips at the
  point of choice, mirroring the live product, so users learn what each module
  contains without scrolling.
- **Real reviews.** Add a Trustpilot embed once a real profile with real reviews exists.

## ON HOLD (blocked — needs a decision or confirmation, do not action)

- **Provenance block (finance / write-off / stolen).** OFF until the product team
  confirms these checks are actually delivered. The live site advertises "finance
  databases" but the sample report does not show finance/write-off/stolen markers.
  Shipping these unconfirmed is a mis-sell / legal exposure. There is a commented
  placeholder in `index.html` (search "OPTIONAL PROVENANCE BLOCK") to enable once confirmed.
- **Ratings / user counts.** The previous live site showed "4.9/5" and "50,000+
  users" with no data behind them (owner-confirmed false). Removed. Do NOT re-add
  any rating, count, or testimonial until real and verifiable.

---

_Last updated: 2026-06-13 (v2.0). Keep this file current as part of every version bump._
