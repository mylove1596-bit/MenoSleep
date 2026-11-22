# MenoSleep public pages

Static HTML pages for the public facing documents. No build step, no framework, no tracking.

| File | Purpose |
| --- | --- |
| `index.html` | Product overview and download entry point |
| `privacy.html` | Privacy policy (App Store Connect privacy policy URL) |
| `terms.html` | Terms of service |
| `disclaimer.html` | Clinical disclaimer |
| `support.html` | Support and common questions |
| `404.html` | Not found page |
| `assets/style.css` | One shared stylesheet |

## URLs once GitHub Pages is on

```
https://mylove1596-bit.github.io/MenoSleep/
https://mylove1596-bit.github.io/MenoSleep/privacy.html
https://mylove1596-bit.github.io/MenoSleep/terms.html
https://mylove1596-bit.github.io/MenoSleep/disclaimer.html
https://mylove1596-bit.github.io/MenoSleep/support.html
```

## Enabling Pages

Settings → Pages → Build and deployment → Source: **GitHub Actions**. The workflow in
`.github/workflows/pages.yml` then publishes the repository root on every push to `main`.

## Rules for editing

- Every page keeps the same header, footer and stylesheet. One stylesheet, no inline styles.
- Policy pages carry a version number. When a policy changes, bump the version, update
  the date, and update the consent version stored in the app (currently `2026-11-22`).
- No medical claims. Use "improves sleep behaviour", "learns CBT-I techniques",
  "discuss with your doctor". Never "treats", "cures", "diagnoses".
- No analytics, no fonts, no third party scripts. The site must load offline from a
  file:// URL with no network access.
