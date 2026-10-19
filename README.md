# asanaly.beishenov.com

Static copy of the portfolio of artist Бейшенов Асаналы (https://asanaly.beishenov.com),
originally built on Adobe Portfolio. Plain HTML/CSS/JS plus all images — no build step.

## Structure

```
index.html                     Home (list of galleries)
gallery/index.html             Alias of the home page
knmii/                         Kyrgyz National Museum of Fine Arts collection
personal/                      Private collection
the-state-tretyakov-gallery/   State Tretyakov Gallery
o-khudozhnike/                 About the artist
contact/                       Contact form (opens visitor's mail client)
assets/css/                    Adobe Portfolio base + per-page theme CSS, site.css additions
assets/js/site.js              Minimal runtime: nav, photo grids, lightbox, contact form
assets/img/                    All images (every responsive variant)
```

All URLs are relative — double-click `index.html` to view locally, or deploy the folder
as-is to GitHub Pages / any static host.

## Regenerating

The mirror script and runtime source live in the sibling repo
[beishenov/beishenov.com](https://github.com/beishenov/beishenov.com):

```sh
cd ../beishenov.com
python3 scripts/mirror.py https://asanaly.beishenov.com ../asanaly.beishenov.com
```

## Notes

- Fonts load from Adobe Typekit, restricted to `asanaly.beishenov.com`; other hosts fall
  back to system fonts.
- The contact form has no backend; it composes an email to the address on the contact page.
