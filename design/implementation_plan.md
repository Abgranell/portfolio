# Incremental Implementation Plan: Arnau Boix Granell Portfolio Upgrade
*Zero-Breaking Static HTML/CSS Rollout Architecture*
*Author: UX/UI Designer & Senior Frontend Developer*

---

## 1. Executive Summary & Rollout Strategy

### Directives:
1. **Preserve Static Architecture:** Zero migration to React, Next.js, or external frameworks. The portfolio remains 100% compatible with GitHub Pages static hosting.
2. **Preserve Relative Asset Paths:** All existing assets (`imatges/*`, `giff/*`) and folder structures (`cat/`, `eng/`, `css/`) remain completely intact.
3. **Bilingual Parity:** Every modification in English is synchronously executed in Catalan.
4. **Zero Downtime & Reversible Checkpoints:** Each phase represents an atomic Git commit with automated regression checks.

---

## 2. File-by-File Modification Matrix

| Phase | Target File(s) | Key Actions & Enhancements | Reversibility Checkpoint |
| :---: | :--- | :--- | :--- |
| **Phase A** | `css/styles.css` | Unify color palette (resolve khaki vs sky blue bug), eliminate body flex anti-pattern, centralize card, tag, grid, navigation, carousel, and video classes. | `checkpoint-phase-A-css` |
| **Phase B** | `index.html`<br>`cat/wip.html`<br>`eng/wip.html` | Polish landing splash card, typography, and button styling. Create `eng/wip.html` to eliminate 404 easter egg bug. | `checkpoint-phase-B-splash` |
| **Phase C** | `cat/main-cat.html`<br>`eng/main-eng.html` | Transform Homepage: Sticky navigation, modern Hero, 4 Core Impact Pillars, Flagship Project Spotlight, verified About Me, structured Experience & Education timelines with thesis handles. | `checkpoint-phase-C-homepage` |
| **Phase D** | `cat/projectes-professionals-cat.html`<br>`eng/projectes-professionals-eng.html` | Reorder projects: COGNITIUM (TIAGo VLA @ MWC 2026), PRISM reference, GRAIL (correct title & 40M€ scope), INTELLIMAN. Integrate categorized tags, carousels with bullets, and video embeds. | `checkpoint-phase-D-pro-projects` |
| **Phase E** | `cat/articles-cat.html`<br>`eng/articles-eng.html` | Lead with PRISM (ERF 2026 / arXiv:2603.05574). Fix critical publication link swap between Article 2 (ICRA 2023) and Article 3 (CCIA 2022). Correct co-author name (Alberto San-Miguel-Tello). | `checkpoint-phase-E-publications` |
| **Phase F** | `cat/projectes-academics-cat.html`<br>`eng/projectes-academics-eng.html` | Fix TFM factual error ("treball de fi de grau" -> "treball de fi de màster"). Feature AIxHRI Summer School, Engihack 1st Prize, and TFG VR manipulation. Implement bullet carousels. | `checkpoint-phase-F-acad-projects` |
| **Phase G** | `cat/altres-cat.html`<br>`eng/altres-eng.html` | Fix critical broken language link in `eng/altres-eng.html` (`altres-cat.html` -> `../cat/altres-cat.html`). Reframe page as "Community, Leadership & Initiatives". Elevate euRobotics DII and remove placeholder alt text. | `checkpoint-phase-G-community` |
| **Phase H** | `cat/plantilla-cat.html` | Archive or deprecate `cat/plantilla-cat.html` to prevent indexing of unfinished TODO placeholders. Run full repo link verification. | `checkpoint-phase-H-cleanup` |

---

## 3. Detailed Execution Phases

