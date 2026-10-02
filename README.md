# HEAT — Project Page

Project page for **HEAT: Heterogeneous End-to-End Autonomous Driving via Trajectory-Guided World Models**
(IEEE RA-L 2026, under review).

Live site: https://heat2026.github.io/

Built from the [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template),
matching the layout of our other project pages (VIPS, VR-Drive).

## Deploying

`heat2026/heat2026.github.io` is a GitHub organization page, so the repository name matches the domain
and the site is served from the repository root.

Push the contents of this directory to `main`:

```bash
git init -b main
git add .
git commit -m "Add HEAT project page"
git remote add origin https://github.com/heat2026/heat2026.github.io.git
git push -u origin main
```

Then, in **Settings → Pages**, set the source to `main` / `/ (root)`. The site goes live at
`https://heat2026.github.io/` within a minute or two.

`.nojekyll` is already present, so GitHub Pages serves the files as-is without running Jekyll.

### Using a different name

If you pick a different organization name, update every occurrence of `heat2026.github.io` in
`index.html` (Open Graph / Twitter / JSON-LD URLs):

```bash
sed -i 's/heat2026\.github\.io/YOURNAME.github.io/g' index.html
```

## Before going public

- [x] arXiv ID `2605.19631` verified against the live arXiv listing.
- [ ] Confirm the author order and the equal-contribution / corresponding-author marks (the submitted LaTeX has the author block commented out).
- [ ] The **Code** button is a disabled "Coming Soon" chip. Once the repo is public, turn it back into a link:
      replace the `<span class="button is-normal is-rounded is-coming-soon" ...>` with
      `<a href="..." target="_blank" class="external-link button is-normal is-rounded is-dark">` and drop the
      "(Coming Soon)" suffix.
- [ ] Update the venue line in the hero once the paper is accepted.

## Layout

```
index.html                     all page content
static/css/                    bulma + template styles (unmodified)
static/js/                     carousel, slider, copy-bibtex, scroll-to-top (unmodified)
static/images/teaser.png       Fig. 1  — heterogeneous-domain motivation + trajectory-driven learning
static/images/method.png       Fig. 2  — three-stage HEAT framework
static/images/qualitative.png  qualitative planning vs. LAW on nuScenes / NAVSIM / Waymo
static/images/clusters.png     trajectory-guided behavior clusters
static/images/umap.png         UMAP of visual and action latents
static/images/attention.png    episodic memory retrieval weights
static/images/favicon*         generated lettermark icons
static/pdfs/                   drop the paper PDF here if you want to host it locally
```

All figures were rendered from the paper's source PDFs at 170 dpi and capped at 1920 px wide.

## License

Website content is licensed under
[CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/).
