# Changelog

## 2026-11-23

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