### Phase A: Core Stylesheet & Component Architecture (`css/styles.css`)
- **Action Items:**
  1. Define `:root` variables: `--bg-canvas`, `--bg-card`, `--text-primary`, `--text-secondary`, `--text-muted`, `--border-subtle`, `--accent-primary`, `--accent-hover`, and semantic tag colors (`--tag-hw-*`, `--tag-sw-*`, `--tag-ai-*`, `--tag-metric-*`).
  2. Normalize `body` to standard flow (`display: block; margin: 0; padding: 0;`).
  3. Define reusable component styles:
     - `.site-header`, `.nav-container`, `.nav-logo`, `.nav-links`, `.nav-lang-btn`.
     - `.impact-grid`, `.impact-card`, `.impact-metric`, `.impact-label`.
     - `.spotlight-grid`, `.spotlight-card`.
     - `.case-study-card`, `.case-study-header`, `.badge`.
     - `.tag-pill`, `.tag-pill-hw`, `.tag-pill-sw`, `.tag-pill-ai`, `.tag-pill-metric`.
     - `.video-wrapper`, `.carousel-container`, `.carousel-slide`, `.carousel-btn`, `.carousel-dots`, `.dot`.
  4. Write the upgraded touch-enabled vanilla JS carousel helper (~40 lines) to be embedded or linked.

### Phase B: Landing Splash & WIP Easter Egg (`index.html`, `cat/wip.html`, `eng/wip.html`)
- **Action Items:**
  1. In `index.html`, wrap content in `.centered-layout`. Elevate avatar styling with subtle border and shadow. Refine language buttons with modern hover animations.
  2. In `cat/wip.html`, update styling to match the new color tokens while preserving the dancing pug GIF.
  3. Create `eng/wip.html` mirroring `cat/wip.html` in English ("Work in Progress - Currently updating this section. Please check back soon!") to prevent 404 errors when clicking the secret button on English pages.

### Phase C: Homepage Transformation (`cat/main-cat.html`, `eng/main-eng.html`)
- **Action Items:**
  1. Add sticky top navigation bar with bilingual switch and LinkedIn button.
  2. Implement Hero Header: Profile image, full name, professional headline (*"Robotics Researcher | Learning-Based Manipulation, Vision-Language-Action (VLA) Models & Sim2Real Transfer"*), and Eurecat affiliation badge.
  3. Implement the **4 Core Impact Pillars** grid.
  4. Implement the **Flagship Project Spotlight** (COGNITIUM, PRISM, GRAIL) with direct navigation buttons.
  5. Replace existing text in "Sobre mi / About Me" with verified, high-impact narrative from `content/about_me.md`.
  6. Update "Experiència Professional / Professional Experience" with detailed contributions from `content/experience.md`.
  7. Update "Estudis / Education" with class rank (2nd/298), 35 honors, and formal UPCommons thesis links.

### Phase D: Professional Projects (`cat/projectes-professionals-cat.html`, `eng/projectes-professionals-eng.html`)
- **Action Items:**
  1. Replace custom inline style blocks with centralized classes from `css/styles.css`.
  2. Project 1: **COGNITIUM** — Feature PAL Robotics TIAGo PRO, Hugging Face LeRobot, MWC 2026 live demo, looping GIF, photo carousel, and YouTube video embed.
  3. Project 2: **PRISM** — Highlight as lead-author publication milestone (cross-referenced with `articles-*.html`).
  4. Project 3: **GRAIL** — Correct title to *"Generative Robotics & AI for EU Industrial Leadership"*, emphasize €40M Horizon Europe flagship status and ~20 consortium partners (Siemens, ETH Zurich, DLR).
  5. Project 4: **INTELLIMAN** — Detail Franka Emika Panda Sim2Real manipulation in Isaac Lab, dishwasher door manipulation, and demonstration GIF.
  6. Upgrade all carousels to support dot pagination and touch swipe.

