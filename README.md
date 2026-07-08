# Jubayed Ahmed — Portfolio (Randomized)

Four complete portfolio designs, one random pick per visit.

**Live:** https://jashuvo.github.io

## How it works

`index.html` is a tiny router. On every fresh visit it randomly picks one of the four designs in `/designs` and loads it via `location.replace()` — no build step, no server, works on plain GitHub Pages.

- Won't repeat the same design twice in a row in one browser tab (tracked via `sessionStorage`).
- Force a specific design by sharing a link like `?design=console.html`.

## The four designs

| File | Concept |
|---|---|
| `designs/manifest.html` | Cargo manifest — deep green & crimson, port-city theme |
| `designs/console.html` | `OPS://JUBAYED` — amber CRT terminal, live uptime counter |
| `designs/pipeline.html` | CI/CD pipeline — violet/mint, scroll-driven spine, kinetic type |
| `designs/bento.html` | Bento grid — light/dark toggle, mitchellhou.com-inspired |

All four pull from the same source data (LinkedIn career history, projects, skills) and each links to the same resume PDF at the repo root.

## Editing

Each design is a fully self-contained HTML file — no shared components. Update career/project content in **all four** files to keep them in sync. `Jubayed_Ahmed_Resume.pdf` must stay at the repo root; every design links to it as `../Jubayed_Ahmed_Resume.pdf`.

## Deploy

Push to `main` → `.github/workflows/deploy.yml` builds and deploys automatically.
One-time setup: **Settings → Pages → Source: GitHub Actions**.

## Add or remove a design from rotation

Edit the `DESIGNS` array at the top of the script in `index.html`.

---
Designed & built solo — no template, no team.
