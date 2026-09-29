# From Exascale CFD to Data-Driven Hemodynamics

A 15-minute general presentation (2026) of the doctoral research of **Thien-Tam Nguyen** (Ph.D. Civil Engineering, North Dakota State University; advisor Dr. Trung B. Le), prepared for a scientific audience with a background in computational physics and fluid mechanics. The deck follows a *simulate → learn* arc:

- **Opening:** career timeline and the motivation of simulating blood flow across scales.
- **Part 1 · Simulate:** *OvrFlw* (formerly AMRESSIF), an AMReX-based incompressible Navier–Stokes solver for exascale systems, including its numerical method, verification and validation (Taylor–Green vortex, lid-driven cavity vs. Ghia et al.), scaling on ALCF Aurora, and a $1024^3$, $Re = 30{,}000$ production run.
- **Part 2 · Learn:** unsupervised learning (Hankel Dynamic Mode Decomposition) on high-fidelity CFD of six patient-specific intracranial aneurysms, stratifying patients into *laminarized* vs. *transient* flows at clinical resolutions. Based on Nguyen et al., *Modal analysis of blood flows in saccular aneurysms*, Phys. Fluids 37, 011906 (2025).

The slides live in [`weekly-presentations/`](weekly-presentations/) and are built with [Slidev](https://sli.dev).

---

## Using this NDSU template written in Slidev

If you want to use this NDSU template written in Slidev, see the instructions below. Slides are written in Markdown, served as a web app, and deployed automatically on every push.

### Setup

Requires [Node.js](https://nodejs.org) (v20+) and [pnpm](https://pnpm.io).

```bash
cd weekly-presentations
pnpm install   # first time only
pnpm dev       # start dev server at localhost:3030
```

To build the static export:

```bash
pnpm build    # outputs to dist/
pnpm export   # exports to PDF (requires Playwright)
```

---

### Project structure

```
slides.md                   Global config + ordered list of src: references (index only)
pages/                      One file per section — these are the actual slides
  00a-cv.md                 Presenter CV (career timeline)
  00b-motivation.md         Motivation slide
  00c-part1-title.md        Part title slide (NDSU green title design)
  01-intro.md               Goal + roadmap
  ...
templates/                  Copy-paste starting points — never imported by slides.md
  00-opening.md
  title.md
  section-divider.md
  bullets.md
  bullets-image-right.md
  equations.md
  result-single.md
  result-comparison.md
  figure-grid.md
  two-cols-text-figure.md
  animation.md
public/
  assets/
    backgrounds/            Slide background images
    figures/                Simulation output figures and animations (add yours here)
    logos/                  Institution logos
```

---

### Adding a new slide section

1. Pick the closest template from `templates/` and copy it to `pages/`:
   ```bash
   cp templates/result-single.md pages/08-new-result.md
   ```

2. Edit the content in the new file.

3. Add a `src:` entry to `slides.md` in the right position:
   ```yaml
   ---
   src: ./pages/08-new-result.md
   ---
   ```

Numbering is manual — to insert between existing slides, rename the files to keep them in order.

To turn a slide off without deleting it, add `hide: true` to its frontmatter.

---

### Working with images and figures

Place figures in `public/assets/figures/`. Reference them in slides using `:src` (not `src`):

```html
<!-- Static figure -->
<img :src="'/assets/figures/cavity-re3200.png'" class="rounded-lg max-h-64" alt="Re=3200" />

<!-- In image-right layout frontmatter — plain string is fine here -->
image: /assets/figures/cavity-re3200.png
```

> **Rule:** Always use `:src="'/path'"` on `<img>` and `<video>` tags inside Markdown.
> Plain `src="/path"` triggers Vite's module resolver and throws an error.
> Frontmatter fields (`background:`, `image:`) are exempt — use plain strings there.

#### Replacing placeholder images

Every result slide has a `<!-- replace ... -->` comment marking the placeholder image.
Search for it to find all slides still using backgrounds as stand-ins:

```bash
grep -r "replace" pages/
```

---

### Working with animations

Use **WebM** for video animations (CFD simulations, particle traces):

```html
<video
  :src="'/assets/figures/animation.webm'"
  autoplay loop muted playsinline
  class="rounded-lg max-h-80"
/>
```

Use **animated WebP** for simple diagrams (works in `<img>` tags, auto-plays like GIF):

```html
<img :src="'/assets/figures/diagram.webp'" class="rounded-lg max-h-64" alt="Diagram" />
```

Avoid GIF for scientific content — the 256-color limit destroys scientific colormaps.

---

### Working with logos

Logos live in `public/assets/logos/`. All logos should be PNG with transparent backgrounds.
To strip a white background using ImageMagick:

```bash
magick logo.png -fuzz 8% -transparent white -trim +repage logo.png
```

In slides, use `brightness-0 invert` to force white on dark backgrounds:

```html
<img :src="'/assets/logos/NDSU.png'" class="h-8 brightness-0 invert opacity-80" alt="NDSU" />
```

For slides with variable backgrounds (light or dark), use `dark:brightness-0 dark:invert` instead.

---

### Deployment

The project is connected to your choice of hosting service. 
Every push to `main` triggers a new build automatically — no manual steps needed. 
The hosted URL always reflects the latest commit.

To deploy manually:
```bash
git add -A
git commit -m "update slides"
git push
```