### Phase E: Publications & Scientific Dissemination (`cat/articles-cat.html`, `eng/articles-eng.html`)
- **Action Items:**
  1. Article 1: **PRISM (ERF 2026 / arXiv:2603.05574)** — Feature as lead article. Include architectural diagram (`imatges/Article3.svg`), empirical benchmarks (21.2% -> 98.0%), full author list (Alberto San-Miguel-Tello), and YouTube video demonstration embed.
  2. Article 2: **ICRA 2023** — Cloth Manipulation with Automatic Semantic Labelling. Link directly to IEEE Xplore document `10161122` (`10.1109/ICRA48891.2023.10161122`) and DIGITAL.CSIC.
  3. Article 3: **CCIA 2022** — Garment Manipulation Dataset. **Fix link error:** Remove incorrect ICRA 2023 IEEE link and replace with verified IOS Press DOI (`10.3233/FAIA220334`) and DIGITAL.CSIC handle (`10261/281403`).

### Phase F: Academic Projects & Theses (`cat/projectes-academics-cat.html`, `eng/projectes-academics-eng.html`)
- **Action Items:**
  1. Project 1: **Master's Thesis (TFM)** — **Fix factual error in Catalan:** Change "treball de fi de grau" to "treball de fi de màster". Highlight grade 10/10 with Honors, Isaac Lab GPU physics, Franka Panda ROS 2 hardware bridge, and UPCommons handle `2117/428855`.
  2. Project 2: **AIxHRI Summer School** — Inria / Loria (Nancy, France) advanced doctoral training in VLAs and RLHF.
  3. Project 3: **Engihack 2024** — 1st Prize Winner (€3,000, InduBotics team, TV3 broadcast), EcoShower mechatronic bypass system, and photo carousel.
  4. Project 4: **Bachelor's Thesis (TFG)** — IRI CSIC-UPC VR cloth manipulation framework, HTC Vive Pro, Stereolabs ZED 2i, Leap Motion tracking, and UPCommons handle `2117/372083`.

### Phase G: Community, Leadership & Initiatives (`cat/altres-cat.html`, `eng/altres-eng.html`)
- **Action Items:**
  1. **Fix Critical Bug in `eng/altres-eng.html`:** Change broken relative link from `<a href="altres-cat.html">` to `<a href="../cat/altres-cat.html">`.
  2. Elevate page title and tone from colloquial "Popurri" to **"Community, Leadership & Professional Initiatives"** (*"Comunitat, Lideratge i Iniciatives"*).
  3. Feature **euRobotics Diversity and Inclusion Initiative (DII)**, detailing active contributions to European Robotics Forum workshops and ethical robotics guidelines.
  4. Fix image alt placeholder: Replace `alt="TODO: NOM FOTO"` with `alt="euRobotics Diversity and Inclusion Initiative Logo"`.

### Phase H: Repository Hygiene & Template Deprecation (`cat/plantilla-cat.html`)
- **Action Items:**
  1. Deprecate `cat/plantilla-cat.html` (add `<meta name="robots" content="noindex, nofollow">` or archive) to eliminate raw TODO placeholders from public search engines.
  2. Execute a local link checker script across all HTML files to ensure 0 broken links, 0 missing assets, and 100% bilingual parity.

---

## 4. Risk Mitigation & Verification Matrix

| Potential Risk | Impact | Mitigation Strategy |
| :--- | :---: | :--- |
| **CSS Regression on Subpages** | Medium | Normalize global body while ensuring subpage wrappers utilize unified `.container` and `.case-study-card` classes. Test every page across mobile (375px), tablet (768px), and desktop (1440px). |
| **Broken Relative Paths** | High | All assets must use strict relative paths (`../imatges/`, `../css/` from subdirectories; `imatges/`, `css/` from root). Run automated regex validation. |
| **Carousel Touch Conflicts** | Low | Carousel touch event listeners use passive event handling and a minimum delta threshold (50px) to prevent vertical scroll blocking. |
| **Bilingual Divergence** | High | Every copy edit is mirrored between English and Catalan before Git commit. Glossaries validated against `analysis/technical_reviews/technical_assessment.md`. |
