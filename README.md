# Phu Quoc, nine nights

A one-page trip app for our family trip to Phu Quoc, 15 to 24 August 2026.
Built for phones. Three tabs: **Trip**, **Map**, **Days**.

Static site, no build step and no dependencies. Vercel serves `index.html` as-is.

## What is in here

```
index.html            the whole app, about 58 KB
fonts/                Outfit and Plus Jakarta Sans, subset to the glyphs used
img/                  photos (WebP) and the four circular map thumbnails
icons/                home-screen icons
manifest.webmanifest  lets it install to the home screen
vercel.json           long cache on assets, noindex on everything
```

## Editing

Everything lives in `index.html`. Trip content is two arrays near the bottom
of the `<script>` block:

- `STAYS` is the four hotels, each with its photo, location note and halal note.
- `DAYS` is the ten calendar days, each with a list of timed items.

Change those and the Trip, Map and Days tabs all update, because every view
renders from the same two arrays.

The island outline and the route are inline SVG paths in the Map section.
The outline is real: it comes from the OpenStreetMap coastline for Phu Quoc,
simplified to 168 points. The route line is schematic, and the four stop
markers sit slightly offshore with a hairline back to the true position so
that the two close pairs stay separately tappable.

## Credits

Island outline from OpenStreetMap contributors, ODbL.
Photos from Wikimedia Commons, CC BY-SA 4.0: Kiss Bridge, An Thoi harbour,
Hon Thom cable car and Kiss of the Sea by Vivu Vietnam; Grand World by
Matsuoka Akiyoshi; Vinpearl Safari by Khoitran1957; Sao Beach by Trantuonglam.

## Note

This page names our family and lists the dates we are away. It is set to
noindex, but anyone with the link can read it. Keep the link private.
