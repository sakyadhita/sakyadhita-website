# Sakyadhita Web Site
[![Netlify Status](https://api.netlify.com/api/v1/badges/33b02bdb-9658-4530-9b42-55a1957cb999/deploy-status)](https://app.netlify.com/sites/sakyadhita/deploys)

This is the Sakyadhita International static web site created using [Astro](https://astro.build).

The design is based on a previous website written by
[Triton Software Engineering](https://github.com/TritonSE/SI-Website-Revamp)
which was a SERN three tier application (SQL, Express, React, Node). This version
retains the React components but all content has been extracted into Astro
content collections. The backend Express Server and SQL database is no longer
needed.

The website is hosted on Netlify and all form submissions are sent to Netlify.

## 🚀 Project Structure

Inside this repository, you'll see the following folders and files:

```text
/
├── astro.config.mjs          # Astro configuration file 
├── public/                   # Location of static assets
│   ├── assets/               # Location of static content (images, documents)
│   └── favicon.svg
├── src/
│   ├── css/                  # Location CSS files
│   │   └── index.css
│   ├── media/                # Location of dynamic assets (eg. images)
│   │   └── logo.svg
│   ├── components/           # React components
│   │   └── Slideshow.jsx
│   ├── content/              # Location of page content (Markdown and data)
│   │   └── config.ts
│   ├── layouts/              # Location of layouts for pages
│   │   └── PageLayout.astro
│   └── pages/                # Location of pages
│       └── index.astro
├── package.json
```

To create or change content, please place all static content (eg. documents,
images) in `public/content`. A content named `xx` in this directory can be
referenced from elsewhere on the website as absolute URLs beginning
with `/content` eg. `/content/xx`

`src/content` contains all the content contained in the website, eg pages,
conferences, publications, newsletters etc. as Markdown files. Content in
`public/content` can be linked from Markdown files, either within frontmatter or
as embedded links.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `pnpm install`             | Installs dependencies                            |
| `pnpm run dev`             | Starts local dev server at `localhost:3000`      |
| `pnpm run build`           | Build your production site to `./dist/`          |
| `pnpm run preview`         | Preview your build locally, before deploying     |
| `pnpm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `pnpm run astro -- --help` | Get help using the Astro CLI                     |


## Deploying

This website can be deployed on Netlify without any special requirements apart
from Netlify Forms which should be enabled.