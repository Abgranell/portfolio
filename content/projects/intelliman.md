# INTELLIMAN: AI-Powered Manipulation System for Advanced Robotic Service, Manufacturing and Prosthetics

## Metadata
- **Project Type:** European Union Horizon Europe Research Project
- **Host Institution:** Eurecat (Consortium Member; Project led by University of Bologna, with DLR, IIT, etc.)
- **Period:** 2022 – 2026
- **Role:** Robotics Researcher
- **Hardware Platform:** Franka Emika Panda 7-DOF Robotic Arm
- **Simulation Platforms:** NVIDIA Isaac Sim, NVIDIA Isaac Lab
- **Official URL:** [https://intelliman-project.eu/](https://intelliman-project.eu/)
- **Media Assets:** `../imatges/Intelliman_logo.svg`, `../imatges/intelliman.gif`

---

## English Version

### The Challenge
Developing robots capable of performing complex manipulation tasks—such as dynamically grasping delicate objects, sorting recyclable industrial waste, or handling household appliances—requires policies that can adapt to variable friction, mass distributions, and non-rigid surface contacts. Traditional Reinforcement Learning (RL) trained purely in physical reality is prohibitively slow, dangerous, and sample-inefficient. Conversely, policies trained exclusively in simulation typically fail when transferred to physical manipulators due to discrepancies in contact physics, sensor noise, and actuator latency (the Sim2Real gap).

### Arnau's Direct Contributions
- **Deep RL Environment Modeling:** Formulated and developed dynamic manipulation tasks in **NVIDIA Isaac Sim** and **Isaac Lab**, utilizing GPU-parallelized physics to simulate thousands of environments concurrently.
- **Imitation Learning Pre-Training:** Utilized Imitation Learning (IL) policies derived from expert demonstrations to initialize Deep RL agents, cutting exploration time by orders of magnitude and resolving exploration bottlenecks in complex sequential tasks.
- **Domain Randomization & Sim2Real Bridging:** Formulated comprehensive domain randomization pipelines across physical parameters (mass, restitution, friction coefficients, surface textures, joint dampening) to ensure zero-shot policy robustness during physical deployment.
- **Real-Time 3D Object Pose Tracking:** Adapted and integrated 6-DoF spatial object pose estimation algorithms to feed continuous Cartesian state observations to the active RL policy.
- **Physical Robot Interface:** Implemented low-latency ROS 2 control bridges to execute simulation-trained policies directly on physical **Franka Emika Panda** manipulators.

### Results & Impact
- Drastically reduced policy convergence time by combining imitation demonstration priors with massively parallelized GPU reinforcement learning.
- Successfully demonstrated reliable physical transfer of complex manipulation behaviors from Isaac Lab onto physical Franka Panda manipulators without physical policy re-tuning.
- Delivered foundational research milestones on circular economy and domestic manipulation for the EU Horizon Europe INTELLIMAN project.

### Hardware & Stack
- **Hardware:** Franka Emika Panda 7-DOF collaborative robotic arm, depth vision sensors.
- **Software Stack:** NVIDIA Isaac Sim, NVIDIA Isaac Lab, ROS 2, Python, PyTorch, Deep Reinforcement Learning (PPO), Imitation Learning.

---

## Versió en Català

### Títol Oficial
**INTELLIMAN: Sistema de Manipulació Basat en IA per a Serveis Robòtics Avançats, Manufactura i Pròtesis**

### El Repte
Capacitar braços robòtics per dur a terme tasques de manipulació dinàmica d'alta complexitat —com la manipulació d'electrodomèstics, la subjecció d'objectes fràgils o el reciclatge d'elements industrials— exigeix polítiques de control capaces d'adaptar-se a variacions contínues en la massa, la fricció i les geometries. L'aprenentatge per reforç (RL) aplicat directament sobre robots físics és lent, perillós per a la integritat del maquinari i ineficient en consum de dades. D'altra banda, les polítiques apreses únicament en simulació solen fallar estrepitosament en la realitat a causa de les diferències en la dinàmica de contactes i els retards dels actuadors (la bretxa Sim2Real).

### Aportacions Directes d'Arnau
- **Modelatge d'Entorns de RL en GPU:** Desenvolupament d'entorns de manipulació dinàmica d'alta fidelitat a **NVIDIA Isaac Sim** i **Isaac Lab**, aprofitant l'acceleració per GPU per simular milers d'instàncies paral·leles d'aprenentatge simultani.
- **Acceleració mitjançant Aprenentatge per Imitació:** Implementació de polítiques prèvies d'aprenentatge per imitació (IL) a partir de demostracions expertes per inicialitzar els agents de RL, evitant fases d'exploració aleatòria ineficients i accelerant dràsticament la convergència de l'entrenament.
- **Mitigació de la Bretxa Sim2Real:** Disseny d'estratègies avançades d'aleatorització de domini (*domain randomization*), variant coeficients de fricció, inèrcies, latències i soroll sensorial per blindar la política davant les incerteses del món real.
- **Seguiment Espacial 3D d'Objectes:** Adaptació i integració d'algoritmes d'estimació de posició i orientació 3D (6-DoF) en temps real per alimentar les polítiques de control amb l'estat precís dels objectes manipulats.
- **Integració amb el Robot Físic:** Configuració de comunicacions de baixa latència en **ROS 2** per connectar les polítiques apreses amb la interfície de control del braç articulat **Franka Emika Panda**.

### Resultats i Impacte
- Reducció dràstica del temps d'entrenament dels agents mitjançant la combinació híbrida d'imitació i reforç paral·lelitzat.
- Transferència reeixida de polítiques des d'Isaac Lab al manipulador físic Franka Panda sense necessitat d'ajust manual sobre el robot.
- Compliment dels objectius científics i industrials d'Eurecat en el marc del consorci europeu INTELLIMAN.

### Maquinari i Tecnologies
- **Maquinari:** Braç robòtic col·laboratiu Franka Emika Panda (7 DoF), sensors de visió 3D.
- **Entorn de Programari:** NVIDIA Isaac Sim, NVIDIA Isaac Lab, ROS 2, Python, PyTorch, PPO, Aprenentatge per Imitació.
