# PRISM: Personalized Refinement of Imitation Skills for Manipulation via Human Instructions

## Metadata
- **Publication Venue:** European Robotics Forum (ERF 2026)
- **Preprint / Repository:** arXiv:2603.05574 ([https://arxiv.org/abs/2603.05574](https://arxiv.org/abs/2603.05574))
- **Video Demonstration:** [https://www.youtube.com/watch?v=yUUkD1LsCWY](https://www.youtube.com/watch?v=yUUkD1LsCWY)
- **Authors:** **Arnau Boix-Granell** (First Author), Alberto San-Miguel-Tello, Magí Dalmau-Moreno, Néstor García
- **Affiliations:** Eurecat, Technological Center of Catalonia & UPC
- **Media Asset:** `../imatges/Article3.svg`

---

## English Version

### The Challenge
Imitation Learning (IL) offers an intuitive mechanism for non-experts to teach robots tasks by recording demonstrations. However, standard IL policies suffer from poor out-of-distribution generalization: when the physical setup, obstacle locations, or user requirements change slightly, the policy fails. Conversely, retraining Reinforcement Learning (RL) policies from scratch requires expert reward engineering and enormous sample complexity. The core challenge was to create an interactive, unified pipeline where an existing demonstration policy can be rapidly adapted to new constraints and configurations using natural language and human-in-the-loop feedback without manual reward coding.

### Arnau's Direct Contributions
- **Conceptual Architecture & Method Formulation:** Conceived, formulated, and led the development of PRISM as first author, integrating Imitation Learning and Reinforcement Learning into a cohesive skill refinement framework.
- **LLM-Driven Reward Synthesis (Eureka Extension):** Extended the state-of-the-art Eureka framework to iteratively synthesize and optimize RL reward functions directly from high-level natural language prompts describing target behaviors and spatial constraints.
- **Interactive Human-in-the-Loop Refinement:** Implemented real-time human correction mechanisms allowing supervisors to guide intermediate policy rollouts, instantly correcting suboptimal trajectories and enforcing safety constraints.
- **Isaac Lab Benchmarking Environment:** Built GPU-accelerated simulation environments in **NVIDIA Isaac Lab**, establishing rigorous empirical benchmarks for pick-and-place and obstacle-avoidance manipulation tasks under domain shift.
- **Lead Paper Authorship:** Conducted ablation studies, generated technical figures, and authored the scientific manuscript presented at the European Robotics Forum 2026.

### Results & Metrics
- **Dramatic Performance Elevation:** Under challenging constraint-shift conditions, the baseline imitation policy achieved only **21.2% success rate**. Through PRISM's Isaac Lab RL refinement, the policy achieved **98.0% success rate**.
- **LLM Prompt + Human Feedback Synergy:** Combining iterative GPT-5 Eureka prompt reward refinement with interactive human feedback corrections achieved **96.8% success rate** under strict out-of-distribution constraints.
- **Data & Compute Efficiency:** Drastically lowered the demonstration data requirements and computation time compared to training new policies from scratch.

### Hardware & Stack
- **Simulation Environment:** NVIDIA Isaac Lab, NVIDIA Isaac Sim.
- **Software Stack:** Python, PyTorch, Large Language Models (GPT-5 / Eureka framework), ROS 2, Imitation Learning, Reinforcement Learning.

---

## Versió en Català

### Títol Oficial
**PRISM: Personalized Refinement of Imitation Skills for Manipulation via Human Instructions** *(Refinament Personalitzat d'Habilitats d'Imitació per a la Manipulació mitjançant Instruccions Humanes)*

### El Repte
L'aprenentatge per imitació (IL) permet ensenyar habilitats als robots de manera intuïtiva mitjançant demostracions guiades. Tanmateix, les polítiques apreses presenten una capacitat de generalització deficient davant situacions fora de la distribució original: qualsevol variació en la posició d'un obstacle o en les restriccions espacials provoca el fracàs de la tasca. D'altra banda, reentrenar agents de RL des de zero requereix una complexa enginyeria manual de funcions de recompensa i milions d'interaccions. El repte consistia a formular un mètode unificat que permeti adaptar una política d'imitació genèrica a nous escenaris i restriccions mitjançant llenguatge natural i retroalimentació humana interactiva sense programar recompenses a mà.

### Aportacions Directes d'Arnau
- **Concepció i Lideratge Metodològic:** Formulació i disseny integral de PRISM com a primer autor, unint l'aprenentatge per imitació i l'aprenentatge per reforç en un mateix flux de refinament d'habilitats.
- **Generació de Recompenses amb LLMs (Extensió Eureka):** Adaptació del paradigma d'última generació Eureka per sintetitzar i refinar funcions de recompensa de RL de forma iterativa mitjançant models de llenguatge a partir de descripcions verbals de la tasca.
- **Correcció Humana en Bucle Tancat (*Human-in-the-Loop*):** Implementació de mecanismes de correcció en temps real que permeten a l'operador humà reorientar les trajectòries intermèdies i imposar límits de seguretat.
- **Desenvolupament Experimental a Isaac Lab:** Creació d'entorns de proves paral·lels a **NVIDIA Isaac Lab** per avaluar de forma empírica tasques de subjecció, transport i col·locació (*pick-and-place*) amb obstacles imprevistos.
- **Redacció de l'Article Científic:** Execució d'estudis d'ablació, anàlisi de resultats i redacció de la publicació presentada a l'European Robotics Forum 2026.

### Resultats i Mètriques
- **Millora Radical de Rendiment:** Davant condicions amb noves restriccions geomètriques, la política base d'imitació només assolia un **21,2% d'èxit**. Mitjançant el refinament per reforç a Isaac Lab, PRISM va elevar l'èxit fins al **98,0%**.
- **Sinergia LLM + Retroalimentació Humana:** La combinació de refinament de recompenses amb GPT-5 (Eureka) i intervencions humanes en bucle va assolir una taxa d'èxit del **96,8%** en configuracions altament exigents fora de distribució.
- **Eficiència Computacional:** Reducció notable del volum de dades requerit i del cost de càlcul respecte a l'aprenentatge des de zero.

### Maquinari i Tecnologies
- **Entorn de Simulació:** NVIDIA Isaac Lab, NVIDIA Isaac Sim.
- **Entorn de Programari:** Python, PyTorch, Models de Llenguatge (GPT-5 / Eureka), ROS 2, IL, RL.
