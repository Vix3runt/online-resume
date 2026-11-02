<h1 align="center">online-resume</h1>

<p align="center">
  <a href="https://github.com/tarrex/online-resume/blob/main/LICENSE"><img src="https://img.shields.io/github/license/tarrex/online-resume?style=flat-square" alt="GitHub License"></a>
  <a href="https://github.com/tarrex/online-resume/forks"><img src="https://img.shields.io/github/forks/tarrex/online-resume?style=flat-square" alt="GitHub forks"></a>
  <a href="https://github.com/tarrex/online-resume/stargazers"><img src="https://img.shields.io/github/stars/tarrex/online-resume?style=flat-square" alt="GitHub stars"></a>
  <a href="https://tarrex.github.io/online-resume"><img src="https://img.shields.io/website?style=flat-square&url=https%3A%2F%2Ftarrex.github.io%2Fonline-resume" alt="Demo website"></a>
</p>

<h4 align="center">A minimalist Jekyll theme for online, print, and PDF resumes.</h4>

## Features

- Resume content managed in YAML with Markdown support.
- Modular and configurable resume sections.
- Responsive and print-friendly layouts for web and PDF.
- Multilingual support with language-specific fonts.
- Optional math rendering with KaTeX or MathJax.
- Customizable theme colors, fonts, and styles.
- Privacy mode and search-engine indexing controls.
- Easy deployment to GitHub Pages and other static hosting platforms.


## Requirements

- Jekyll `4.4.1`.
- Ruby `2.7` or later; Ruby `3.4` is used by the deployment workflow.
- Bundler, or the `jekyll/jekyll:latest` Docker image.

The resolved Jekyll and gem versions are committed in `Gemfile.lock`. The Docker tag is only a runtime environment; the lockfile is the reproducible dependency contract.

## Create your resume

Fork or copy this repository, then edit:

- `_data/data.yml`: resume content.
- `images/profile.png`: profile image.
- `_config.yml`: languages, fonts, integrations, and theme settings.
- `assets/css/custom.css`: optional style overrides.

Preview with Docker:

```bash
docker run --rm --volume "$PWD:/srv/jekyll" --publish 4000:4000 \
  jekyll/jekyll:latest \
  bundle exec jekyll serve --host 0.0.0.0 --livereload
```

Open <http://localhost:4000/>.

## Resume data

Edit `_data/data.yml` to update your profile, contact details, and resume sections. Use `show` to enable a section, `order` to position it, and `summary` for Markdown content. Empty optional values are not displayed. The comments in the data file document the available fields and contact formats.

## Configuration

The main settings in `_config.yml` are:

- `url` and `baseurl` for the deployed site address;
- `private` and `message`;
- `allow_indexing` and `show_theme_credit`;
- `theme_color`;
- `default_language` and `languages`;
- `math` and `features.math`;
- `analytics.umami`, `analytics.google`, and `analytics.cloudflare`.

Analytics are emitted only in a production build and remain disabled by default. Math rendering supports `katex` and `mathjax`; keep the configured CDN version pinned.

## Multiple languages

`index.html` selects its resume data and language through front matter. To add another language, create a root-level page such as `zh.html`:

```yaml
---
layout: default
data: data
lang: zh
---
```

This reuses `_data/data.yml` with the `zh` locale, font, direction, and date settings from `_config.yml` and `_data/i18n.yml`.

For independently translated content, copy the data file:

```bash
cp _data/data.yml _data/data_zh.yml
```

Then change the page's `data` value:

```yaml
data: data_zh
```

Add the corresponding locale, direction, and font settings under `languages` in `_config.yml`. Use `direction: rtl` for a right-to-left language.

## Deploy to GitHub Pages

The repository includes `.github/workflows/jekyll.yml`. In the repository's Pages settings, choose **GitHub Actions** as the publishing source. Pushes to `main` build with the locked Jekyll version and deploy the generated artifact; pull requests build without deploying.

The workflow uses the Pages-provided base path, so project sites such as `https://USERNAME.github.io/online-resume/` resolve assets correctly.

## Related theme

- [Hugo edition](https://github.com/tarrex/hugo-theme-online-resume)
