# Jinhua Deng Portfolio

Bilingual Hugo portfolio for SLAM localization and motion-control roles.

## Local development

This project uses Hugo Extended `v0.170.1`. Install that Hugo release locally, or use the project-local binary at `.tools/hugo/hugo` when it is available in the current workspace.

The Hugo Profile starting point is pinned to commit `5fc40a91d6bab447e6e8685e05bbf47f39b214dd` from October 11, 2026.

```bash
hugo server
```

Build the production site:

```bash
hugo --gc --minify --baseURL "https://siyiovo.github.io/"
```

## Content updates

- Edit Chinese pages under `content/zh-cn/`.
- Edit the matching English pages under `content/en/`.
- Add project media under `static/images/` and reference it with `/images/<file>`.
- Add `static/resume/jinhua-deng-zh.pdf` and `static/resume/jinhua-deng-en.pdf` when the résumés are ready. The links appear automatically when the files exist.

## Public project sources

The registration visualizer image is sourced from `siyiovo/pcl_registration_visualizer` at `static/images/pcl-registration-visualization.png`. Its repository credit appears in the footer. The GitHub avatar at `static/images/jinhua-deng.jpg` is sourced from `https://github.com/siyiovo.png`.

Interface icons are self-hosted from Lucide (ISC license). The GitHub mark is from Simple Icons (CC0-1.0); their license files are in `static/icons/`.

## Publishing

Push the repository's default branch and GitHub Actions will build and publish the site through GitHub Pages.
