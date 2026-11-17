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

## GitHub Pages

Recommended repository name: `public-app-pages`. Create it as a **public** repository under the developer's GitHub account, push the `main` branch, then enable **Settings → Pages → Deploy from a branch → main → /(root)**. GitHub Pages uses HTTPS on its `github.io` domain.

After the repository is created, the K Podcast page paths will follow this pattern (replace `<github-username>` with the actual account name):

- `https://<github-username>.github.io/public-app-pages/apps/k-podcast/privacy.html`
- `https://<github-username>.github.io/public-app-pages/apps/k-podcast/support.html`

These are URL patterns, not live links. Confirm the final addresses after the repository exists, Pages is enabled, and the site is reachable. Add a custom domain only if one is already owned and configured; it is not needed for this setup.

## Publishing checklist

- Replace all `TODO` and draft contact text in the app's pages.
- Verify every privacy statement against the app build being submitted.
- Check the rendered pages in Hebrew and English, including all links.
- Ensure the repository contains no tokens, private URLs, personal information that was not intentionally made public, or unlicensed app content.
- Publish and confirm both policy and support URLs load over HTTPS before entering them in App Store Connect.

K Podcast's pages are still drafts until its public support contact is selected and the statements are rechecked against the submitted build.
