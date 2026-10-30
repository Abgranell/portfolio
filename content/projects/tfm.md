# Master's Thesis (TFM): Reinforcement Learning for Complex and Dynamic Manipulation Tasks

## Metadata
- **Institution:** Universitat Politècnica de Catalunya (UPC ETSEIB) & Fundació Eurecat
- **Period:** September 2023 – January 2025 (Formally Defended January 31, 2025)
- **Degree:** Double Master's Degree in Automatic Control & Robotics Engineering and Industrial Engineering
- **Academic Distinction:** Grade 10 / 10 with Honors (*Matrícula d'Honor*)
- **Advisors:** Dr. Néstor García Hidalgo (Eurecat) and Prof. Jan Rosell Gratacòs (UPC / IOC)
- **UPCommons Handle:** `https://hdl.handle.net/2117/428855` (Publication Handle: `579551cc-36d6-441e-a54d-ec78524d9299`)
- **Media Asset:** `../imatges/tfm2.gif`

---

## English Version

### The Challenge
Executing non-prehensile and dynamic manipulation tasks—such as unlatching and opening a hinged dishwasher door—represents an intricate challenge in robotics. Closed kinematic loops, dynamic friction transitions, varying spring resistance, and contact discontinuities render traditional motion planning and fixed-gain position control brittle and prone to jamming. Training policies with Reinforcement Learning (RL) within physics simulators offers a promising alternative, yet overcoming the severe discrepancy between simulated contact models and real physical dynamics (the Sim2Real gap) remains the central obstacle to practical robotic deployment.

### Arnau's Direct Contributions
- **High-Performance Simulation Framework:** Built an advanced simulation benchmark in **NVIDIA Isaac Sim** and **Isaac Lab**, exploiting GPU tensor parallelization to train Deep RL agents across thousands of simultaneous instances.
- **Dynamic Task Modeling:** Accurately modeled the nonlinear joint kinematics, latch resistance, and inertial dynamics of a commercial dishwasher door and mechanical latch.
- **Curriculum & Reward Formulation:** Designed specialized reward structures and curriculum learning stages that enabled the Franka Emika Panda robotic manipulator to coordinate its end-effector trajectory, grasp compliance, and continuous pulling force without losing contact.
- **Sim2Real Transfer Methodology:** Evaluated and implemented system identification and domain randomization strategies (friction coefficients, actuator dynamics, observation latency) to ensure policy resilience against unmodeled physical perturbations.
- **Physical ROS 2 Bridge:** Established an asynchronous ROS 2 communication bridge between Isaac Sim/Lab and physical hardware, successfully verifying Sim2Real policy execution on a real **Franka Emika Panda** robot arm.

### Results & Impact
- Successfully trained a robust RL policy capable of dynamically approaching, latching, and fully opening a simulated dishwasher door across diverse initial conditions.
- Achieved stable zero-shot physical deployment of simpler policy primitives over ROS 2 on the physical Franka Panda robot.
- Formally defended before the academic tribunal at UPC ETSEIB on January 31, 2025, receiving the maximum grade of 10/10 with Honors (*Matrícula d'Honor*).

### Hardware & Stack
- **Hardware:** Franka Emika Panda 7-DOF robotic manipulator, workstation with NVIDIA RTX GPU.
- **Software Stack:** NVIDIA Isaac Sim, NVIDIA Isaac Lab, ROS 2, PyTorch, Python, PhysX.

---

## Versió en Català

### Títol Oficial
**Treball de Fi de Màster (TFM): Reinforcement Learning for Complex and Dynamic Manipulation Tasks** *(Aprenentatge per Reforç per a Tasques de Manipulació Dinàmica i Complexa)*

### El Repte
L'execució de tasques de manipulació dinàmica amb restriccions cinemàtiques tancades —com ara desencallar el pestell i obrir la porta abatible d'un rentavaixelles— constitueix un repte d'alta dificultat en robòtica. Les variacions en les forces de fricció, la resistència de les molles internes i la transició sobtada de contactes fan que el control posicional rígid clàssic sigui ineficaç i provoqui bloquejos mecànics. L'aprenentatge per reforç (RL) en entorns simulats permet descobrir patrons de moviment adaptatius, però la discrepància entre els motors de física i la realitat (la bretxa Sim2Real) suposa un gran obstacle per al seu funcionament sobre robots físics.

### Aportacions Directes d'Arnau
- **Arquitectura de Simulació en GPU:** Disseny d'un entorn de simulació avançat a **NVIDIA Isaac Sim** i **Isaac Lab**, aprofitant el processament paral·lel en GPU per accelerar l'entrenament de milers d'agents de RL en paral·lel.
- **Modelatge Físic de l'Entorn:** Reconstrucció precisa del model cinemàtic i dinàmic del rentavaixelles, parametritzant les resistències de la frontissa i els mecanismes d'enclavament de la porta.
- **Estratègia de Recompenses i Aprenentatge Progressiu:** Formulació de funcions de recompensa i fases d'aprenentatge progressiu (*curriculum learning*) que van permetre al braç Franka Emika Panda coordinar trajectòries adaptatives mantenint la força de tracció contínua.
- **Investigació de Tècniques Sim2Real:** Anàlisi i implementació d'estratègies d'aleatorització de domini (coeficients de fricció, inèrcies i retards de comunicació) per garantir la robustesa de les polítiques davant imprecisions del model.
- **Pont de Comunicació en ROS 2:** Desenvolupament d'un canal de control en ROS 2 per connectar l'entorn de simulació amb el maquinari real, validant la transferència de tasques bàsiques sobre un braç robòtic físic Franka Emika Panda.

### Resultats i Impacte
- Entrenament exitós d'una política de RL robusta capaç d'obrir la porta d'un rentavaixelles simulat davant diferents condicions inicials.
- Verificació experimental de la transferència de moviments al robot real Franka Panda mitjançant ROS 2.
- Defensat el 31 de gener de 2025 davant el tribunal de la UPC ETSEIB amb una qualificació de 10/10 amb Matrícula d'Honor.

### Maquinari i Tecnologies
- **Maquinari:** Braç articulat Franka Emika Panda (7 DoF), GPU NVIDIA RTX.
- **Entorn de Programari:** NVIDIA Isaac Sim, NVIDIA Isaac Lab, ROS 2, Python, PyTorch, PhysX.
