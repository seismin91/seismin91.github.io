# Sumin Kim — Personal Website

[Visit the site](https://seismin91.github.io) · [Chirpy documentation](https://chirpy.cotes.page/posts/getting-started/)

An English-language personal website built with Jekyll and Chirpy 7.6.0.

## Structure

- **Profile & Research**: About & CV (`/about/`) includes a biography, experience, education, and research interests. Publications (`/publications/`) lists journal articles and conference contributions by year.
- **Notes & Projects**: Blog (`/blog/`) and Projects (`/projects/`) provide separate spaces for personal work. Categories, tags, and archives are accessible from the blog.
- **Home**: A profile summary, links to both areas, two recent publications, and the three latest posts.

The public Google Scholar profile supplied by the site owner was checked on 2026-10-04. The bibliography contains 15 journal articles and 9 conference contributions. Education and earlier positions remain unfilled until supplied. Citation counts are not displayed, and there is no automatic Scholar synchronization.

For the DAS article, the official English title, authors, and page range come from the [publisher record](https://journal.seg.or.kr/articles/article/P2bz/). Its page range is 214–226; the imported Scholar record had 214–216.

## Update your information

| Content | File |
| --- | --- |
| Site title, description, social name, and public email | `_config.yml` |
| Biography, affiliation, experience, education, and interests | `_data/profile.yml` |
| Publication list | `_data/publications.json` |
| Homepage introduction and navigation | `_includes/portfolio-intro.html` |
| Profile sections | `_includes/profile.html` |
| Projects | `_tabs/projects.md` |
| Blog listing | `_tabs/blog.html` |
| Sidebar groups and links | `_data/navigation.yml` |
| Social links | `_data/contact.yml` |
| Additional styles | `assets/css/portfolio.css` |
| Site-wide typeface | `assets/css/jekyll-theme-chirpy.scss` |
| Avatar | `assets/img/avatar.svg` |

To add degrees, replace `education: []` in `_data/profile.yml` with entries containing `degree`, `institution`, `field`, and `period`. Add earlier positions to `experience` using `role`, `organization`, and `period`. Only add verified details intended for public display.

## Write a post

Create `_posts/YYYY-MM-DD-title.md` with front matter like this, using the actual publication date:

```yaml
---
title: Your post title
date: 2026-10-04 18:00:00 +0900
categories: [Notes]
tags: [learning]
description: A short summary of the post.
---
```

Write the body in Markdown below the front matter. Set `pin: true` to place a post at the top of the blog listing. Home shows the three latest posts; the blog shows all posts without pagination. `hidden: true` removes a post from these lists but does not make it private. An empty state is displayed when there are no posts.

## Preview locally

Use Ruby 3.4 and Bundler:

```sh
bundle install
bundle exec jekyll serve
```

Open `http://127.0.0.1:4000`.

## Deployment

GitHub Pages uses **Settings → Pages → Build and deployment → Source → GitHub Actions**. A push to `main` triggers the build, internal link checks, and deployment in `.github/workflows/pages-deploy.yml`.

The site URL is `https://seismin91.github.io` with an empty `baseurl`. Comments, analytics, and PWA caching are disabled. The original repository history is preserved.

Site text uses Helvetica, with Arial and the browser's sans-serif font as fallbacks. The font uses the visitor's installed typefaces. Icon fonts and monospaced code formatting retain their specialized fonts.

## Theme updates

The theme is pinned to 7.6.0 in `Gemfile`. Compare changes to the official Starter before updating, especially the overridden `_layouts/home.html`, `_includes/sidebar.html`, `_includes/head.html`, `_data/locales/en.yml`, and `assets/css/jekyll-theme-chirpy.scss`.

## Credits

- [Chirpy Starter](https://github.com/cotes2020/chirpy-starter)
- [Chirpy Theme](https://github.com/cotes2020/jekyll-theme-chirpy)
- Theme license: MIT (`LICENSE`)
