# XEY Labs — Landing Page

Official landing page for **XEY Labs**, hosted on GitHub Pages.

Built from the [UI/UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) design system:

- **Style:** Loud minimal / bold editorial — oversized type, hairline grid, rows instead of cards
- **Colors:** paper `#F4F3EE` · ink `#101210` · single acid accent `#C6F531`
- **Type:** Archivo 900 (display) · IBM Plex Mono (labels & meta)
- **Motion:** 350ms subtle reveal + marquee ticker, `prefers-reduced-motion` respected

Zero dependencies — static HTML + one shared stylesheet, no build step.

## Structure

```
index.html            landing page
blog/index.html       the log — entry index
blog/hello-lab.html   first post ("Hello, lab.")
assets/style.css      shared stylesheet (design system)
```

**Menambah post baru:** copy `blog/hello-lab.html`, ubah konten + judul, terus tambahin satu baris `<a class="trow">` di `index.html` (section `#log`) dan `blog/index.html`. Jangan lupa tambahin `<item>` di `feed.xml` dan `<url>` di `sitemap.xml`.

## Edit me

Open `index.html` and search for `TODO`:

- GitHub org URLs (`https://github.com/xeylabs`)
- Contact email
- Placeholder project cards ("Coming soon")

## Run locally

```bash
python -m http.server 8471
# open http://localhost:8471
```

## Deploy

Pushed to the `xeylabs.github.io` repository and served automatically by GitHub Pages.
