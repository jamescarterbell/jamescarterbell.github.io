# James Bell's blog

A [Zola](https://www.getzola.org/) blog using the
[Linkita](https://github.com/salif/linkita) theme and GitHub Pages.

## Local development

Install **Zola 0.23.6**, the version used by the deployment workflow.
On Windows, Zola is available through `winget install --id getzola.zola --exact`.

After cloning the repository, initialize the theme and start the preview:

```powershell
git submodule update --init --recursive
zola serve
```

Open <http://127.0.0.1:1111>. Zola reloads the site when content changes.

## Writing

Add Markdown files under `content\blog\`, for example
`content\blog\my-next-post.md`:

```toml
+++
title = "My next post"
date = 2026-11-11
description = "A short summary."

[taxonomies]
tags = ["notes"]
+++

Write your post here.
```

Add `draft = true` before `[taxonomies]` to keep a post unpublished.
Preview drafts with `zola serve --drafts`.

Edit `content\about\_index.md` for the About page and `zola.toml` for the site title,
description, profile, and navigation.

## Publish on GitHub Pages

1. Create an empty public GitHub repository. Use `jamescarterbell` for a project
   site, or `jamescarterbell.github.io` for your account's root site. Do not
   initialize the remote with a README, license, or gitignore.
2. In the repository's **Settings > Pages**, choose **GitHub Actions** as the
   source.
3. Set `base_url` in `zola.toml` to the published URL:
   `https://jamescarterbell.github.io/jamescarterbell` for the project site, or
   `https://jamescarterbell.github.io` for the root site. The workflow obtains the
   actual Pages URL automatically, including any project path or custom domain.
4. Commit and push this folder, replacing `REPOSITORY` below with the chosen
   repository name:

```powershell
git add .
git commit -m "Set up Zola blog with Linkita"
git remote add origin https://github.com/jamescarterbell/REPOSITORY.git
git push -u origin main
```

Every push to `main` builds and deploys the site. Deployment can also be started
manually from **Actions > Deploy Zola to GitHub Pages > Run workflow**.
No personal access token or `gh-pages` branch is needed.

## Checks and theme updates

```powershell
zola check --skip-external-links
zola build
```

The theme is pinned to a Git submodule commit. To update it:

```powershell
git submodule update --remote themes/linkita
zola check --skip-external-links
zola build
git add themes/linkita
git commit -m "Update Linkita theme"
```

Review the theme's changelog before updating. If a newer release requires a
newer Zola version, update both your local installation and `zola_version` in
`.github\workflows\pages.yml`.
