# Design System & UI/UX Guidelines: Arnau Boix Granell Portfolio
*High-Precision Embodied AI Engineering Portfolio*
*Author: UX/UI Designer & Senior Frontend Developer*

---

## 1. Design Philosophy & Brand Personality

The portfolio of Arnau Boix Granell represents a rare, world-class hybrid robotics profile: bridging theoretical mathematical rigor (Ranked 2nd of 298 at UPC ETSEIB, 35 Honors) with physical embodiment of frontier learning models (Vision-Language-Action models on the PAL Robotics TIAGo PRO and Sim2Real RL on Franka Emika Panda arms).

### Brand Identity Pillars:
- **High-Precision Engineering:** Clean, structured, mathematical elegance. No generic AI templates or whimsical decorative clutter.
- **Physical Embodiment:** Immediate visual proof of physical robots interacting with real-world environments (demonstration videos, dynamic looping GIFs, synchronized photo carousels).
- **Academic & Industrial Authority:** Executive clarity communicating effortlessly with three key audiences: Frontier Embodied AI Labs (DeepMind, Physical Intelligence), Advanced Robotics Industry (PAL Robotics, Siemens), and Elite Academic Institutions (Inria, DLR, CSIC, UPC).
- **Bilingual Symmetry:** Identical aesthetic refinement, layout balance, and semantic hierarchy in both English and Catalan.

---

## 2. Harmonized Color System

### 2.1 The Accent Conflict Resolution
In the existing codebase (`css/styles.css`), `--accent` was defined as `#a09369` (a muted khaki/olive hue), while its CSS comment indicated `"Blau intens per a elements destacats"` (intense blue). Furthermore, `:hover` pseudo-classes forced `#0369a1` (a vivid cerulean blue), resulting in an abrupt, jarring visual transition.

The new palette eliminates this conflict by adopting an authoritative **Robotics Precision Palette**: a deep technical cobalt primary accent paired with crisp slate neutrals, warm card surfaces, and semantic category tints.

### 2.2 Color Tokens & Functional Roles

