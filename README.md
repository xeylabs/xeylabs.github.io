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
index.html            landing page (EN — default)
id|zh|ja|kr/          terjemahan lengkap landing (5 bahasa: ID/EN/中文/日本語/한국어)
blog/index.html       the log — blog biasa (entry index)
blog/hello-lab.html   post 001 ("Hello, lab.")
blog/build-in-public.html  post 002 ("Why we build in public")
projects/index.html   indeks proyek
projects/log/index.html    build log — blog khusus proyek (terpisah dari the log)
projects/mythic/      halaman detail proyek Mythic (+ build log per proyek)
feed.xml              RSS The Log (blog biasa) · projects/feed.xml = RSS Build Log
privacy.html          privacy notice (+ /{lang}/privacy.html)
assets/style.css      shared stylesheet (design system)
sitemap.xml + robots.txt  untuk SEO
LICENSE               MIT
```

**Menambah post blog biasa:** copy `blog/hello-lab.html`, ubah konten + judul, terus tambahin satu baris `<a class="trow">` di `index.html` (section `#log`) dan `blog/index.html`. Jangan lupa tambahin `<item>` di `feed.xml` dan `<url>` di `sitemap.xml`.

**Menambah entri build log proyek:** post-nya hidup di `projects/<nama>/` (5 bahasa, slug sama). Tambahin baris `<a class="trow">` di halaman detail proyek (section build log) dan di `projects/log/index.html`, lalu `<item>` di `projects/feed.xml` dan `<url>` di `sitemap.xml`. Post proyek tidak pernah masuk `blog/` atau `feed.xml` — itu khusus blog biasa.

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
