# Website Audit: Structure, Architecture, Code Quality & Bilingual Integrity
*Forensic Codebase Analysis — Compiled by Career Auditor*

## 1. Physical Architecture & Repository Map

```
portfolio/
├── index.html                           # Landing page & language selector
├── css/
│   └── styles.css                       # Shared stylesheet & color palette
├── cat/                                 # Catalan version (7 files)
│   ├── main-cat.html                    # Homepage (About me, Exp, Education)
│   ├── projectes-professionals-cat.html # Professional Projects (GRAIL, COGNITIUM, INTELLIMAN)
│   ├── projectes-academics-cat.html     # Academic Projects (Summer School, TFM, Engihack, TFG)
│   ├── articles-cat.html                # Publications (PRISM, ICRA 2023, CCIA 2022)
│   ├── altres-cat.html                  # Other activities (euRobotics DII)
│   ├── plantilla-cat.html               # Unused template page containing TODO placeholders
│   └── wip.html                         # Work In Progress page
├── eng/                                 # English version (5 files)
│   ├── main-eng.html                    # Homepage (About me, Exp, Education)
│   ├── projectes-professionals-eng.html # Professional Projects (GRAIL, COGNITIUM, INTELLIMAN)
│   ├── projectes-academics-eng.html     # Academic Projects (Summer School, TFM, Engihack, TFG)
│   ├── articles-eng.html                # Publications (PRISM, ICRA 2023, CCIA 2022)
│   └── altres-eng.html                  # Other activities (euRobotics DII)
├── imatges/                             # 19 static images & project gifs
└── giff/
    └── WIP.gif                          # Animated dancing pug GIF used in cat/wip.html
```

---

## 2. Broken Links & Navigation Bugs

### 2.1 Critical Bug: Broken Language Switcher in `eng/altres-eng.html`
- **Location:** `eng/altres-eng.html` (Line 218)
- **Current Code:** `<a href="altres-cat.html" class="lang-btn">CAT</a>`
- **Issue:** On the English page, the relative path points to `altres-cat.html` instead of `../cat/altres-cat.html`.
- **User Impact:** Clicking "CAT" in the English "Others" page yields a **404 Not Found** error.

### 2.2 Critical Bug: Secret Button 404 in `eng/main-eng.html`
- **Location:** `eng/main-eng.html` (Line 103)
- **Current Code:** `<a href="wip.html" class="secret-btn" title=""></a>`
- **Issue:** The file `wip.html` only exists inside `cat/wip.html`; there is no `eng/wip.html`.
- **User Impact:** Clicking the hidden button next to LinkedIn on the English homepage yields a **404 Not Found** error.

### 2.3 Broken Publication Link: Mixed-Up Citations for Article 2 & 3
- **Location:** 
  - `cat/articles-cat.html` (Lines 283–310)
  - `eng/articles-eng.html` (Lines 283–310)
- **Finding:**
  - Article 2 is the **ICRA 2023** paper: `A Virtual Reality Framework for Fast Dataset Creation Applied to Cloth Manipulation with Automatic Semantic Labelling`. Its DOI is `10.1109/ICRA48891.2023.10161122`, which corresponds to IEEE Xplore document `10161122`. On the website, it links to Digital CSIC (`https://digital.csic.es/handle/10261/354962`).
  - Article 3 is the **CCIA 2022** paper: `Garment Manipulation Dataset for Robot Learning from Demonstration Using a Virtual Reality Framework`.
  - **The Error:** In both language versions, Article 3 links to `https://ieeexplore.ieee.org/abstract/document/10161122`! This means clicking the link under CCIA 2022 opens the **ICRA 2023** paper on IEEE Xplore, instead of the CCIA 2022 IOS Press / CSIC publication (`http://hdl.handle.net/10261/281403` or `https://ebooks.iospress.nl/doi/10.3233/FAIA220334`).

