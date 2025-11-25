# Squid Proxy Control Center

This repository hosts a Jekyll site that includes a Squid Proxy GUI mockup. The page lets you plan deployments, configure ACLs, tune caching, and export a generated `squid.conf` preview.

## Features
- Squid Proxy Control Center page with deployment, ACL, caching, SSL/TLS, logging, and telemetry controls.
- Config preview/export panel with downloadable configuration text.
- Responsive layout and status widgets styled via Sass.

## Quick start (local development)
Follow these steps exactly as written—you can copy/paste the commands.

1. **Install prerequisites**
   - Ruby 3.0 or newer (check with `ruby -v`).
   - Bundler (check with `bundle -v`; install with `gem install bundler` if missing).

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Run the site locally**
   ```bash
   bundle exec jekyll serve --livereload
   ```
   Then open the printed URL (usually `http://127.0.0.1:4000`). The Squid GUI lives at `/squid-proxy-gui.html`.

4. **Stop the server**
   - Press `Ctrl + C` in the terminal when you're done.

## Building for production
Use the build command to generate the static site in `_site/`:
```bash
bundle exec jekyll build
```
The output can be hosted on any static server.

## Deploying to GitHub Pages (step-by-step)
1. Commit your changes to the main branch of this repo.
2. Push to GitHub.
3. In the GitHub repository settings, enable GitHub Pages and select the **GitHub Actions** or **main branch /docs** option. If you use the `/docs` option, copy the contents of `_site/` into a `docs/` folder and commit.
4. Wait for the deployment to finish, then visit the published URL shown in the GitHub Pages settings.

## Project structure
- `squid-proxy-gui.html` — Squid control center UI and client-side logic.
- `_sass/_squid.scss` — Styles for the Squid page.
- `css/main.scss` — Sass manifest that imports the Squid styles.
- `Gemfile` — Ruby dependencies for building the Jekyll site.

## Troubleshooting
- **Missing dependencies**: Run `bundle install` again after updating the `Gemfile`.
- **Port already in use**: Add `--port 4001` (or another port) to the serve command.
- **Site not updating**: Restart `jekyll serve` after changing `_config.yml`.
