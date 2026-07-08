# McDonald Group website

This is the source for mcdonaldgrouphealth.com / mcdonaldgroupllc.com. It's a static site built with [Eleventy](https://www.11ty.dev/), with a [Decap CMS](https://decapcms.org/) admin panel at `/admin` for managing blog posts and videos.

## Structure

- `src/*.html` — the core pages (Home, Medicare, Health, Life, Contact, legal pages). Edit these directly and redeploy if you need design/content changes beyond blog/video posts.
- `src/content/blog/*.md` — blog posts (managed via `/admin`, or edit directly).
- `src/content/videos/*.yml` — video entries with a YouTube link each (managed via `/admin`, or edit directly).
- `src/admin/` — the Decap CMS admin app. Do not edit unless you're changing what fields are editable (see `config.yml`).
- `src/_includes/base.njk` — shared header/nav/footer for the blog and videos pages.
- `styles.css` — all site styling.

## Local preview (optional, requires Node.js)

```
npm install
npm run serve
```

## Editing content day-to-day

Go to `yourdomain.com/admin`, log in, and use the "Blog Posts" or "Videos" sections. See `CMS-SETUP-GUIDE.md` for one-time setup instructions to enable this login.

## Deploying

Netlify rebuilds the site automatically from this repository every time changes are pushed (including changes made through `/admin`, which commits directly to this repo).
