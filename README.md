# VK1BEN Logbook

My amateur radio logbook. It's a personal blog where I keep notes on my ham radio journey from a Foundation licence in Canberra, through repeaters, antennas and Scouts radio. Built with [Astro](https://astro.build) and deployed on [Cloudflare Workers](https://developers.cloudflare.com/workers/static-assets/) as a static site.

## About the site

- Written by Benjamin Thompson (VK1BEN), based in Canberra, ACT.
- Posts cover getting on air, antenna builds and general learning notes.
- Callsign, name and location live in one place ([`src/consts.ts`](src/consts.ts)) and flow through the whole site.

## Project structure

Astro serves any `.astro` or `.md` file in `src/pages/` as a route based on its file name.

- `src/content/blog/` holds the blog posts as Markdown. `getCollection()` reads them and the frontmatter is type-checked against the schema in `src/content.config.ts`.
- `src/components/` holds the shared Astro components (header, footer, formatted dates and so on).
- `src/layouts/` holds the page layouts, including `BlogPost.astro`.
- `src/consts.ts` holds the site-wide details (callsign, name, location, title, description).
- `public/` holds static assets such as images.

## Commands

All commands are run from the root of the project, from a terminal:

| Command                           | Action                                           |
| :-------------------------------- | :----------------------------------------------- |
| `npm install`                     | Installs dependencies                            |
| `npm run dev`                     | Starts local dev server at `localhost:4321`      |
| `npm run build`                   | Build the production site to `./dist/`           |
| `npm run preview`                 | Preview the build locally, before deploying      |
| `npm run astro ...`               | Run CLI commands like `astro add`, `astro check` |
| `npm run deploy`                  | Deploy the production site to Cloudflare         |
| `npx wrangler tail`               | View real-time logs for the Worker               |

## Build, preview and deploy

The usual workflow for publishing a change:

1. **Build** the production site into `./dist/`:

   ```bash
   npm run build
   ```

2. **Preview** the built site locally through Wrangler, exactly as Cloudflare will serve it. This starts a local server at [http://localhost:4321](http://localhost:4321):

   ```bash
   npm run preview
   ```

   Open [http://localhost:4321](http://localhost:4321) in your browser to check everything looks right before going live.

3. **Deploy** to Cloudflare Workers once you're happy:

   ```bash
   npm run deploy
   ```

   The first deploy will prompt you to log in to your Cloudflare account in the browser.

For day-to-day writing, `npm run dev` also serves the site at [http://localhost:4321](http://localhost:4321) with live reload, so you don't need to rebuild after each edit.

## Learn more

Check out [the Astro documentation](https://docs.astro.build) to learn more about the framework.

## Credit

This site started from Cloudflare's Astro Blog Starter template, which is based on the lovely [Bear Blog](https://github.com/HermanMartinus/bearblog/).
