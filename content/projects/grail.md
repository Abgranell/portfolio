# GRAIL: Generative Robotics & AI for EU Industrial Leadership

## Metadata
- **Project Type:** Flagship EU Horizon Europe Research & Innovation Programme (€40M Budget)
- **Host Institution:** Eurecat, Technological Center of Catalonia (Coordinator)
- **Consortium:** ~20 leading research institutes and industrial leaders (Siemens, ETH Zurich, DLR, Imperial College London, Barcelona Supercomputing Center - BSC, among others)
- **Period:** 2026 – Present
- **Role:** Robotics Researcher
- **Official Website:** [https://grail-robotics.ai/](https://grail-robotics.ai/)
- **Media Asset:** `../imatges/GRAIL_Logo.png`

---

## English Version

### The Challenge
European manufacturing and logistics face increasing demand for high-mix, low-volume production that traditional fixed-automation pipelines cannot accommodate. Existing industrial robots rely on rigid, pre-programmed trajectories designed by expert engineers, which fail when encountering novel geometries, component misalignments, or unstructured human-robot workspaces. Achieving true industrial autonomy demands sovereign European foundation models capable of reasoning about natural language instructions, visually inspecting dynamic environments, and generating generalized manipulation actions in real time.

### Arnau's Direct Contributions
- **VLM Reasoning Architecture:** Designed and implemented reasoning modules utilizing state-of-the-art Vision-Language Models (VLMs) to interpret high-level natural language instructions and break them down into structured symbolic sub-goals and spatial manipulation primitives.
- **VLA Physical Embodiment:** Integrated Vision-Language-Action (VLA) neural architectures directly onto physical industrial manipulators, establishing direct sensorimotor mapping from RGB-D observations to joint-space/Cartesian velocity commands.
- **Multimodal Demonstration Pipelines:** Developed teleoperation setups using low-latency controllers to collect high-fidelity multimodal human demonstration datasets (video, proprioception, joint torques, language prompts) for generative policy training.
- **Safety and Reliability Constraints:** Formulated closed-loop verification mechanisms ensuring that generative policy rollouts adhere strictly to physical workspace boundaries and collision avoidance bounds.

### Results & Impact
- Enabled autonomous decomposition of multi-step industrial assembly and sorting instructions without task-specific trajectory engineering.
- Established a foundational European training and evaluation pipeline for sovereign embodied intelligence in industrial automation.
- Contributing directly to Eurecat’s core technical deliverables within a €40M pan-European flagship consortium.

### Hardware & Stack
- **Hardware:** Industrial collaborative manipulators, RGB-D perception systems, teleoperation interfaces.
- **Software Stack:** Vision-Language-Action (VLA) architectures, Agentic VLMs, PyTorch, ROS 2, Linux.

---

## Versió en Català

### Títol Oficial
**GRAIL: Generative Robotics & AI for EU Industrial Leadership** *(Robòtica Generativa i IA per al Lideratge Industrial de la Unió Europea)*

### El Repte
El teixit industrial i logístic europeu afronta una creixent demanda de producció d'alta variabilitat i tirades curtes que l'automatització rígida convencional és incapaç de satisfer. Els robots industrials actuals depenen de trajectòries codificades de manera determinista, les quals fallen davant de petites variacions en la posició de les peces, canvis en la geometria dels components o entorns de treball no estructurats. Assolir una autonomia industrial real requereix el desenvolupament de models fundacionals europeus sobirans, capaços de raonar sobre instruccions en llenguatge natural, inspeccionar visualment l'entorn i executar accions de manipulació generalitzables en temps real.

### Aportacions Directes d'Arnau
- **Arquitectura de Raonament amb VLMs:** Disseny i integració de mòduls cognitius basats en models de Visió i Llenguatge (VLM) per interpretar comandes en llenguatge natural i descompondre-les en subobjectius simbòlics i primitives de manipulació espacial.
- **Corporització de Models VLA:** Integració de xarxes Visió-Llenguatge-Acció (VLA) en plataformes robòtiques físiques, establint un mapatge directe (*end-to-end*) des de les observacions sensorials visuals fins a consignes de velocitat en l'espai articular i cartesià.
- **Captura de Demostracions Multimodals:** Desenvolupament de sistemes de teleoperació de baixa latència per capturar conjunts massius de dades de demostració experta (imatge, propiocepció, parells articulars i anotacions d'àudio/text) destinats a l'entrenament de polítiques d'IA generativa.
- **Supervisió de Seguretat Física:** Implementació de mecanismes de verificació en bucle tancat per assegurar que les accions generades per les xarxes neuronals respectin estrictament els límits de l'espai de treball i les restriccions d'evitació de col·lisions.

### Resultats i Impacte
- Descomposició i execució autònoma d'instruccions complexes de muntatge i classificació sense necessitat de programació explícita de trajectòries.
- Consolidació de la infraestructura tecnològica d'IA generativa sobirana dins del consorci de referència Horizon Europe de 40M€ coordinat per Eurecat.

### Maquinari i Tecnologies
- **Maquinari:** Robots col·laboratius industrials, càmeres RGB-D industrials, dispositius de teleoperació.
- **Entorn de Programari:** Models VLA, VLMs agèntics, PyTorch, ROS 2, Linux.
