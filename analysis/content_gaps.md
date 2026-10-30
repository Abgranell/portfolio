# Content Gaps: Strategic Deficits, Missing Information & Optimization Directives
*Strategic Gap Analysis — Compiled by Career Auditor*

## 1. Technical Depth & Quantitative Metrics Gaps

1. **Hardware Specifics Omitted:**
   - The current portfolio mentions "manipulador robòtic mòbil" or "robot manipulador" in several places without immediately highlighting the specific high-end platforms:
     - **PAL Robotics TIAGo PRO / TIAGo** (7-DOF arm, mobile omnidirectional base, RGB-D perception).
     - **Franka Emika Panda** (research-standard 7-DOF torque-controlled collaborative manipulator).
     - **HTC Vive Pro VR + Stereolabs ZED 2i / ZED Mini + Leap Motion** hand tracker.
   - *Recommendation:* Hardware callout tags should explicitly showcase experience on standard industry/research robots.

2. **Absence of Quantitative Performance Metrics:**
   - In **TFM / INTELLIMAN**, the description explains the task of opening a dishwasher door, but lacks specific success rate metrics, training step counts, policy convergence timelines, or reward formulation details.
   - In **PRISM**, the text mentions that the proposed approach "outperforms policies without human feedback", but does not cite the exact percentage improvement in task success, sample efficiency gains, or rollout reduction numbers.
   - In **TFG / Cloth Manipulation**, the dataset规模 (number of trajectories, cloth variations, execution times) is not quantified on the page.

3. **Missing Toolchain & Software Stack Visibility:**
   - Arnau works with elite, cutting-edge robotics toolchains:
     - **Simulation:** NVIDIA Isaac Sim, NVIDIA Isaac Lab.
     - **Learning Frameworks:** Hugging Face LeRobot, PyTorch, Stable-Baselines3 / RLlib, Eureka.
     - **Robotics Middleware:** ROS 2 (rclpy/rclcpp), MoveIt 2.
     - **Models:** OpenVLA, Octo, RT-X, LLM/VLM APIs (GPT-4o, Claude 3.5 Sonnet).
   - Currently, these are only scattered as small badge tags (`<span class="topic-tag">`) without context or depth explaining his direct mastery.

---

## 2. Structural & Storytelling Gaps

1. **Terse Homepage (Missed Hero Impact):**
   - The current `main-*.html` page consists solely of a profile image, a 2-line title, 4 navigation buttons, and brief text cards.
   - It fails to showcase his strongest achievements upfront:
     - Ranked 2nd out of 298 engineers at UPC ETSEIB.
     - Active researcher in a €40M Horizon Europe project (GRAIL).
     - Live demo at MWC Barcelona 2026.
     - 1st author paper at ERF 2026 and co-author at ICRA 2023.
   - *Recommendation:* The homepage should feature a "Key Highlights" or "Featured Impact" showcase before requiring users to navigate away.

2. **Hidden Video Demonstrations:**
   - Robotics is an inherently visual discipline. Currently, video demonstrations for PRISM and COGNITIUM are linked via external text buttons (`Vídeo article →`, `Vídeo projecte →`), taking visitors off the website to YouTube.
   - Embedding responsive video players or clean looping WebP/MP4 previews directly on the project cards would massively increase visual engagement and credibility.

3. **Distinction Between Individual Contribution & Consortium Results:**
   - Projects like GRAIL and INTELLIMAN are multi-million euro consortia involving dozens of international institutions.
   - While the project cards have an "Aportacions / Contributions" bulleted list, recruiters and hiring managers need clearer distinction between what the consortium delivered and what Arnau personally designed, coded, and validated.

---

## 3. Bilingual & Structural Gaps

1. **Asymmetric Page Count:**
   - Catalan version has 7 pages; English version has 5 pages.
   - `eng/wip.html` is completely missing, causing 404 links.
2. **Naming Inconsistencies:**
   - GRAIL: Misnamed in both languages ("General Robot Architecture for Intelligent Learning" vs. "Generative Robotics & AI for EU Industrial Leadership").
   - PRISM: English card title does not match the official publication title on arXiv.
3. **Tone and Polish:**
   - `cat/altres-cat.html` uses the word *"Popurri"*, which undermines the professional academic tone. A phrase like *"Altres activitats i iniciatives"* would be significantly more fitting.

---

## 4. Actionable Directives for Peer Subagents

### Directives for Portfolio Strategist:
- **Reposition Identity:** Frame Arnau as a **"Robotics Researcher specializing in Learning-Based Manipulation, VLAs, and Sim2Real Transfer"**.
- **Front-load Differentiators:** Move his 2nd rank at ETSEIB (298 students), 35 Honors, and MWC 2026 / ERF 2026 milestones to the primary viewport.
- **Hierarchy of Projects:** Prioritize **GRAIL** and **COGNITIUM** at the top of professional experience; feature **PRISM** and **ICRA 2023** as flagship scientific publications.

### Directives for Robotics Technical Editor:
- Standardize all technical terminology across Catalan and English:
  - *Vision-Language-Action (VLA) models* / *Models Visió-Llenguatge-Acció (VLA)*
  - *Imitation Learning (IL)* / *Aprenentatge per imitació*
  - *Reinforcement Learning (RL)* / *Aprenentatge per reforç*
  - *Sim2Real transfer* / *Transferència Sim2Real*
  - *Agentic AI* / *IA agèntica*
- Correct the GRAIL project title to **"Generative Robotics & AI for EU Industrial Leadership"**.
- Verify that TIAGo PRO, Franka Emika Panda, and NVIDIA Isaac Lab are prominently detailed in the technical descriptions.

### Directives for Storytelling Agent:
- Rewrite the project summaries to highlight the narrative arc: from foundational VR garment folding (TFG / ICRA 2023) to dynamic RL in simulation (TFM / Isaac Lab) to state-of-the-art multimodal VLA foundation models deployed on physical mobile manipulators (COGNITIUM / MWC 2026 / GRAIL).
- Upgrade the Catalan tone in `altres-cat.html`, replacing *"Popurri d'altres coses que faig en el meu temps lliure"* with a professional framing of leadership and service to the robotics community.

### Directives for UX/UI Designer:
- Fix the CSS variable discrepancy for `--accent`: align the comment and hover state so button colors do not flash from khaki (`#a09369`) to blue (`#0369a1`).
- Fix the broken language switcher link in `eng/altres-eng.html` (`href="../cat/altres-cat.html"`).
- Fix the secret button link in `eng/main-eng.html` or provide an `eng/wip.html`.
- Fix the mixed-up citation link for CCIA 2022 in `articles-cat.html` and `articles-eng.html`.
- Enhance the image carousel with mobile touch swipe and bullet indicators, and embed video players where available.

### Directives for Recruiter & QA Reviewer:
- Test all external URLs (`arxiv.org`, `digital.csic.es`, `upcommons.upc.edu`, `ieeexplore.ieee.org`, `youtube.com`).
- Validate that all internal links between `cat/` and `eng/` mirror each other seamlessly with zero 404 errors.
