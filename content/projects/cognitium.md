# COGNITIUM: Autonomous & Integrated Cognition for Robots in Unpredictable & Multimodal Environments

## Metadata
- **Project Type:** Applied R&D Project
- **Host Institution:** Eurecat, Technological Center of Catalonia
- **Period:** 2025 – 2026
- **Role:** Robotics Researcher
- **Hardware Platform:** PAL Robotics TIAGo PRO / TIAGo Mobile Manipulator
- **Official URL:** [https://eurecat.org/portfolio-items/cognitium/](https://eurecat.org/portfolio-items/cognitium/)
- **Demonstration Video:** [https://www.youtube.com/watch?v=zPSblj-a-5c](https://www.youtube.com/watch?v=zPSblj-a-5c)
- **Media Assets:** `../imatges/Cobnitium_Logo.webp`, `../imatges/cognitium_MWC_1.jfif`, `../imatges/cogntitium_mwc.gif`

---

## English Version

### The Challenge
Deploying autonomous mobile manipulators in unconstrained, crowded human environments requires handling unpredictable physical disturbances, changing scene layouts, and ambiguous human commands. Traditional pipeline architectures separate SLAM, task planning, and motion planning into brittle cascading modules where perception errors easily cause total execution failure. The COGNITIUM project sought to implement an integrated, cognitive architecture leveraging frontier Vision-Language-Action (VLA) foundation models and agentic Vision-Language Models (VLMs) to achieve robust, real-time closed-loop manipulation on a full-scale mobile robotic manipulator.

### Arnau's Direct Contributions
- **VLA Model Benchmarking:** Designed and conducted a systematic benchmarking evaluation across frontier open-source and proprietary Vision-Language-Action (VLA) architectures to select the optimal model balancing inference latency, spatial precision, and generalization capacity.
- **LeRobot Framework Integration:** Configured and adapted the **Hugging Face LeRobot** ecosystem to interface directly with the hardware control layers of the physical **PAL Robotics TIAGo PRO / TIAGo** robot.
- **VLA Fine-Tuning & Policy Deployment:** Trained, fine-tuned, and deployed sensorimotor manipulation policies from teleoperated demonstration datasets, achieving autonomous grasp and placement of varied target objects directly from onboard camera streams.
- **Agentic VLM Reasoning Engine:** Formulated and deployed an agentic VLM supervisory framework acting as an executive reasoner, evaluating task success, re-prompting low-level policies upon unexpected object movement, and orchestrating multi-modal dialogue with human users.
- **High-Profile Live Demonstration:** Programmed, calibrated, and conducted live autonomous robotic manipulation demonstrations at the **Mobile World Congress (MWC) Barcelona 2026**, successfully performing tasks under real-world auditorium interference, intense dynamic lighting, and dense crowds.

### Results & Impact
- Validated real-time closed-loop manipulation execution running natively on the physical TIAGo mobile manipulator.
- Showcased reliable error recovery driven by agentic visual feedback without human teleoperation intervention during live public demonstrations.
- Presented Eurecat's cutting-edge cognitive robotics capabilities to thousands of international industry executives and researchers at MWC 2026.

### Hardware & Stack
- **Hardware:** PAL Robotics TIAGo PRO / TIAGo mobile manipulator, onboard RGB-D cameras, high-performance edge compute.
- **Software Stack:** Hugging Face LeRobot, Vision-Language-Action (VLA) models, Vision-Language Models (VLM), Agentic AI, ROS 2, Python, PyTorch.

---

## Versió en Català

### Títol Oficial
**COGNITIUM: Cognició Generalitzada i Integrada per a Robots en Entorns Impredictibles i Multimodals**

### El Repte
El desplegament de manipuladors mòbils autònoms en entorns quotidians amb presència humana exigeix gestionar pertorbacions físiques inesperades, canvis continus en la disposició dels objectes i instruccions verbals ambigües. Les arquitectures tradicionals desconnecten la percepció, la navegació i el control motor en subsistemes aïllats altament sensibles a errors de calibratge. El projecte COGNITIUM va plantejar el desenvolupament d'una arquitectura cognitiva unificada que combina models fundacionals de Visió-Llenguatge-Acció (VLA) amb models de Visió i Llenguatge (VLM) agèntics per assolir una manipulació robusta en bucle tancat sobre un robot mòbil d'escala real.

### Aportacions Directes d'Arnau
- **Banc de Proves (*Benchmarking*) de Models VLA:** Disseny i execució d'un estudi comparatiu rigorós de diverses arquitectures VLA de codi obert i propietàries per determinar el model amb millor equilibri entre latència d'inferència, precisió espacial i capacitat de generalització.
- **Integració de la Plataforma LeRobot:** Adaptació i integració de la biblioteca **Hugging Face LeRobot** amb la capa de control de baix nivell del manipulador mòbil físic **PAL Robotics TIAGo PRO / TIAGo**.
- **Entrenament i Desplegament de Polítiques:** Adaptació (*fine-tuning*) i validació de polítiques neuronals de manipulació basades en dades de demostració, aconseguint la subjecció i reubicació autònoma d'objectes no vistos prèviament a partir de la càmera del robot.
- **Orquestració Agèntica amb VLMs:** Implementació d'un agent de raonament basat en VLM encarregat de supervisar la correcta execució de les tasques, detectar fallades de subjecció i reajustar les accions de forma autònoma davant d'obstacles imprevistos.
- **Demostració en Directe al Mobile World Congress:** Posada a punt, calibratge i operació de la demostració robòtica autònoma en directe al **Mobile World Congress (MWC) Barcelona 2026**, executant tasques de manipulació interactiva amb públic davant de condicions lumíniques complexes i canvis constants en l'entorn.

### Resultats i Impacte
- Validació experimental amb èxit del desplegament de models VLA en temps real sobre el robot mòbil TIAGo.
- Capacitat de recuperació autònoma davant pertorbacions físiques mitjançant el bucle de realimentació de l'agent VLM.
- Difusió tecnològica d'alt impacte davant la comunitat industrial i tecnològica internacional congregada al MWC 2026.

### Maquinari i Tecnologies
- **Maquinari:** Manipulador mòbil PAL Robotics TIAGo PRO / TIAGo, càmeres RGB-D integrades, unitat de càlcul GPU embarcada.
- **Entorn de Programari:** Hugging Face LeRobot, models VLA, models VLM, IA agèntica, ROS 2, Python, PyTorch.
