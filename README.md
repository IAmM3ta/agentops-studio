# Agent Ops Studio

Public marketing site for [agentops.studio](https://agentops.studio).

Agent Ops Studio is a sub-brand of Memetic Media, run by Robert F. Thomas. The site offers **LedgerWright / Spreadsheet Rescue**: AI-assisted bookkeeping and data-desk work for small businesses (contractors, trades, property managers, and similar). Supplier bills, receipts, and messy spreadsheets are cleaned, categorized, and tagged by job and cost type, then returned as CSV and Excel.

This repository is the website only. It is plain HTML and CSS, served free from GitHub Pages. There is no build step, no application source, and no secrets.

## File structure

| Path | What it is |
| --- | --- |
| `index.html` | The whole marketing page: hero, how it works, services and pricing, sample, FAQ, contact |
| `404.html` | Page shown for unknown addresses |
| `css/styles.css` | All presentation. Mobile-first |
| `assets/favicon.svg` | Icon used by modern browsers |
| `assets/favicon-32.png` | PNG icon |
| `assets/apple-touch-icon.png` | Icon for phones saving the site to the home screen |
| `assets/og.png` | Image used when the link is shared (1200×630) |
| `favicon.ico` | Fallback icon requested at the site root |
| `sitemap.xml` | Sitemap for the homepage |
| `robots.txt` | Crawler rules, points at the sitemap |
| `CNAME` | Custom domain. The file contains exactly `agentops.studio` |
| `.github/workflows/pages.yml` | Deploys the site to GitHub Pages on every push to `main` |
| `CHANGELOG.md` | Dated notes. This repo keeps an entry for each day the site changes |

Root-absolute paths (`/css/styles.css`, `/#pricing`) are used because the site is hosted at the domain root. Preview it with a local server, not by opening the HTML file directly.

## Preview locally

From the repository root:

```bash
python3 -m http.server 8080
```

Then open [http://127.0.0.1:8080/](http://127.0.0.1:8080/). The unknown-page layout is at [http://127.0.0.1:8080/404.html](http://127.0.0.1:8080/404.html). GitHub Pages will also serve `404.html` for missing paths once the site is published.

## Edit prices and copy

Almost everything a visitor reads is in `index.html`. `404.html` repeats the header, the Pay / Book link, and the copyright line. If you change one, change the other.

**Prices.** In `index.html`, search for the comment `PRICES`. The four catalog figures are:

- Starter (Spreadsheet Rescue): **$150**
- Standard: **$350**
- Premium: **$750**
- Monthly retainer: **from $750/mo, ask for a quote**

Those numbers appear three times. Update all of them together:

1. The visible cards in the pricing section
2. The footnote under the cards, if the Square checkout amount changes
3. The `application/ld+json` block in the document head (`price` and `minPrice`)

**Payment link.** Every Pay / Book button uses:

```text
https://square.link/u/rX4tuObB
```

Search for `square.link` and replace each one if the link changes. As of 2026-11-21 that Square page checks out **Spreadsheet Rescue at $150**, described there as one messy spreadsheet delivered within 48 hours. The Starter card and the turnaround answer repeat that 48-hour promise. If the Square offer changes, update the Starter card, the FAQ turnaround answer, the pricing footnote, and this README together. Standard, Premium, and the retainer tell the visitor to email first so the amount can be confirmed before they pay.

**Contact.** The only public email is `robert@agentops.studio`. Search for `mailto:` in both HTML files.

**Sample.** The before/after table and the three example cards are fictional and say so in several places. Keep that label if you rewrite the rows. Do not replace them with a real client's file.

**Donor sample (added 2026-11-22).** `index.html` has a second sample at `#donors` for nonprofit gift exports, plus a FAQ answer. The rows follow the fictional `donors` profile sample in the private tool repo. Keep these limits in the copy: duplicates are linked not merged, doubtful gifts stay blank, each row reports receipt-readiness, and the service does not write receipts or edit a donor database. The footer links to `/#donors` (the header nav is unchanged). The meta description mentions donor lists. `sitemap.xml` lastmod is 2026-11-22.

**Naming.** Public copy uses only these names:

- Robert F. Thomas
- Memetic Media
- Agent Ops Studio

Do not add a phone number, a street address, testimonials, client names, statistics, or certifications. Do not add third-party scripts, fonts, or trackers. The page loads one stylesheet and no JavaScript on purpose.

Package blurbs (what "a short stack" or "a larger desk" means) are the public description of the catalog. If the real scope of a tier is different, edit that card's paragraph. The page already says odd files are quoted before payment.

## Deploy

Pushes to `main` run `.github/workflows/pages.yml`. The workflow checks that `CNAME` is exactly `agentops.studio`, then runs:

1. `actions/configure-pages`
2. `actions/upload-pages-artifact` (the repository root)
3. `actions/deploy-pages`

You can also run it by hand from the Actions tab (`workflow_dispatch`).

**One-time Pages setup** (a person with admin access on the repository):

1. Settings → Pages → Build and deployment → Source: **GitHub Actions**.
2. After the first successful deploy, set the custom domain to `agentops.studio`. The `CNAME` file in the repo does not, by itself, register the domain in the Pages settings.
3. When the certificate is ready, enforce HTTPS.

Until the custom domain is attached, GitHub may also offer the project URL `https://iamm3ta.github.io/agentops-studio/`. Styles and images on this site use root paths, so use the custom domain (or a local server) to review the design. The project URL under `github.io` will not find `/css/styles.css`.

## DNS

At the registrar for `agentops.studio`:

**Apex (`@`) — four A records**

- `185.199.108.153`
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

**`www` — one CNAME**

- `www` → `iamm3ta.github.io`

Point `www` at `iamm3ta.github.io`, not at the repository name and not at a `*.github.io` host that includes the project. GitHub redirects between the apex and `www` once both are in place. The domain written in `CNAME` (the apex, `agentops.studio`) is the one visitors should see.

Remove any old A, AAAA, or CNAME records on `@` and `www` that point somewhere else. A proxy that terminates HTTPS in front of GitHub Pages will fight the certificate GitHub issues. Leave the records as DNS only.

GitHub's own Pages docs also list AAAA (IPv6) records. Check those docs before adding any, in case the addresses have changed, and keep the four A records above either way.

Verify the domain in the GitHub account or organization Pages settings and add the TXT record GitHub shows you. That stops another project from claiming `agentops.studio`.

DNS changes can take a while to show up everywhere. After they do, confirm:

```bash
dig +short agentops.studio A
dig +short www.agentops.studio CNAME
```

The A lookup should list the four addresses above. The CNAME lookup should end at `iamm3ta.github.io`.

## Changelog

This repo follows a daily-commit practice. When you change the site, add a dated entry at the top of `CHANGELOG.md` for that day, then commit. Newest entries go first. One entry can cover several commits made on the same day.

## What this repo is not

- Not the LedgerWright program. Do not commit its source.
- Not a place for API keys, tokens, or `.env` files.
- Not a form backend. Contact is a `mailto:` link to `robert@agentops.studio`.
