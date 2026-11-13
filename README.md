# marshad.pw

Source for https://marshad.pw, the personal site of Muhammad Arshad. Static HTML and CSS served by GitHub Pages.

- `index.html`: home page
- `blog/`: writing index (`_post-template.html` is a template and is not published)
- `vist-qr/`: permanent MAGSpace card destination. The current GITEX campaign, project email-draft composer and readiness-studio CTA are defined here. Edit `campaign.json` to change the campaign label, official event URL, headline and support copy. Set `active` to `false` or let `endsAt` pass to return to the default hero; the project contact and product links remain available. `muhammad-arshad.vcf` is the downloadable contact card.
- `assets/products/`: existing product brand marks used on the card where available. Dastaan remains a plain text name because this site source has no official Dastaan logo asset.
- `visit-qr/`: spelling alias that forwards to `/vist-qr/`.
- `assets/products/`: existing product marks used where available. Dastaan is plain text because the personal-site assets do not include its official logo.
- `styles.css`: shared styles
- `assets/`: portrait, share image, favicon and self-hosted fonts (SIL OFL 1.1)