### 2.4 Placeholder Alt Tag in `cat/altres-cat.html`
- **Location:** `cat/altres-cat.html` (Line 238)
- **Current Code:** `<img src="../imatges/euRobotics_logo.png" alt="TODO: NOM FOTO" class="article-img-full">`
- **Issue:** Leftover placeholder `alt="TODO: NOM FOTO"`.

### 2.5 Unfinished File in Production: `cat/plantilla-cat.html`
- **Location:** `cat/plantilla-cat.html` (Lines 1–255)
- **Issue:** The file contains 12 `TODO:` placeholders (e.g. `<title>TODO: Nom pagina</title>`, `<h1>TODO: Titol</h1>`, `<a href="wip.html" class="lang-btn">ENG</a>`). It should not be linked or crawled.

---

## 3. Bilingual Inconsistencies & Factual Discrepancies

| Item / Section | Catalan Version (`cat/`) | English Version (`eng/`) | Verified Source of Truth |
| :--- | :--- | :--- | :--- |
| **Article 1 Title** | *PRISM: Refinament personalitzat d’habilitats d’imitació per a la manipulació mitjançant instruccions humanes* | *PRISM: Prompt-Conditioned Imitation Skill Refinement for Manipulation* | arXiv:2603.05574: **"PRISM: Personalized Refinement of Imitation Skills for Manipulation via Human Instructions"**. The English title is inconsistent with arXiv! |
| **GRAIL Project Name** | *GRAIL: Arquitectura Robòtica General per a l'Aprenentatge Intel·ligent* | *GRAIL: General Robot Architecture for Intelligent Learning* | Official EU Project Title: **"Generative Robotics & AI for EU Industrial Leadership"**. Both versions use an incorrect title! |
| **TFM Description** | Line 325: *"En aquest treball de fi de grau..."* (Bachelor's thesis) | Line 325: *"In this thesis..."* | Factual error in Catalan: it is a **Master's thesis** (*treball de fi de màster*), not a degree thesis. |
| **Tone in "Altres / Others"** | Line 224: *"Popurri d'altres coses que faig en el meu temps lliure."* | Line 224: *"A mix of other activities and interests in my free time."* | The Catalan term "Popurri" is overly informal/colloquial for an international robotics researcher portfolio. |
| **Co-author Name in PRISM** | Alberto San-Miguel | Alberto San-Miguel | On arXiv the author is registered as **Alberto San-Miguel-Tello**. |

---

## 4. CSS Architecture & Visual Design Audit

### 4.1 CSS Palette Discrepancy in `css/styles.css`
- **Location:** `css/styles.css` (Line 8 & Line 60)
- **Code:**
  ```css
  --accent: #a09369; /* Blau intens per a elements destacats */
  ...
  .btn-primary:hover {
      opacity: 0.9;
      background: #0369a1;
  }
  ```
- **Finding:**
  - The comment for `--accent` states `"Blau intens"` (intense blue), but the hex `#a09369` is a tan/khaki/gold hue.
  - On hover, `.btn-primary:hover` forces `background: #0369a1;` which is a bright sky blue!
  - This creates an abrupt, jarring color shift from tan/khaki (`#a09369`) to blue (`#0369a1`).

### 4.2 Body Display Flex Anti-Pattern in Global CSS
- **Location:** `css/styles.css` (Lines 16–28)
- **Code:**
  ```css
  body {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      text-align: center;
  }
  ```
- **Finding:** Centering `body` via `display: flex` and `text-align: center` in the *global* stylesheet fits `index.html` and `wip.html`, but breaks normal document flow for long content pages. As a workaround, **every single sub-page** (`main-*.html`, `projectes-*.html`, `articles-*.html`, `altres-*.html`) is forced to override `body` with an inline block:
  ```css
  body { display: block; text-align: left; position: relative; padding-top: 4rem; padding-bottom: 3rem; }
  ```
- **Recommendation:** Keep default normal flow in `styles.css` and restrict flex-centering only to splash/modal pages like `index.html`.

### 4.3 Redundant Embedded CSS (~200 lines per file)
- Each HTML file carries an extensive embedded `<style>` block (90 to 260 lines) duplicating headers, card components, badges, media wrappers, and carousels.
- Component styles (`.article-card`, `.carousel-container`, `.linkedin-top`, `.lang-selector`, `.btn-back`) should eventually be centralized in `styles.css` without altering layout.

### 4.4 Carousel JavaScript Duplication
- An identical 27-line vanilla JS carousel script (`slideIndexes`, `moveSlide`) is duplicated at the bottom of:
  - `cat/projectes-professionals-cat.html`
  - `eng/projectes-professionals-eng.html`
  - `cat/projectes-academics-cat.html`
  - `eng/projectes-academics-eng.html`
- Lacks touch swiping for mobile devices, keyboard arrow accessibility, or visual dot pagination.

---

## 5. Assets & Media Audit

### 5.1 Asset Inventory & Filename Inconsistencies

| File Path | Type | Referenced By | Observations / Issues |
| :--- | :--- | :--- | :--- |
| `imatges/ArnauBoix.jpeg` | JPEG | `index.html`, `main-*.html` | High quality professional portrait. |
| `imatges/GRAIL_Logo.png` | PNG | `projectes-professionals-*.html` | Project logo. |
| `imatges/Cobnitium_Logo.webp` | WebP | `projectes-professionals-*.html` | **Typo in filename**: `Cobnitium` instead of `Cognitium`. |
| `imatges/cognitium_MWC_1.jfif` | JFIF | `projectes-professionals-*.html` | Photo at MWC 2026. Standard JPEG format preferred over `.jfif` for broad browser compatibility. |
| `imatges/cogntitium_mwc.gif` | GIF | `projectes-professionals-*.html` | **Typo in filename**: `cogntitium` instead of `cognitium`. Located in `imatges/` instead of `giff/`. |
| `imatges/Intelliman_logo.svg` | SVG | `projectes-professionals-*.html` | High quality vector logo. |
| `imatges/intelliman.gif` | GIF | `projectes-professionals-*.html` | Located in `imatges/` instead of `giff/`. |
| `imatges/SummerSchool.gif` | GIF | `projectes-academics-*.html` | Demonstration GIF. Located in `imatges/`. |
| `imatges/SummerSchoolFinal.JPG` | JPEG | `projectes-academics-*.html` | Group photo. Uppercase `.JPG` extension. |
| `imatges/tfm2.gif` | GIF | `projectes-academics-*.html` | Dishwasher door opening simulation demo. |
| `imatges/Engihack1.JPG` | JPEG | `projectes-academics-*.html` | Award photo. Uppercase `.JPG` extension. |
| `imatges/Engihack2.JPG` | JPEG | `projectes-academics-*.html` | Award photo. Uppercase `.JPG` extension. |
| `imatges/Engihack3.jpeg` | JPEG | `projectes-academics-*.html` | Award photo. Mixed extension (`.jpeg` vs `.JPG`). |
| `imatges/tfg1.PNG`, `tfg2.PNG`, `tfg3.PNG` | PNG | `projectes-academics-*.html` | VR environment screenshots. Uppercase `.PNG`. |
| `imatges/Article1.svg` | SVG | `articles-*.html` | CCIA 2022 diagram. |
| `imatges/Article2.jpg` | JPEG | `articles-*.html` | ICRA 2023 experimental setup figure. |
| `imatges/Article3.svg` | SVG | `articles-*.html` | PRISM architecture diagram (contains embedded base64 image data). |
| `imatges/euRobotics_logo.png` | PNG | `altres-*.html` | euRobotics logo. |
| `giff/WIP.gif` | GIF | `cat/wip.html` | Dancing pug animation. |
