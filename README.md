# Monocle Society

A single static page: the white Monocle Society brand mark centered on a rich red background. No build, JavaScript, third-party fonts, analytics or dependencies.

## Preview

Run `python3 -m http.server 4173 --bind 127.0.0.1` from this directory, then open http://127.0.0.1:4173.

## Publish

GitHub Pages serves the root of `main`. Push a commit to publish.
Custom domain: http://monoclesociety.com/ (HTTPS provisioning pending).
GitHub Pages URL: https://monoclesociety.github.io/monocle-website/ (redirects to the custom domain).

## Domain configuration

Configured on 2026-11-24:

- GitHub Pages custom domain: `monoclesociety.com`; tracked in `CNAME`.
- DNS hosted at Hover (`ns1.hover.com`, `ns2.hover.com`).
- Four apex (`@`) A records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, TTL 15 minutes.
- `www` CNAME: `monoclesociety.github.io`, TTL 15 minutes.
- Existing Google mail MX and SPF TXT records preserved.
- Authoritative Hover DNS and public resolvers returned the new records. GitHub served the correct page with the custom-domain Host header.

GitHub is still provisioning the custom-domain TLS certificate. Once it is ready, enable Enforce HTTPS in [Pages settings](https://github.com/monoclesociety/monocle-website/settings/pages) and verify both apex and www. Do not bypass certificate errors while provisioning is pending.

Reference: [GitHub custom-domain setup](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

## Brand provenance

`assets/monocle-society.png` is the exact 181×181 transparent logo thumbnail returned by Canva for the **Monocle Society** Brand Kit (`kAHb3lFuL_Q`) on 2026-11-24. It is displayed at or below its native CSS size. A full-resolution original can replace this file later without changing the layout. The red gradient is a chosen presentation color, not a verified kit palette.

Canva website reference: https://canva.link/9xebq3t1lsfs1lu
Project/evidence: https://linear.app/monoclesociety/issue/MON-34/build-and-deploy-the-monocle-society-logo-landing-page