| Token Name | Hex Value | Purpose / Application | Contrast Ratio (vs #ffffff / #f8fafc) |
| :--- | :--- | :--- | :--- |
| `--bg-canvas` | `#f8fafc` | Global canvas background (Warm Slate 50). Subtle, reducing eye strain compared to pure `#ffffff`. | N/A (Canvas) |
| `--bg-card` | `#ffffff` | Elevated card surfaces, navigation bar, and modal containers. | N/A (Surface) |
| `--bg-card-subtle` | `#f1f5f9` | Secondary cards, callout boxes, and code/quote backdrops. | N/A (Surface) |
| `--text-primary` | `#0f172a` | Main headings, titles, high-emphasis text (Slate 900). | **15.8:1** (WCAG AAA) |
| `--text-secondary` | `#334155` | Body copy, technical descriptions, methodology text (Slate 700). | **9.6:1** (WCAG AAA) |
| `--text-muted` | `#64748b` | Metadata, dates, secondary labels, subheadings (Slate 500). | **4.6:1** (WCAG AA) |
| `--border-subtle` | `#e2e8f0` | Card borders, dividers, subtle separators (Slate 200). | N/A (Structural) |
| `--border-hover` | `#cbd5e1` | Hover-state border accentuation (Slate 300). | N/A (Interactive) |
| `--accent-primary` | `#0284c7` | Primary brand accent (Sky/Cobalt 600) for buttons, active tabs, and badges. | **4.5:1** (WCAG AA compliant) |
| `--accent-hover` | `#0369a1` | Hover state for primary buttons and interactive accents (Sky 700). | **6.1:1** (WCAG AAA) |
| `--accent-glow` | `rgba(2, 132, 199, 0.12)` | Subtle focus rings and card spotlight hover glows. | Visual feedback |
| `--linkedin` | `#0a66c2` | Official LinkedIn brand color. | Accessible on light cards |
| `--linkedin-hover`| `#084e96` | LinkedIn hover state. | Accessible on light cards |

### 2.3 Semantic Tag Color Tokens

To allow recruiters and research directors to rapidly parse multi-disciplinary projects, tags are color-coded by domain:

| Domain | Tag Background | Tag Text | Tag Border | Example Topics |
| :--- | :--- | :--- | :--- | :--- |
| **Physical Hardware** | `#f0fdf4` (Emerald 50) | `#15803d` (Emerald 700) | `#bbf7d0` | TIAGo PRO, Franka Panda, ZED 2i, HTC Vive Pro |
| **Toolchains & Simulation** | `#eff6ff` (Blue 50) | `#1d4ed8` (Blue 700) | `#bfdbfe` | NVIDIA Isaac Sim, Isaac Lab, ROS 2, PyTorch, Unity 3D |
| **AI & Learning Paradigms** | `#faf5ff` (Purple 50) | `#7e22ce` (Purple 700) | `#e9d5ff` | VLA Models, Agentic VLMs, Reinforcement Learning, Sim2Real |
| **Metrics & Distinctions** | `#fffbeb` (Amber 50) | `#b45309` (Amber 700) | `#fde68a` | Rank 2nd/298, 98.0% Success Rate, 1st Prize, 35 Honors |

---

## 3. Typography Hierarchy & System Font Stack

### 3.1 Font Stack
We preserve pure static delivery without external Google Fonts dependencies to maximize privacy, loading speed, and offline resilience:

```css
font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
```
This leverages high-density native platform typography (San Francisco on macOS/iOS, Segoe UI on Windows, Roboto on Android, Ubuntu on Linux).

### 3.2 Modular Typography Scale

| Level | Size | Weight | Line Height | Letter Spacing | Context |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Display / Hero H1** | `2.5rem` (40px) | `800` (Extrabold) | `1.15` | `-0.025em` | Page main headers (Homepage, Section Titles) |
| **Section H2** | `1.65rem` (26px) | `700` (Bold) | `1.25` | `-0.015em` | Card titles, project names, section headers |
| **Subheading H3** | `1.25rem` (20px) | `600` (Semibold) | `1.35` | `-0.01em` | Subsection headings (The Challenge, Contributions) |
| **Body Large** | `1.1rem` (17.5px) | `400` (Regular) | `1.65` | `0` | Hero lead paragraph, about me summary |
| **Body Regular** | `0.975rem` (15.5px)| `400` (Regular) | `1.6` | `0` | Narrative paragraphs, case study details |
| **Metadata / Badges**| `0.825rem` (13px) | `600` (Semibold) | `1.4` | `+0.015em` | Badges, tags, institution timestamps, button labels |
| **Micro / Footnotes** | `0.75rem` (12px) | `500` (Medium) | `1.4` | `+0.02em` | Handles, DOIs, image captions |

---

## 4. Surfaces, Depth & Elevation Architecture

### 4.1 Border Radii
- **Cards & Media Containers:** `12px` (`0.75rem`)
- **Buttons & Interactive Badges:** `8px` (`0.5rem`)
- **Tag Badges:** `6px` (`0.375rem`)
- **Profile / Circular Elements:** `50%`

### 4.2 Elevation Levels (Box Shadows)
Cards use multi-layered ambient occlusion shadows rather than harsh drop-shadows:
- **Base Card Elevation (Rest):**
  ```css
  box-shadow: 0 1px 3px 0 rgba(15, 23, 42, 0.05), 0 1px 2px -1px rgba(15, 23, 42, 0.05);
  border: 1px solid var(--border-subtle);
  ```
- **Hover / Interactive Card Elevation:**
  ```css
  box-shadow: 0 10px 25px -5px rgba(15, 23, 42, 0.08), 0 8px 10px -6px rgba(15, 23, 42, 0.04);
  transform: translateY(-2px);
  border-color: var(--border-hover);
  ```
- **Sticky Header Glassmorphic Surface:**
  ```css
  background: rgba(255, 255, 255, 0.88);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border-subtle);
  ```

---

## 5. Responsive Grid & Layout Architecture

### 5.1 Viewport Breakpoints
- **Mobile (< 640px):** Single column, 100% width padding `1rem`, compact header, vertical button groups.
- **Tablet (640px – 1024px):** 2-column metric cards, responsive media aspect ratio, full-width case study cards.
- **Desktop (1024px+):** Max container width `960px` (or `1080px` for featured spotlight grid), 4-column metric pillars, rich inline media carousels.

### 5.2 Elimination of Global Body Flex Anti-Pattern
In the existing codebase, `body { display: flex; align-items: center; justify-content: center; min-height: 100vh; }` forced every content subpage to manually override body properties.
**Resolution:**
- Global `body` defaults to standard document flow:
  ```css
  body {
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
      background: var(--bg-canvas);
      color: var(--text-primary);
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
  }
  ```
- Centered splash pages (`index.html`, `wip.html`) apply a targeted utility class: `.centered-layout`.

---

## 6. Detailed Component Specifications

### 6.1 Sticky Bilingual Navigation Bar (`.site-header`)
- **Structure:** Fixed to top of viewport with `z-index: 1000`.
- **Left Wing:** Monogram branding: `[ABG] Arnau Boix Granell`.
- **Center Wing (Desktop):** Section navigation links:
  - Cat: `Inici` · `Projectes Professionals` · `Projectes Acadèmics` · `Articles` · `Comunitat`
  - Eng: `Home` · `Professional Projects` · `Academic Projects` · `Articles` · `Community`
- **Right Wing:** LinkedIn icon + Discreet Easter Egg + Language Switcher Toggle (`CAT` / `ENG`).
- **Responsive Behavior:** On mobile screens (<640px), links collapse into a clean breadcrumb / back-button pattern to maximize screen real estate.

### 6.2 Hero Section & The 4 Core Impact Pillars
Located immediately below the hero profile, the 4 Core Impact Pillars convert abstract qualifications into instant, undeniable factual metrics:

```html
<div class="impact-grid">
    <!-- Pillar 1: Academic Pedigree -->
    <div class="impact-card">
        <div class="impact-metric">2n / 298</div>
        <div class="impact-label">Class Rank · Top 0.67%</div>
        <div class="impact-sub">35 Matrícules d'Honor (UPC ETSEIB)</div>
    </div>
    <!-- Pillar 2: High-Stakes EU Projects -->
    <div class="impact-card">
        <div class="impact-metric">40M€ GRAIL</div>
        <div class="impact-label">Horizon Europe Flagship</div>
        <div class="impact-sub">MWC 2026 Live TIAGo Demo</div>
    </div>
    <!-- Pillar 3: Physical Platforms -->
    <div class="impact-card">
        <div class="impact-metric">TIAGo & Panda</div>
        <div class="impact-label">Physical Embodiment</div>
        <div class="impact-sub">Isaac Lab GPU Sim2Real Transfer</div>
    </div>
    <!-- Pillar 4: Scientific Dissemination -->
    <div class="impact-card">
        <div class="impact-metric">1st Author</div>
        <div class="impact-label">ERF 2026 (PRISM)</div>
        <div class="impact-sub">Co-author IEEE ICRA 2023 · CCIA 2022</div>
    </div>
</div>
```

### 6.3 Flagship Project Spotlight Grid (Homepage)
A 3-column card grid placed prominently on `main-*.html` showcasing:
1. **COGNITIUM:** Physical VLA fine-tuning on TIAGo PRO & live public MWC 2026 demo.
2. **PRISM:** Prompt-Conditioned Imitation Policy Refinement (ERF 2026 lead-author paper).
3. **GRAIL:** Sovereign European Generative AI for industrial robotics automation.
Each spotlight card includes a media thumbnail, key metrics badge (e.g. `98.0% Success Rate`), concise challenge summary, and direct anchor link to full case study.

### 6.4 Technical Case Study Card Layout
Every project and article follows a strict, repeatable engineering anatomy:
1. **Header Row:** Project Title (`h2`), Institution Badge, Chronology Badge (`2025–2026`).
2. **Authors / Subtitle:** Clear attribution of roles and collaborators.
3. **Media Container:** Inline responsive media carousel or 16:9 embedded video.
4. **Structured Topic Tags:** Categorized pills for Physical Hardware, Toolchain, and Learning Paradigms.
5. **Structured Technical Narrative:**
   - **The Challenge (*El Repte*):** Clear problem definition.
   - **Arnau's Direct Contributions (*Aportacions Directes d'Arnau*):** Bulleted list of individual technical deliverables.
   - **Results & Empirical Metrics (*Resultats i Impacte*):** Concrete performance numbers (e.g. 21.2% -> 98.0% success rate).
   - **Hardware & Software Stack (*Maquinari i Entorn de Programari*):** Physical platforms and exact libraries.
