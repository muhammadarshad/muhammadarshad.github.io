# marshad.pw — personal site

Local build of the identity hub for Muhammad Arshad, founder of MAGSpace. It is not published. Do not push, create a GitHub repository, or change DNS until he approves the steps below.

## Files

- `index.html` — one-page site
- `styles.css` — self-contained styles (dark / light)
- `CNAME` — `marshad.pw`
- `robots.txt`, `sitemap.xml`, `404.html`
- `assets/favicon.svg`, `assets/og-image.png` (1200×630)
- `assets/fonts/` — self-hosted Newsreader and Instrument Sans (SIL OFL 1.1)
- `preview-desktop.png`, `preview-mobile.png` — local QA screenshots (need not be published)

## Where the files should go

The public user-site repository `muhammadarshad/muhammadarshad.github.io` does not exist (GitHub API 404, and `https://muhammadarshad.github.io/` is 404). The research project site `muhammadarshad/pages-mprc` already serves `https://muhammadarshad.github.io/pages-mprc/`.

Publish this page from a **new** repo named `muhammadarshad.github.io`. Do not add these files to `pages-mprc`.

Note: GitHub Pages applies a user-site custom domain to project sites by default, so once `marshad.pw` is attached, the MPRC hub is also expected at `https://marshad.pw/pages-mprc/`. Existing `muhammadarshad.github.io/pages-mprc/` links should still be checked after go-live (GitHub often redirects the default host to the custom domain). Do not set a separate custom domain on `pages-mprc` unless that move is intentional.

## DNS records (from GitHub docs)

Source: [Managing a custom domain for your GitHub Pages site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

GitHub says to add the custom domain in the repository Pages settings **before** pointing DNS at GitHub, to reduce subdomain-takeover risk. Also consider verifying `marshad.pw` at the account level first. Do not add wildcard records (`*.marshad.pw`). Remove any parking or default `@` / `www` records that do not match the table.

Apex (`marshad.pw`, host `@`) — all four A records and all four AAAA records:

| Type | Name | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |

`www` subdomain (recommended so GitHub can issue HTTPS and redirect `www` to the apex):

| Type | Name | Value |
| --- | --- | --- |
| CNAME | `www` | `muhammadarshad.github.io` |

Some registrars want a trailing dot on the CNAME target (`muhammadarshad.github.io.`). If the registrar supports `ALIAS`/`ANAME` at the apex, that can point `@` at `muhammadarshad.github.io` instead of the A/AAAA set; A + AAAA is the portable option. GitHub recommends keeping A records if you also add AAAA.

DNS can take up to 24 hours. Then enable **Enforce HTTPS** in the repo Pages settings.

## Publishing steps that need approval

None of these have been done.

1. Create a public GitHub repository named `muhammadarshad.github.io` under the `muhammadarshad` account.
2. Push these site files (optional: omit `preview-desktop.png` and `preview-mobile.png`).
3. In the repo: Settings → Pages → serve from the default branch, folder `/ (root)`.
4. Optionally verify `marshad.pw` in the account Pages domain settings.
5. Set the custom domain to `marshad.pw` and save (GitHub may write or refresh `CNAME`).
6. At the registrar, add the A, AAAA, and `www` CNAME records above; remove conflicting records.
7. After DNS resolves, turn on Enforce HTTPS.
8. Point GitHub, LinkedIn, X, and ORCID website fields at `https://marshad.pw`, and add the site to Google Search Console.

A consistent portrait still needs to be supplied before the initials mark can be replaced.
