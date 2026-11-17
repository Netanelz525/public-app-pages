# Public App Pages

Shared, static pages for public app information such as privacy policies and support pages. Each app lives in its own directory so multiple projects can use one small public repository without sharing app source code or private content.

## Layout

```text
apps/
  k-podcast/
    privacy.html
    support.html
  _template/
    privacy.html
    support.html
index.html
```

Copy `apps/_template/` to `apps/<app-slug>/`, then replace every `TODO` before publishing. Keep contact details and policy text specific to that app. Do not put secrets, private feed URLs, user data, credentials, or internal server addresses here: all files in this repository and the published site are public.

## Repository and GitHub Pages

The public repository is [Netanelz525/public-app-pages](https://github.com/Netanelz525/public-app-pages); the `main` branch is pushed. K Podcast's public support contact has been added. Enable **Settings → Pages → Deploy from a branch → main → /(root)** after reviewing the app-specific pages. The generic files in `apps/_template/` intentionally contain `TODO` markers and must be replaced when copied for another app. GitHub Pages uses HTTPS on its `github.io` domain.

After Pages is enabled and the site is reachable, the K Podcast page URLs are expected to be:

- `https://netanelz525.github.io/public-app-pages/apps/k-podcast/privacy.html`
- `https://netanelz525.github.io/public-app-pages/apps/k-podcast/support.html`

These addresses are not live until Pages is enabled and GitHub finishes deploying. Confirm both load over HTTPS before using them in App Store Connect. A custom domain is optional.

## Publishing checklist

- Replace all `TODO` and draft contact text in the app's pages.
- Verify every privacy statement against the app build being submitted.
- Check the rendered pages in Hebrew and English, including all links.
- Ensure the repository contains no tokens, private URLs, personal information that was not intentionally made public, or unlicensed app content.
- Publish and confirm both policy and support URLs load over HTTPS before entering them in App Store Connect.

K Podcast's pages include the selected public support contact. Recheck all privacy statements against the submitted build before entering the live URLs in App Store Connect.
