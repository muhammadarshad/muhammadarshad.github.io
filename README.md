# marshad.pw

Source for https://marshad.pw, the personal site of Muhammad Arshad. Static HTML and CSS served by GitHub Pages.

- `index.html`: home page
- `blog/`: writing index (`_post-template.html` is a template and is not published)
- `vist-qr/`: permanent MAGSpace card destination. The default profile and product links stay available when no campaign is active. Edit `campaign.json` to turn on a campaign, set optional ISO 8601 `startsAt` / `endsAt` dates, and supply `headline`, `body`, `ctaLabel` and an HTTPS `ctaUrl`. Set `active` to `false` or let `endsAt` pass to return to the default card page. Invalid or unavailable campaign config is ignored.
- `visit-qr/`: spelling alias that forwards to `/vist-qr/`.
- `styles.css`: shared styles
- `assets/`: portrait, share image, favicon and self-hosted fonts (SIL OFL 1.1)
