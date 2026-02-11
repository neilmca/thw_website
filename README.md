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
The workflow now also deploys the built site to GitHub Pages automatically for pushes to `main`. The Pages deployment uses the official Actions (`actions/upload-pages-artifact` + `actions/deploy-pages`) so the site will be served from the repository's Pages settings.

Notes:
- Ensure Pages is enabled in the repository settings (Repository > Settings > Pages). The Pages action will publish to the repository's Pages site using the repository permissions.
- For a custom domain, add a `CNAME` file to the repository root or configure it in the Pages settings.
# thw_website Update