# paveyranne-amaury.github.io

Personal website built with [Quarto](https://quarto.org), deployed on GitHub Pages.

## Structure
- English (default) at the root; other languages under `/<code>/`.
- A page and its translations share the same path: `posts/foo/` ⇄ `fr/posts/foo/`.
- `lang-switch.html`: language switcher, navbar localisation and translated strings (`I18N`).

## Adding a post
Create `posts/<slug>/index.qmd`, then its translation at `fr/posts/<slug>/index.qmd` (same slug).

## Adding a language (example: Spanish, `es`)
1. Create `es/_metadata.yml` (`lang: es`), `es/index.qmd`, `es/about.qmd`
   and `es/posts/_metadata.yml`.
2. In `lang-switch.html`: add `"es"` to `LANGS` and an `es` entry to `I18N`.
3. In `_quarto.yml`: add `- text: "Español"` / `href: "#lang=es"` to the language menu.