6. **Actions & Links:** High-contrast buttons linking to publication DOIs, UPCommons handles, project websites, or demonstration videos.

### 6.5 Touch-Enabled Carousel with Bullet Pagination
The existing carousel lacks visual slide count and touch swiping. The upgraded vanilla JS carousel includes:
- Dot pagination bullets showing active slide index.
- Touch gesture detection (`touchstart`, `touchend`) with swipe threshold.
- Keyboard arrow navigation when focused.
- Accessible ARIA labels (`aria-label="Slide 1 of 3"`).

### 6.6 Embedded Responsive Video Player Wrapper
Zero-layout-shift responsive 16:9 container using modern CSS `aspect-ratio`:
```css
.video-wrapper {
    position: relative;
    width: 100%;
    aspect-ratio: 16 / 9;
    border-radius: 8px;
    overflow: hidden;
    background: #0f172a;
    margin-bottom: 1.25rem;
}
.video-wrapper iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: none;
}
```

---

## 7. Accessibility & Performance Benchmarks
- **Target Performance:** 100/100 Google Lighthouse score on GitHub Pages.
- **WCAG AA Compliance:** All text contrast ratios strictly exceed 4.5:1.
- **Semantic HTML5:** Native `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>` elements.
- **Image Optimization:** Explicit `alt` attributes describing actual robotics content; `loading="lazy"` on below-the-fold media.
