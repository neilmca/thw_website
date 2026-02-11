This repository contains a minimal Jekyll "Hello World" site.

How to run locally (macOS, zsh):

1. Install bundler and gems:

```shell
# install bundler if you don't have it
gem install bundler
bundle install
```

2. Build and serve the site locally:

```shell
bundle exec jekyll serve
```

3. Open http://127.0.0.1:4000 in your browser.

Files added:
- `Gemfile` — pins Jekyll dependency
- `_config.yml` — site config
- `_layouts/default.html` — base layout
- `index.md` — home page
- `assets/main.css` — simple stylesheet
- `.gitignore` — ignores build artifacts
 
CI
--
This repository includes a GitHub Actions workflow at `.github/workflows/jekyll-build.yml` that builds the site on pushes and pull requests to `main`. The generated `_site` directory is uploaded as an artifact named `jekyll-site` for each workflow run.

GitHub Pages
--
The workflow now deploys the built site to GitHub Pages automatically for pushes to `main` by publishing the generated `_site` directory to a `gh-pages` branch (via `peaceiris/actions-gh-pages@v3`).

Notes:
- In the repository Settings > Pages, set the source to the `gh-pages` branch (the action publishes to that branch). Allow a minute or two after the action completes for Pages to become available.
- For a custom domain, add a `CNAME` file to the repository root (it will be published to `gh-pages`) or configure it in the Pages settings.
# thw_website Update