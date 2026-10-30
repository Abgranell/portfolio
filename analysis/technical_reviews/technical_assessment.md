# Exhaustive Robotics Technical Review & Project Assessments
*Compiled by Robotics Technical Editor*

## 1. Standardized Robotics & AI Bilingual Glossary

| English Term | Catalan Standard Term | Technical Context & Usage Constraint |
| :--- | :--- | :--- |
| **Vision-Language-Action (VLA) Model** | *Model de Visió-Llenguatge-Acció (VLA)* | End-to-end foundation model mapping multimodal tokens (RGB image + language instruction) directly to robot end-effector / joint actions. |
| **Vision-Language Model (VLM)** | *Model de Visió-Llenguatge (VLM)* | Multimodal reasoning model used for semantic scene decomposition, spatial reasoning, and high-level agentic task planning. |
| **Imitation Learning (IL) / Learning from Demonstration (LfD)** | *Aprenentatge per imitació (IL) / Aprenentatge per demostració (LfD)* | Learning policies from expert trajectories (Behavioral Cloning, teleoperation rollouts). |
| **Reinforcement Learning (RL)** | *Aprenentatge per reforç (RL)* | Policy optimization (e.g., PPO/SAC) through environment interaction and reward maximization. |
| **Prompt-Conditioned Policy Refinement** | *Refinament de polítiques condicionat per instruccions* | Adapting a pre-trained base policy to unseen constraints using iterative natural-language prompts. |
| **LLM-Driven Reward Synthesis (Eureka)** | *Síntesi de recompenses guiada per LLM (Eureka)* | Algorithmic generation and evolutionary refinement of code-level reward functions using LLMs. |
| **Sim2Real Transfer & Domain Randomization** | *Transferència de simulació a realitat (Sim2Real) i aleatorització de domini* | Closing dynamic/perceptual reality gaps through parametric randomization of physics, inertia, friction, and visual textures. |
| **Mobile Manipulator** | *Manipulador mòbil* | Holonomic or differential base paired with an articulated arm (specifically PAL Robotics TIAGo / TIAGo PRO). |
| **Contact-Rich Dynamic Manipulation** | *Manipulació dinàmica amb contacte ric* | Manipulation involving discontinuous force profiles, mechanical latches, friction transitions, and closed kinematic chains. |
| **Deformable Object Manipulation** | *Manipulació d'objectes deformables* | Manipulation of non-rigid textiles or garments characterized by infinite degrees of freedom and severe visual occlusion. |
| **Low-Dimensional Semantic State Representation** | *Representació d'estat semàntica de baixa dimensionalitat* | Topological or keypoint-based state encoding abstracting mesh complexity into discrete manipulation states. |

---

## 2. Project-by-Project Exhaustive Technical Assessments

### 2.1 GRAIL — Generative Robotics & AI for EU Industrial Leadership
- **Official Designation:** Horizon Europe Flagship Initiative (€40M+ total investment, ~20 partner institutions led by Eurecat).
- **Core Problem:** Bridging semantic generalization (understanding complex natural language commands) with high-frequency, safety-critical continuous joint execution in industrial manufacturing.
- **System Architecture:** Hierarchical agentic framework decoupling high-level Vision-Language Models (VLM reasoning) from low-level continuous Vision-Language-Action (VLA) execution and teleoperation demonstration acquisition pipelines.
- **Arnau's Contributions:**
  1. Integrating VLM reasoning engines to interpret unstructured natural-language instructions into structured task plans.
  2. Deploying and evaluating VLA foundation models on physical robotic manipulators for instruction-based control.
  3. Designing human-in-the-loop teleoperation workflows to record multimodal demonstration datasets.

### 2.2 COGNITIUM — Autonomous & Integrated Cognition in Multimodal Environments
- **Platform:** PAL Robotics TIAGo Pro / TIAGo mobile manipulator (7-DOF arm, mobile base, multimodal head).
- **Software Toolchain:** Hugging Face LeRobot open-source framework, OpenVLA, Agentic VLM reasoning.
- **Core Problem:** Real-time edge inference of billion-parameter models on physical robots, handling self-occlusions, and coordinate frame transforms under unscripted environments.
- **Arnau's Contributions:**
  1. Systematic benchmarking of open-source and proprietary VLA architectures.
  2. Training and fine-tuning VLA policies using Hugging Face LeRobot.
  3. Direct physical deployment and closed-loop control on the PAL Robotics TIAGo mobile manipulator.
  4. Implementing high-level Agentic VLM supervision for error recovery.
  5. Live physical demonstration presentation at Mobile World Congress (MWC) Barcelona 2026.

### 2.3 INTELLIMAN — AI-Powered Robotic Manipulation for Service, Manufacturing and Prosthetics
- **Platform & Simulation:** Franka Emika Panda 7-DOF manipulator, NVIDIA Isaac Sim, NVIDIA Isaac Lab (GPU-accelerated PhysX 5).
- **Core Problem:** Dynamic contact-rich manipulation involving spring-loaded latch mechanisms (opening dishwasher doors).
- **Methods:** Deep Reinforcement Learning (PPO) accelerated by Imitation Learning demonstration pre-training, paired with domain randomization across dynamic and friction parameters to bridge the reality gap.
- **Arnau's Contributions:**
  1. Building GPU-accelerated parallel simulation environments in Isaac Lab.
  2. Formulating imitation pre-training strategies to bypass exploration bottlenecks.
  3. Implementing domain randomization regimes for Sim2Real transfer.
  4. Integrating 6D object pose tracking with ROS 2 sensor pipelines.

