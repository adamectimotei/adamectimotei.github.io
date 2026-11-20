# adamectimotei.github.io

A Jekyll blog for GitHub Pages, using the built-in `minima` theme. GitHub builds it, so no setup or Actions are needed.

## Put it online (one time, about 5 minutes)

1. On GitHub, create a new **public** repository named exactly `adamectimotei.github.io`. Leave "Add a README" unticked.
2. Upload everything in this folder, including the `_drafts` folder and the hidden `.gitignore`:
   - in the browser: **Add file → Upload files**, drag the files in, commit; or
   - from a terminal in this folder:
     ```bash
     git init -b main
     git add .
     git commit -m "Set up blog"
     git remote add origin https://github.com/adamectimotei/adamectimotei.github.io.git
     git push -u origin main
     ```
3. In the repo, open **Settings → Pages**. Under *Build and deployment*, set **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, and save.
4. After a minute or two the site is live at **https://adamectimotei.github.io**. The **Actions** tab shows each build.

## Publish a post

Posts in `_drafts/` are not published. To publish one:

1. Move it to `_posts/` and rename it with the publishing date in front:
   `_drafts/masking-pentest-traffic-for-ai.md` → `_posts/2026-11-24-masking-pentest-traffic-for-ai.md`
2. Commit and push. The post appears on the home page and in the RSS feed (`/feed.xml`).

Every post starts with a front matter block:

```yaml
---
layout: post
title: "Post title"
description: "One sentence, used for search results and link previews."
---
```

The rest is ordinary Markdown: headings, tables, and code blocks with a language (```` ```http ````) all work.

Moving a post from the Docs draft: in the doc, use **Export → Markdown**, paste the text under the front matter, and delete the date/author line and the LinkedIn section.

## Change the look and the details

- `_config.yml`: site title, description, and the GitHub and LinkedIn handles shown in the footer. Changes to this file need a push to take effect.
- `about.md`: the About page.
- `index.md`: the text above the post list on the home page.

## Custom domain (optional)

Buy a domain, then in **Settings → Pages → Custom domain** enter it and follow GitHub's DNS instructions. Set `url` in `_config.yml` to the new address.

## Preview on your own computer (optional)

Needs Ruby. In this folder:

```bash
bundle install
bundle exec jekyll serve --drafts
```

Then open http://localhost:4000. `--drafts` also shows the posts in `_drafts/`.

## Cross-posting

When you copy a post to dev.to, Hashnode or Medium, set its canonical URL to the post's address on this site, so search engines treat this site as the original.
