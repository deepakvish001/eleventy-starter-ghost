# Ghostleaf

Ghostleaf is a static publishing frontend that combines Ghost as a headless content platform with Eleventy as a fast site generator. It fetches posts, pages, authors, tags, and site settings from the Ghost Content API and produces a deployable static site in `dist`.

## What it provides

- Ghost posts and pages rendered as static HTML
- Author and tag archive pages
- Featured-content ordering
- RSS feed, sitemap, robots file, redirects, and security headers
- Local and lazy-loaded images
- Inline CSS and HTML minification for production builds
- BrowserSync development server with a custom 404 response
- Netlify-ready build configuration

## Technology stack

| Area | Technology |
| --- | --- |
| Content platform | Ghost Content API |
| Static generator | Eleventy |
| Templates | Nunjucks and Markdown |
| Styling | CSS with CleanCSS minification |
| Images | Eleventy local-image and lazy-image plugins |
| Deployment | Netlify-compatible static output |

## Prerequisites

- Node.js 14 or newer for the current dependency baseline
- Yarn
- A Ghost site and Content API key

## Environment configuration

Create or update `.env` with the following values:

```dotenv
GHOST_API_URL=https://your-ghost-site.example
GHOST_CONTENT_API_KEY=replace-with-content-api-key
SITE_URL=http://localhost:8080
```

`SITE_URL` is optional and overrides the public URL returned by Ghost. Use hosting environment variables for deployed builds and avoid committing private credentials.

## Install and run

```bash
git clone <repository-url>
cd <repository-directory>
yarn install
yarn start
```

The development server builds the site from Ghost content and watches local templates for changes.

## Commands

| Command | Purpose |
| --- | --- |
| `yarn start` | Start the development workflow |
| `yarn dev` | Run Eleventy with the development environment |
| `yarn build` | Generate a production site in `dist` |
| `yarn test` | Verify that a production build completes |
| `yarn lint` | Lint JavaScript sources |

## Project structure

```text
src/_data/          Ghost site data loaders
src/_includes/      Layouts, partials, icons, and styles
src/authors/        Author archive templates
src/posts/          Post templates
src/tags/           Tag archive templates
src/transforms/     Build-time HTML transforms
.eleventy.js        API integration and Eleventy configuration
netlify.toml        Hosting configuration
```

## Deployment

Set `GHOST_API_URL`, `GHOST_CONTENT_API_KEY`, and the production `SITE_URL` in the hosting environment. The production command is `yarn build`, and the publish directory is `dist`. A Ghost deploy hook can trigger a rebuild whenever published content changes.

## Roadmap

Ghostleaf will be modernized through focused changes covering dependency upgrades, resilient API error handling, pagination, content caching, accessible navigation, responsive media, image fallbacks, metadata validation, structured data, test fixtures, template tests, security headers, preview workflows, and deployment observability.

## Contributing

Branch from `main`, keep each pull request focused, run `yarn lint` and `yarn test`, avoid committing real Ghost credentials, and document any content-model or deployment change.

## License and attribution

The project remains available under the [MIT License](LICENSE). Existing Ghost Foundation and contributor attribution is retained.