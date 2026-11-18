# sams-site-redo

A one-page portfolio set in a moonlit field rendered entirely in glyphs: teal grass strokes, cypress trees, shadows woven from your own bio text, and a path of `@Q08` characters. You walk a small lantern-carrying figure through the field; each glowing ring is a project, and reaching one opens its card. The path ends at a ruined stone tower built from dense glyphs and swaying moss. Its arched door opens the About card.

## Run it

It's a single static file with no build step.

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Edit your content

Everything you'd want to change lives in the `SITE` object near the bottom of `index.html`: name, role, about text, facts, email, links and projects. Each project's `at: [path, distance]` places its light beside one of the two winding paths (path `0` or `1`, distance in world units from the start, negative goes the other way).

## Controls

- Click or tap the ground to walk; click a light's label to walk to it
- Arrow keys / WASD to walk, scroll or `+`/`-` to zoom
- **work / about / contact** in the top bar open plain, accessible lists. Picking a project in **work** walks you there

The renderer lowers its glyph resolution automatically on slow machines and respects `prefers-reduced-motion`.

## Deploy

Works as-is on GitHub Pages (Settings → Pages → deploy from branch), Netlify, Vercel or any static host.
