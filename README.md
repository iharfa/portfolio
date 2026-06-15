# iHarfa — Portfolio

A static portfolio site showcasing iHarfa's civic-tech, open-data, and public-interest
projects hosted on Vercel.

## Structure

```
index.html                 # the whole site (Tailwind via CDN)
images/                    # project preview screenshots + WIP placeholders
.claude/launch.json        # local preview config (npx serve on :4173)
```

## Run locally

```bash
npx serve -l 4173 .
# then open http://localhost:4173
```

## Deploy to Vercel

It's a static site — no build step.

```bash
vercel        # preview
vercel --prod # production
```

Or import the repo in the Vercel dashboard and accept the defaults (framework: "Other").

## Updating project screenshots

Card previews live in `images/`. To refresh a screenshot of a live tool:

```bash
curl -L -o images/<name>.png \
  "https://image.thum.io/get/width/1280/crop/720/wait/8/noanimate/<live-url>"
```

The two work-in-progress projects (Rannamaari Tracker, See My Island) use the
SVG placeholders in `images/`. Replace the `src` in `index.html` with a real
screenshot once each tool is live.
