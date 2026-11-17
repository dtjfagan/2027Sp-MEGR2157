# MEGR 2157 – Design Portfolio Template

This repository is an MkDocs site (same engine Fab Academy uses) with the Analyze / Decide / Communicate framework built into every assignment page. The rendered site — with the left-hand navigation to every assignment — lives in `docs/`; this README is just for people working with the repo itself.


## Don't do, possible save for later. Preview locally

```bash
pip install -r requirements.txt
mkdocs serve
```
### sub header

Then open http://127.0.0.1:8000 in your browser. The sidebar nav updates automatically from `mkdocs.yml`.

## Publish

Push to `main` — the included GitHub Actions workflow (`.github/workflows/deploy.yml`) builds the site and publishes it to GitHub Pages automatically.

## Structure

```
2027Sp-MEGR2157/
├── .github/
│   └── workflows/
│       └── deploy.yml          <- GitHub Actions: auto-builds and deploys to Pages on every push
├── docs/
│   ├── index.md                <- Course homepage
│   ├── MEGR2156title.png       <- Homepage banner
│   ├── assets/images/
│   │   └── grid-bg.png         <- Isometric grid background
│   ├── stylesheets/
│   │   └── extra.css           <- Site colors (#005035 green, white text, gold links)
│   └── weeks/
│       ├── week-01-introduction/index.md
│       ├── week-02-design-for-fundamental-stresses/index.md
│       ├── week-03-parametric-design-and-fea/index.md
│       ├── week-04-bending-stress-and-stiffness/index.md
│       ├── week-05-fits/index.md
│       ├── week-06-drawings-part-1/index.md
│       ├── week-07-drawings-part-2/index.md
│       ├── week-08-midterm/index.md
│       ├── week-09-finite-element-analysis/index.md
│       ├── week-10-gears/index.md
│       ├── week-11-pulleys/index.md
│       ├── week-12-lead-screw/index.md
│       ├── week-13-motor-selection/index.md
│       ├── week-14-engineering-disasters/index.md
│       ├── week-15-awards-and-guest-speakers/index.md
│       └── final-exam/index.md
├── templates/
│   └── assignment-template.md  <- Blank assignment page for reference (not published)
├── .gitignore
├── mkdocs.yml                  <- Controls site nav (left sidebar) and theme
├── requirements.txt            <- Python dependencies for MkDocs Material
└── README.md                   <- This file
```

## Adding or renaming a page

1. Add a new folder under `docs/weeks/` (or elsewhere in `docs/`) with an `index.md`.
2. Add a matching line to the `nav:` section of `mkdocs.yml` — this is what makes it appear in the sidebar on every page.