### 2.4 PRISM — Personalized Refinement of Imitation Skills via Human Instructions (ERF 2026)
- **Venue & Citation:** European Robotics Forum (ERF 2026) · arXiv:2603.05574.
- **Authors:** **Arnau Boix-Granell** (1st Author), Alberto San-Miguel-Tello, Magí Dalmau-Moreno, Néstor García.
- **Core Innovation:** Prompt-conditioned imitation policy refinement using GPT-5 driven Eureka reward synthesis combined with interactive human feedback rollouts in NVIDIA Isaac Lab.
- **Empirical Benchmarks:**
  - Zero-shot unrefined baseline: **21.2%** success.
  - Isaac Lab RL convergence: **98.0%** convergence.
  - PRISM with human feedback: **96.8%** empirical success with dramatic sample complexity reduction.
- **Arnau's Contributions:** Conceived the theoretical framework, implemented simulation environments in Isaac Lab, developed the prompt-engineering feedback loop, executed empirical benchmarks, and served as lead author.

### 2.5 Master's Thesis (TFM) — RL for Complex and Dynamic Manipulation Tasks
- **Degree:** Double Master's Degree in Industrial Technologies and Automatic Control & Robotics (UPC ETSEIB & Eurecat).
- **Defense Date:** January 31, 2025 (Average Master's GPA: 9.02/10, 12 Honors). Handle: `hdl.handle.net/2117/428855`.
- **Core Achievement:** Developed a GPU-accelerated parallel simulation framework in NVIDIA Isaac Sim and Isaac Lab, training PPO agents to operate spring-loaded dishwasher doors. Implemented domain randomization and established a ROS 2 hardware bridge to physical Franka Emika Panda.
- **Correction:** Must never be labeled as a "treball de fi de grau" in Catalan.

### 2.6 ICRA 2023 & Bachelor's Thesis (TFG) — VR Garment Manipulation & Semantic Labelling
- **Venue & Citation:** IEEE International Conference on Robotics and Automation (ICRA 2023) · DOI: `10.1109/ICRA48891.2023.10161122`.
- **Bachelor's Thesis:** Defended July 2022 at UPC ETSEIB & IRI CSIC-UPC (Matrícula d'Honor; Bachelor's GPA: 8.88/10, Ranked 2nd of 298 engineers). Handles: `hdl.handle.net/10261/304847` & `hdl.handle.net/2117/372083`.
- **Core Innovation:** Immersive VR environment in Unity 3D integrating HTC Vive Pro, Stereolabs ZED 2i/Mini stereo cameras, and Leap Motion hand tracking to record human demonstrations of cloth manipulation. Developed a low-dimensional topological representation that automatically classifies cloth configurations into 19 manipulation categories.
- **Citation Fix:** Article 2 is ICRA 2023; Article 3 is CCIA 2022 (IOS Press / DIGITAL.CSIC `10261/281403`).

### 2.7 AIxHRI Summer School — Advanced AI for Human-Robot Interaction
- **Host:** Inria / Loria (Nancy, France) & AI Grand Est ENACT (July 2026).
- **Focus:** Intensive doctoral training in multimodal foundation models, VLA fine-tuning, RLHF on physical platforms, and safe HRI.

### 2.8 Engihack 2024 — EcoShower Project (1st Prize Winner)
- **Organizer & Achievement:** Col·legi d'Enginyers Industrials de Catalunya (EIC) · 1st Prize Winner (€3,000) with team *InduBotics*. Featured on TV3 program *Tot es mou*.
- **Mechatronic Focus:** Automated fluidic recirculation system with electromechanical bypass valving and inline thermal sensors eliminating water waste during shower warm-up.

---

## 3. Mandatory Technical Guidelines for Storytelling Agent & UX/UI Designer

1. **Title Integrity:** Always use official names ("Generative Robotics & AI for EU Industrial Leadership"; "PRISM: Personalized Refinement of Imitation Skills for Manipulation via Human Instructions"; Master's Thesis for TFM).
2. **Empirical Precision:** State the PRISM benchmark figures (21.2% baseline, 98.0% Isaac Lab RL, 96.8% with human feedback).
3. **Exact Hardware & Toolchains:** Specify PAL Robotics TIAGo Pro, Franka Emika Panda, NVIDIA Isaac Lab, Hugging Face LeRobot, ROS 2, and HTC Vive Pro.
4. **Citation Disambiguation:** Link ICRA 2023 to IEEE Xplore (`10.1109/ICRA48891.2023.10161122`) and CCIA 2022 to IOS Press (`10.3233/FAIA220334`) / DIGITAL.CSIC.
5. **Professional Tone:** Reframe "Altres / Others" as "Community, Leadership & Professional Initiatives", highlighting the euRobotics Diversity and Inclusion Initiative (DII).
