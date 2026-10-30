# Professional Portfolio Strategy: Arnau Boix Granell
*High-Impact Positioning, Architecture, Project Hierarchy & Execution Blueprint*
*Formulated by Portfolio Strategist*

---

## 1. Executive Summary & Strategic Objectives

The professional career of Arnau Boix Granell represents a rare, highly prized profile in the global robotics landscape: **a hybrid researcher and roboticist who bridges mathematical rigor and academic excellence with hands-on, physical platform deployment of cutting-edge learning models (VLAs, Agentic VLMs, Sim2Real RL).**

### Strategic Objectives:
1. **Elevate Identity from Generalist Engineer to Specialized Robotics AI Researcher:** Shift from the modest title *"Manipulative and Collaborative Robotics Researcher"* to a compelling, modern positioning: *"Robotics Researcher | Learning-Based Manipulation, Vision-Language-Action (VLA) Models & Sim2Real Transfer"*.
2. **Front-Load Exceptional Differentiators:** Make his standout academic achievement (**Ranked 2nd out of 298 engineers at UPC ETSEIB**, **35 cumulative Honors / *Matrícules d'Honor***) and elite real-world milestones (**MWC 2026 live TIAGo demo**, **€40M Horizon Europe GRAIL project**, **ERF 2026 1st-author paper**, **ICRA 2023 paper**) immediately visible on the homepage viewport.
3. **Preserve Architecture & Enhance UX/Bilingual Parity:** Maintain the existing vanilla HTML/CSS multi-page architecture without unnecessary dependencies or framework rewrites, while fixing critical navigation bugs (broken CAT switcher, secret button 404, citation swaps) and establishing symmetrical English and Catalan versions.
4. **Transform Project Cards into Structured Technical Case Studies:** Restructure project and publication cards to clearly distinguish individual contributions from consortium efforts, highlight the exact physical hardware and software toolchain (TIAGo PRO, Franka Panda, Isaac Lab, LeRobot, ROS 2), and embed visual proof directly in-line.

---

## 2. Professional Positioning & Core Value Proposition

### 2.1 The Professional Identity Formula
```
[Academic Rigor & Mathematical Foundations] 
                     + 
[Frontier Learning Paradigms: VLAs, Agentic VLMs, Eureka RL] 
                     + 
[Sim2Real Physical Embodiment on TIAGo PRO & Franka Panda]
                     =
World-Class Robotics AI Researcher capable of taking complex manipulation
from theoretical formulation and simulation directly to physical platform deployment.
```

### 2.2 Core Differentiators Matrix

| Differentiator | Factual Evidence | Strategic Framing for Portfolio |
| :--- | :--- | :--- |
| **Elite Academic Pedigree** | Ranked 2nd of 298 at UPC ETSEIB; 35 *Matrícules d'Honor* (23 in Bachelor's, 12 in Master's); PAU 12.386/14; High School in USA. | Demonstrates exceptional intellectual horsepower, fast learning speed, mathematical rigor, and bilingual communication mastery. |
| **Frontier Robotics AI Mastery** | Fine-tuning and deploying VLAs (LeRobot, OpenVLA); Agentic AI reasoning with VLMs; Prompt-conditioned RL with Eureka extensions (PRISM). | Shows capability at the absolute frontier of modern robotics—bridging foundation models and embodied physical execution. |
| **Physical Platform Deployment (Sim2Real)** | Deployed learned policies on physical PAL Robotics TIAGo PRO mobile manipulator and Franka Emika Panda 7-DOF arm; closed the sim-to-real gap using NVIDIA Isaac Lab and ROS 2. | Distinguishes him from purely theoretical "simulation-only" AI researchers. He understands physical kinematics, latency, real-time control, sensor noise, and hardware safety. |
| **High-Stakes European Consortia & Industry Impact** | Researcher in GRAIL (€40M flagship Horizon Europe initiative with Siemens, ETH, DLR, Imperial) and INTELLIMAN; live public demo at Mobile World Congress (MWC) Barcelona 2026. | Validates ability to collaborate in international consortia, meet industrial deliverables, and present robust systems in high-profile public arenas. |
| **Peer-Reviewed Scientific Record** | 1st Author at ERF 2026 (PRISM); Co-author at IEEE ICRA 2023; Lead author at CCIA 2022; INIREC Competitive Research Fellowship. | Solid track record of peer-reviewed research, dataset generation, and academic dissemination. |
| **Leadership & Community Service** | Active Member of the euRobotics Diversity & Inclusion Initiative (DII), ERF workshop contributor; 1st Prize Engihack 2024 (€3,000 award, TV3 broadcast). | Demonstrates ethical awareness, teamwork, public speaking under pressure, and active leadership within the European robotics ecosystem. |

---

## 3. Target Audiences & Evaluator Personas

The portfolio must speak convincingly to three distinct evaluator archetypes without alienating any of them:

- **Audience A: Frontier AI & Embodied Intelligence Labs** (DeepMind, Physical Intelligence, Skild AI, TRI, Hugging Face):
  - *Scrutinizes:* VLA/VLM mastery, Isaac Lab/Sim, large-scale demonstration capture, Sim2Real transfer.
  - *Strategic Response:* Feature COGNITIUM (VLA deployment with LeRobot), PRISM (Eureka-style prompt-conditioned RL policy refinement), and GRAIL (VLM agentic planning and teleoperation collection). Emphasize NVIDIA Isaac Lab, PyTorch, and VLA architectures.
- **Audience B: Advanced Robotics Industry & Corporate R&D** (PAL Robotics, ABB, KUKA, Siemens, Franka Robotics):
  - *Scrutinizes:* Physical hardware reliability, ROS 2 integration, industrial standards, consortium delivery.
  - *Strategic Response:* Highlight live deployment on the TIAGo mobile manipulator at MWC 2026, Franka Emika Panda Sim2Real deployment for dishwasher manipulation, and key role in the €40M Horizon Europe GRAIL project.
- **Audience C: Elite Academic & Public Research Institutions** (Inria, DLR, CSIC, UPC, ETH Zurich, EPFL):
  - *Scrutinizes:* 1st-author publications (ERF, ICRA), mathematical rigor (Rank 2nd/298), scientific methodology.
  - *Strategic Response:* Showcase Class Rank (2nd out of 298 at ETSEIB), 35 Matrícules d'Honor, ERF 2026 first-author paper, and IEEE ICRA 2023 paper, along with clear thesis defense links on UPCommons and DIGITAL.CSIC.

---

## 4. Portfolio Architecture & Navigation Strategy

### 4.1 Architecture Preservation Directives
In strict compliance with `.agents/AGENTS.md` and user rules:
- **No framework migration:** Preserve vanilla HTML5 and CSS3 deployed on GitHub Pages.
- **Maintain multi-page site structure:** Keep `index.html` (entry point / language picker), `cat/` directory, and `eng/` directory.
- **Maintain existing URLs:** Do not break existing bookmarkable endpoints (`main-*.html`, `projectes-professionals-*.html`, `projectes-academics-*.html`, `articles-*.html`, `altres-*.html`).

### 4.2 Structural & Semantic Enhancements

```
portfolio/
├── index.html                           # Clean entry splash & language selection
├── css/
│   └── styles.css                       # Centralized, unified stylesheet (fixed accent colors)
├── cat/                                 # Catalan Architecture
│   ├── main-cat.html                    # Redesigned Homepage: Hero + Metrics Grid + Featured Spotlight + About + Exp + Edu
│   ├── projectes-professionals-cat.html # Professional Projects: GRAIL, COGNITIUM, INTELLIMAN (Elevated Case Studies)
│   ├── projectes-academics-cat.html     # Academic Projects: TFM, AIxHRI Summer School, Engihack, TFG
│   ├── articles-cat.html                # Publications: PRISM (ERF 2026), ICRA 2023, CCIA 2022 (Fixed Links)
│   ├── altres-cat.html                  # Elevated: "Comunitat, Lideratge i Iniciatives" (euRobotics DII)
│   └── wip.html                         # Coordinated WIP Easter Egg
└── eng/                                 # English Architecture (Strict Parity)
    ├── main-eng.html                    # Redesigned Homepage: Hero + Metrics Grid + Featured Spotlight + About + Exp + Edu
    ├── projectes-professionals-eng.html # Professional Projects: GRAIL, COGNITIUM, INTELLIMAN (Elevated Case Studies)
    ├── projectes-academics-eng.html     # Academic Projects: TFM, AIxHRI Summer School, Engihack, TFG
    ├── articles-eng.html                # Publications: PRISM (ERF 2026), ICRA 2023, CCIA 2022 (Fixed Links)
    ├── altres-eng.html                  # Elevated: "Community, Leadership & Initiatives" (Fixed CAT Switcher)
    └── wip.html                         # Added to prevent 404 on secret button
```

### 4.3 Key Architectural Changes Justified:
1. **Fix Broken Navigation Elements:**
   - In `eng/altres-eng.html`, fix line 218 from `<a href="altres-cat.html" class="lang-btn">CAT</a>` to `<a href="../cat/altres-cat.html" class="lang-btn">CAT</a>`.
   - Add `eng/wip.html` mirroring `cat/wip.html` so the hidden easter-egg button never triggers a 404 error.
   - Fix Article 2 & 3 link mixup: Point CCIA 2022 to DIGITAL.CSIC / IOS Press, and ICRA 2023 to IEEE Xplore (`10.1109/ICRA48891.2023.10161122`).
2. **Elevate "Altres / Others" Section Framing:**
   - Rename page header from *"Others / Popurri d'altres coses que faig en el meu temps lliure"* to **"Community, Leadership & Initiatives"** (*"Comunitat, Lideratge i Iniciatives"*). Framing euRobotics DII under "Community & Leadership" significantly enhances executive stature.
3. **Cross-Page Sticky / Global Navigation:**
   - Provide clean top-bar navigation back to Home and between subpages to prevent "dead-end" subpage browsing.

---

## 5. Homepage Enhancement Strategy (`main-eng.html` & `main-cat.html`)

The homepage features:
- **Hero Section:** Clear modern title, verified affiliation at Eurecat Robotics & Automation Unit.
- **Core Impact Pillars (4 Metric Cards):**
  1. *Academic Rigor:* 2nd of 298 cohort (Top 0.67%) · 35 Matrícules d'Honor (UPC ETSEIB).
  2. *Frontier AI Projects:* €40M Flagship Horizon Europe GRAIL · MWC 2026 Live TIAGo Demo.
  3. *Physical Platforms:* TIAGo PRO Mobile Manipulator & Franka Emika Panda.
  4. *Scientific Impact:* First-author at ERF 2026 · Co-author at IEEE ICRA 2023.
- **Featured Spotlight (Flagship Previews):**
  - COGNITIUM: Physical VLA Deployment on TIAGo PRO @ MWC 2026.
  - PRISM: Prompt-Conditioned Policy Refinement (ERF 2026 Lead Author).
  - GRAIL: Sovereign European Foundation AI for Industrial Robotics.
- **Structured Experience & Education:** Clear, verified chronologies with thesis handles.

---

## 6. Project Prioritization & Case Study Hierarchy

### TIER 1: Flagship Case Studies (Full Technical Depth, Inline Media & Direct Spotlight)
1. **COGNITIUM — Physical VLA Deployment on TIAGo Mobile Manipulator (Eurecat, 2025–2026)**
2. **PRISM — Personalized Refinement of Imitation Skills via Human Instructions (ERF 2026 / arXiv:2603.05574)**
3. **GRAIL — Generative Robotics & AI for EU Industrial Leadership (Horizon Europe, 2026–Present)**

### TIER 2: Core Research & Academic Foundations (Elevated Technical Detail)
4. **Master's Thesis (TFM) — Reinforcement Learning for Complex & Dynamic Manipulation Tasks (2023–2025)**
5. **INTELLIMAN — AI-Powered Manipulation System for Advanced Service & Manufacturing (Horizon Europe, 2022–2026)**
6. **ICRA 2023 & Bachelor's Thesis (TFG) — VR Learning from Demonstration Framework for Garment Folding (IRI CSIC-UPC, 2021–2022)**

### TIER 3: Distinctions, Community Leadership & Specialized Training
7. **Engihack 2024 — EcoShower Project (1st Prize Winner, €3,000 Award, TV3 Broadcast)**
8. **euRobotics Diversity and Inclusion Initiative (DII) (2026–Present)**
9. **AIxHRI Summer School (Inria / Loria, Nancy, France, 2026)**
10. **CCIA 2022 Publication — Garment Manipulation Dataset via VR (Lead Author)**

---

## 7. Project Case Study Template / Structural Standard

Every project card in `projectes-professionals-*.html`, `projectes-academics-*.html`, and `articles-*.html` must follow this schema:
1. **Header:** Title, Badge (Institution/Venue + Year).
2. **Authors / Subtitle:** Clear attribution of roles.
3. **Media Container:** Responsive carousel, looping GIF, or video embed.
4. **Structured Topic Tags:** Categorized by Hardware, Toolchain, and Learning Methods.
5. **Technical Narrative:**
   - *The Challenge:* Core engineering problem.
   - *Arnau's Direct Contributions:* Bulleted specific responsibilities.
   - *Results & Impact:* Concrete outcomes, presentations, publications, or metrics.
6. **Action Links:** Direct links to paper (arXiv / IEEE / CSIC / UPCommons), code/website, and video demonstrations.

---

## 8. Specific Directives for Peer Subagents

- **Robotics Technical Editor:** Correct GRAIL title to *"Generative Robotics & AI for EU Industrial Leadership"*; ensure exact naming for TIAGo, Franka Panda, NVIDIA Isaac Lab, and LeRobot; enforce standardized terminology in English and Catalan.
- **Storytelling Agent:** Build the narrative progression across all projects (VR demonstrations -> Sim2Real RL -> Embodied VLAs); rewrite Catalan text in `altres-cat.html` to eliminate colloquialisms.
- **UX/UI Designer:** Resolve `--accent` CSS color conflict (`#a09369` vs `#0369a1`); fix broken links; implement Hero metric cards and structured case studies; add touch/dot navigation to carousels.
- **Recruiter & QA Reviewer:** Verify all links, citation URLs, bilingual symmetry, and responsive mobile rendering.
