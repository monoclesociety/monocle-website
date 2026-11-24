# Monocle Society

A single static page: the white Monocle Society brand mark centered on a rich red background. No build, JavaScript, third-party fonts, analytics or dependencies.

## Preview

Run `python3 -m http.server 4173 --bind 127.0.0.1` from this directory, then open http://127.0.0.1:4173.

## Publish

GitHub Pages serves the root of `main`. Push a commit to publish.
Live site: https://monoclesociety.github.io/monocle-website/

## Connect monoclesociety.com

DNS is currently hosted at Hover (`ns1.hover.com`, `ns2.hover.com`); apex A and www CNAME records were absent on 2026-11-24. The custom domain has not yet been set on Pages, so the live GitHub URL remains usable.

1. In [GitHub Pages settings](https://github.com/monoclesociety/monocle-website/settings/pages), save `monoclesociety.com` as the custom domain. GitHub creates a `CNAME` file on main; pull that commit before subsequent changes.
2. In Hover, add four A records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`.
3. Add a CNAME record for `www` pointing to `monoclesociety.github.io` (no repository path). Preserve mail and other unrelated DNS records.
4. After GitHub confirms DNS and provisions the certificate, enable Enforce HTTPS. Verify both apex and www.

Reference: [GitHub custom-domain setup](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

## Brand provenance

`assets/monocle-society.png` is the exact 181×181 transparent logo thumbnail returned by Canva for the **Monocle Society** Brand Kit (`kAHb3lFuL_Q`) on 2026-11-24. It is displayed at or below its native CSS size. A full-resolution original can replace this file later without changing the layout. The red gradient is a chosen presentation color, not a verified kit palette.

Canva website reference: https://canva.link/9xebq3t1lsfs1lu
Project/evidence: https://linear.app/monoclesociety/issue/MON-34/build-and-deploy-the-monocle-society-logo-landing-page
