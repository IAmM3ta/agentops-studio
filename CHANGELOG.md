# Changelog

## Scope

Agent Ops Studio is the Memetic Media sub-brand for LedgerWright templates, Spreadsheet Rescue, and custom business dashboards, operated by Robert Thomas. Constraints: $0 spend freeze (free Vercel and Neon tiers only; no paid services, domains, or API runs without Robert's OK). Cold email is on hold.

## 2026-11-26

### Added

- New page [/donor-list/](https://agentops.studio/donor-list/), "Clean the donor list before the year-end receipts go out", for nonprofits heading into Giving Tuesday and December receipts. It covers what the donor cleanup does (likely duplicates and households linked with a reason and never merged; pledges, hedged or double amounts, and unwritten dates left blank; DAF and matching-gift rows marked unclear for hard vs soft credit; every row says receipt ready yes or no and why), a fictional SAMPLE before/after table of ten of the 16 sample rows, the seven-line report ("Booked gifts: $7,490.00 across 13 rows"), the same pricing (the Square link charges only the $150 Starter; higher tiers email first), and contact. Service JSON-LD with the $150 Starter offer.
- The sample rows come from the private engine's `samples/donors_export.txt`. A live grok-4.5 run of the donors profile on 2026-11-26 gave the same headline, report lines, and per-row values, so the page says "checked against a live run" for this sample only, and states plainly that it is not an accuracy rate and that we don't write receipts, give tax advice, or import into donor databases.
- Homepage `#donors` section has a "See the full donor-list sample" button, and the donor FAQ answer links to the new page. The "Donor lists" footer link on the homepage, `/rent-roll/`, `/mixed-currency/`, and `/excel-formula-fix/` now goes to `/donor-list/`.
- `sitemap.xml` lists `/donor-list/`, and the homepage lastmod is now 2026-11-26.

### Unchanged

- Prices, the Square links, `CNAME`, Pages settings, and DNS. No address, phone, or secret was added.

## 2026-11-25
- `/excel-formula-fix/`: new #prices section with pay-after-preview tiers on new Square links: Small fix $10 (https://square.link/u/mhkT08AL), Standard $25 (https://square.link/u/LKtpxWZs), Dashboard/Tracker $50 (https://square.link/u/O2381SNX), plus the $150 Starter for bigger jobs. JSON-LD offers, meta descriptions and FAQ updated to match; the header CTA on this page now jumps to #prices instead of the $150 checkout.
- New high-intent page `/excel-formula-fix/` ("Formula broken? See it fixed before you pay"): pay-after-preview flow (PREVIEW screenshots first, then the existing $150 Starter Square link), free 20-row fix via prefilled email, $14/$24 Gumroad trackers for visitors who don't need a fix, Service + FAQPage JSON-LD. Linked from the homepage teardown section and footer; added to `sitemap.xml`.
- IndexNow key file at the site root so new URLs can be submitted to Bing/Yandex.

### Added

- New page [/mixed-currency/](https://agentops.studio/mixed-currency/), "Bills in dollars, euros, and pounds", for anyone whose bills tracker adds EUR to USD. It covers what the cleanup does (open, billed, and credit totals kept per currency, with no conversion and no cross-currency grand total; "$612.50 CAD" stays CAD; European "1.450,00" is read as 1,450.00 and labeled; a computed balance is labeled), a fictional SAMPLE before/after of six bills in USD, CAD, EUR, and GBP, the same pricing (Square link charges only the $150 Starter; higher tiers email first), and contact. The sample comes from the private engine's `samples/currency_invoices.txt` and matches its stand-in output: "6 documents, $320.00, 612.50 CAD, 950.00 EUR, and 780.00 GBP still open."
- Homepage FAQ: "Some of my bills are in euros, pounds, or Canadian dollars. Is that a problem?" It links to the new page.
- `sitemap.xml` lists `/mixed-currency/`. The homepage and `/rent-roll/` lastmod are now 2026-11-25. Footer link "Mixed-currency bills" added on the homepage, `/rent-roll/`, and the new page.

### Unchanged

- Prices, the Square link, `CNAME`, Pages settings, and DNS. No address, phone, or secret was added. The page says plainly that we don't convert currencies or post to accounting software.

## 2026-11-24

### Changed

- Homepage JSON-LD `makesOffer` now includes the three live LedgerWright Gumroad templates, with the same prices and URLs as the `#templates` buttons: [Cash Flow Tracker](https://ledgerwright.gumroad.com/l/cashflow-tracker) $14, [LedgerWright Bundle](https://ledgerwright.gumroad.com/l/ledgerwright-bundle) $24, [Job-Cost Tracker](https://ledgerwright.gumroad.com/l/job-cost-tracker) $14. Square offers are unchanged.
- Added `twitter:image:alt` on the homepage and `/rent-roll/` (matching each page's `og:image:alt`) so shared-image previews have accessible text.
- `/dashboard-intake/` now has Open Graph and Twitter card tags, so a shared intake link is not a bare URL. Prices in those tags stay $750 / $1,500.

### Unchanged

- Gumroad buy buttons on `#templates` are unchanged. No address, phone, or secret was added. `CNAME`, Pages settings, and DNS were not touched.

## 2026-11-23

### Added

- LedgerWright Gumroad store is live (seller: [ledgerwright](https://ledgerwright.gumroad.com)):
  - [Cash Flow Tracker](https://ledgerwright.gumroad.com/l/cashflow-tracker), $14
  - [Job-Cost Tracker](https://ledgerwright.gumroad.com/l/job-cost-tracker), $14
  - [LedgerWright Bundle](https://ledgerwright.gumroad.com/l/ledgerwright-bundle), $24
- Payouts are set up on Gumroad.
- "Buy on Gumroad" buttons are live on [agentops.studio](https://agentops.studio) (`#templates`) and the [LedgerWright templates page](https://iamm3ta.github.io/ledgerwright-templates/). Placeholder coming-soon notes and mailto links were replaced; JSON-LD offers point to Gumroad.

### Existing

- Square checkout links on [agentops.studio](https://agentops.studio) for Spreadsheet Rescue and dashboard builds: $150, $295 Founding Bundle (through Dec 1), $250 deposit, $750, $1,500.

### Changed

- Upwork profile completeness went from 60% to 65% (languages, four skills, and a portfolio item; rate remains $85/hr). Two catalog projects are approved and live: Bill tagging ($150 / $350 / $750) and 500-row cleanup ($150). No Connects were bought.

### In progress

- LedgerWright Autopilot MVP is in private preview (116/116 tests). `ledgerwright-desk` PR #1 is unmerged. Launch still needs an xAI key and a payment gate.

### Planned

- Fiverr and Contra listings, Upwork job watching, and daily revenue routines.

### Out of scope

- No projects have been paused or killed. Portfolio park/kill decisions remain pending Robert's review.

## 2026-11-23
- Staged (not live until merged to `main`): `#templates` cards gain a "Buy on Gumroad" button next to the existing "See the … tracker" link (Cash Flow $14, Bundle $24, Job-Cost $14). Square Pay / Book links for Spreadsheet Rescue and dashboards are unchanged — those are different products. Prices unchanged.
- New page `/rent-roll/` for property managers: what the cleanup checks (rent vs paid per unit, duplicate units and tenants shown and never merged, figures read only from their own column, hedged or two-figure cells left blank, leases kept as written, ended leases marked expired rather than extended), what to send and what comes back (CSV, Excel, an "import ready" column, a short report), a fictional before/after table and three example cards labeled SAMPLE, pricing (Starter $150 by Square, Standard $350, Premium $750, retainer from $750/mo, email first), and contact. The copy matches the LedgerWright `rentroll` profile built today. Homepage: new `#rentroll` teaser after `#donors`, a "Do you clean rent rolls?" FAQ, a "Rent rolls" footer link, and a meta description that mentions rent rolls. `sitemap.xml` adds `/rent-roll/` (lastmod 2026-11-23).
- CI: Pages workflow split into build + deploy jobs with one delayed retry, fixing intermittent "No artifacts named github-pages" deploy failures.
- Fix: founding-offer note text uses solid muted color instead of opacity, so the #upkeep link passes WCAG AA contrast.

- Footer: "Part of Memetic Media" plus links to the Memetic Media network sites (Memetic Media, LedgerWright templates, Memetic Visuals, LiTHOS, MORPHOS) on the homepage, `/start/` and `/dashboard-intake/`. JSON-LD `parentOrganization` gains the Memetic Media URL.
- New `#templates` section linking the standalone LedgerWright templates page (Cash Flow $14, Job-Cost $14, Bundle $24), between `#dashboards` and `#sample`.
- Ops Dashboard Build is live (approved by Robert): homepage section `#dashboards` plus a "Dashboards" nav link, with Starter $750 (https://square.link/u/GcJ8BigP) and Pro $1,500 (https://square.link/u/XYZYaCqO), both verified enabled with redirect to `/start/`. New page `/dashboard-intake/` (intake form, no backend: prefilled email; pay buttons replace the draft's placeholders). JSON-LD offers for $750 and $1,500. `/start/` gets an "Ops Dashboard" card. `sitemap.xml` adds `/dashboard-intake/`, lastmod 2026-11-23.
- FAQ "What does the 30 days of upkeep in the Founding Bundle cover?" (`#upkeep`): two small changes (about 30 min each) or one refresh of up to about 100 rows, 48-hour business-day replies, starts at Rescue delivery, no rollover, exclusions, and how to ask by email. The Founding Bundle line under the Starter card links to it. `/start/` Founding Bundle card states the same terms.
- Founding offers under the Starter card (approved by Robert): Founding Bundle, fix + 30 days upkeep, $295 (https://square.link/u/gGVNbm1B, first 5 clients, through Dec 1) and Founding Custom Build $500 flat with a $250 deposit (https://square.link/u/tVo4GYpe). Both added to the JSON-LD offers.
- "Just paid? Send your file" strip at the top of the homepage, because the $295 and $250 links redirect to the homepage after checkout. `/start/` now has a "Which did you buy?" block for all three packages and a package field in the email subject.
- New post-payment intake page at `/start/` (`start/index.html`, `noindex`). It tells a paid Spreadsheet Rescue buyer exactly what to send, by email to robert@agentops.studio with a prefilled subject and four questions, what happens next, and the Starter scope (one source, about 200 rows or 25 documents, one revision, not advice, no live QuickBooks/Xero edits). Square's "redirect after checkout" setting should point here (see README, "Payment-to-delivery flow").
- Homepage: new first FAQ "I already paid. How do I send my file?" and a pricing-footnote link, both to `/start/`.
- Homepage: Standard, Premium, and retainer buttons changed from "Pay / Book" (which opened the $150 Starter checkout and could charge the wrong amount) to "Get a quote" email links. Their JSON-LD offer `url` now points at `/#pricing` instead of the $150 Square link. The Starter, hero, and header Pay / Book buttons still go to the Square link.

## 2026-11-22
- Public name shortened from "Robert F. Thomas" to "Robert Thomas" across the site (meta author, schema.org, copy, footer) at Robert's request.

This repository follows a daily-commit practice. Add an entry on each day the site changes. Dates are the day the change is made. Newest entries go at the top.

## 2026-11-22

- Added a fictional nonprofit donor-list sample (`#donors`) under the job-cost sample, with a before/after table and three example cards. Copy matches what the LedgerWright `donors` profile actually does: possible duplicates and households are linked, never merged; pledges, unclear amounts, missing names, and unclear dates are left blank and flagged; each row says whether it is ready for a receipt. We do not write receipts or change a donor database.
- New FAQ: "Do you clean donor lists for nonprofits?" The footer and meta description now point at that work. `sitemap.xml` lastmod is 2026-11-22.
- Standard, Premium, and retainer still tell the visitor to email first. The Square link is unchanged and still only charges the $150 Starter.

## 2026-11-21

- First public site for Agent Ops Studio (LedgerWright / Spreadsheet Rescue), reworked from an earlier LedgerWright page and branded for Memetic Media.
- Job-cost catalog: Starter $150, Standard $350, Premium $750, and a monthly retainer from $750/mo.
- Pay / Book buttons go to the Square payment link. Contact is a mailto link to robert@agentops.studio.
- Sample before/after is labeled as fictional. Draft claims that read as measured results were removed.
- GitHub Pages workflow, `CNAME` for agentops.studio, sitemap, robots.txt, 404 page, icons, and social image.
