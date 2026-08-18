# Project Lighthouse

Minimal GitHub Pages site for Project Lighthouse.

## Publish on GitHub Pages

1. Create a new GitHub repository.
2. Copy all files from this folder into the repository.
3. Push to the `main` branch.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, select **Deploy from a branch**.
6. Choose `main` and `/ (root)`.
7. Save.

If the repository is named `<your-github-username>.github.io`, the site becomes your main GitHub Pages site.

If the repository is named `project-lighthouse`, it will normally be served as a project site under your GitHub Pages domain.

## Add a research post

Create a Markdown file inside `_posts` using this filename format:

`YYYY-MM-DD-title-of-post.md`

Example:

```markdown
---
layout: post
title: "Reviewing an Exposed Service Safely"
date: 2026-08-20
category: Research
summary: A short description that appears on the homepage.
---

Write your article here.
```

Commit the file and GitHub Pages will rebuild the site automatically.

## Customise

Update:
- `_config.yml` for the site title and description.
- `about.md` for project information and contact details.
- `assets/css/style.css` for visual styling.

The site intentionally uses no JavaScript, analytics, third-party fonts or external dependencies.


## Included visual assets

- `assets/images/lighthouse-hero.jpg` — homepage hero image
- `assets/images/og-image.jpg` — social/Open Graph preview image
- `assets/images/logo-lighthouse.svg` — logo mark
- `assets/images/favicon.svg` — browser favicon
- `assets/icons/` — section and operating-principle icons

Footer contact: `security@project-lighthouse.my`.
