# Monocle Society

A single static page: the white Monocle Society brand mark centered on a rich red background. No build, JavaScript, third-party fonts, analytics or dependencies.

## Preview

Run `python3 -m http.server 4173 --bind 127.0.0.1` from this directory, then open http://127.0.0.1:4173.

## Publish

GitHub Pages serves the root of `main`. Push a commit to publish.
Live site: https://monoclesociety.com/
GitHub Pages URL: https://monoclesociety.github.io/monocle-website/ (redirects to the custom domain).

## Domain configuration

Configured on 2026-11-24:

- GitHub Pages custom domain: `monoclesociety.com`; tracked in `CNAME`.
- DNS hosted at Hover (`ns1.hover.com`, `ns2.hover.com`).
- Four apex (`@`) A records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, TTL 15 minutes.
- `www` CNAME: `monoclesociety.github.io`, TTL 15 minutes.
- Existing Google mail MX and SPF TXT records preserved.
- Authoritative Hover DNS and public resolvers returned the new records. GitHub served the correct page with the custom-domain Host header.

GitHub approved the TLS certificate for both apex and www on 2026-11-24 (initial certificate expiry 2027-02-22). Enforce HTTPS is enabled in [Pages settings](https://github.com/monoclesociety/monocle-website/settings/pages). Verified apex HTTPS returns 200, HTTP redirects to HTTPS, and www HTTPS redirects to the apex with certificate validation enabled. Some resolvers may retain earlier negative DNS responses until their caches expire.

Reference: [GitHub custom-domain setup](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

## Brand provenance

`assets/monocle-society.svg` is the white vector icon from the previous website, sourced from `src/assets/images/logo_monocle_icon.svg` in the private `monoclesociety/monoclesociety.com` repository. It replaces the Canva thumbnail at the owner's request on 2026-11-24. Both the centered page logo and favicon use this SVG. The trademark lettering has been removed at the owner’s request, and the viewBox is cropped to the square circular mark so it remains centered. The red gradient is a chosen presentation color, not a verified kit palette.

Canva website reference: https://canva.link/9xebq3t1lsfs1lu
Project/evidence: https://linear.app/monoclesociety/issue/MON-34/build-and-deploy-the-monocle-society-logo-landing-page
