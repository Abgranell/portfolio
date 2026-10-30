# VR Framework for Learning from Demonstration & Garment Manipulation (ICRA 2023, CCIA 2022 & TFG)

## Metadata
- **Core Venues & Milestones:**
  - **IEEE ICRA 2023:** *A Virtual Reality Framework for Fast Dataset Creation Applied to Cloth Manipulation with Automatic Semantic Labelling* (DOI: `10.1109/ICRA48891.2023.10161122`)
  - **CCIA 2022:** *Garment Manipulation Dataset for Robot Learning by Demonstration Through a Virtual Reality Framework* (DOI: `10.3233/FAIA220334`) — First Author
  - **Bachelor's Thesis (TFG):** *Development of a Learning from Demonstration Environment Using ZED 2i and HTC Vive Pro* (Handles: `10261/304847` & `2117/372083`) — Grade: 10/10 with Honors (*Matrícula d'Honor*)
- **Host Institutions:** Institut de Robòtica i Informàtica Industrial (IRI, CSIC-UPC) & UPC ETSEIB
- **Advisors & Co-Authors:** Dr. Sergi Foix, Dr. Júlia Borràs, Prof. Carme Torras, Dr. Arnau Dòria-Cerezo
- **Media Assets:** `../imatges/Article2.jpg`, `../imatges/Article1.svg`, `../imatges/tfg1.PNG`, `../imatges/tfg2.PNG`, `../imatges/tfg3.PNG`

---

## English Version

### The Challenge
Teaching dual-arm robotic systems to manipulate deformable objects, such as folding clothes, represents one of the most notoriously difficult problems in robotic manipulation. Unlike rigid bodies, textiles possess infinite degrees of freedom, self-occlude constantly, and deform nonlinearly under the slightest contact forces. Existing datasets were either captured via physical RGB-D cameras (where garment self-occlusion makes state tracking impossible) or generated via open-loop simulation without natural human visual-feedback reflexes, yielding stiff and unrealistic robotic demonstrations.

### Arnau's Direct Contributions
- **Full VR Framework Development:** Engineered an interactive, real-time Virtual Reality demonstration framework in Unity 3D, combining the **HTC Vive Pro** VR ecosystem, **Stereolabs ZED 2i / ZED Mini** depth cameras, and **Leap Motion** optical hand tracking.
- **Physics & Interaction Integration:** Implemented realistic real-time deformable cloth physics within the VR environment, enabling human demonstrators to naturally grasp, drag, fold, and release garments using either handheld controllers or bare hands.
- **Closing the Perception-Action Loop:** Created an architecture that leverages natural human hand-eye visual feedback during demonstrations while simultaneously recording ground-truth 3D mesh vertices, bypassing physical occlusion limitations.
- **Automatic Semantic State Labelling:** Designed and coded a novel low-dimensional topological representation that automatically segments and labels cloth states into semantic folding stages without requiring manual annotation.
- **Dataset Creation & Dissemination:** Generated and publicly released a benchmark dataset comprising 19 distinct cloth manipulation sequences and actions, co-authoring scientific papers presented at **IEEE ICRA 2023** (London) and **CCIA 2022**.

### Results & Impact
- Successfully resolved the trade-off between human sensory feedback and precise ground-truth mesh tracking for deformable object learning.
- Published at the premier global robotics conference (IEEE ICRA 2023) and led publication at CCIA 2022.
- Formed the core of Arnau's Bachelor's Thesis, awarded 10/10 with Honors (*Matrícula d'Honor*) at UPC ETSEIB.

### Hardware & Stack
- **Hardware:** HTC Vive Pro (HMD and controllers), Stereolabs ZED 2i & ZED Mini stereo depth cameras, Leap Motion controller.
- **Software Stack:** Unity 3D Engine, C++, C#, MATLAB, ROS 2, SteamVR.

---

## Versió en Català

### Títol Oficial
**Entorn de Realitat Virtual per a l'Aprenentatge per Demostració i Manipulació de Teixits (ICRA 2023, CCIA 2022 i TFG)**

### El Repte
L'ensenyament de tasques de manipulació d'objectes deformables —com ara el plegat de roba— a robots de dos braços és un dels reptes més complexos de la robòtica actual. A diferència dels objectes rígids, els teixits tenen infinits graus de llibertat, pateixen constants autooclusions visuals i es deformen de manera altament no lineal al mínim contacte. Els conjunts de dades existents fins aleshores es dividien entre captures reals amb càmeres (on l'oclusió impedeix conèixer l'estat intern del teixit) o simulacions en bucle obert sense participació humana, les quals generen moviments rígids i allunyats de la naturalitat del moviment humà.

### Aportacions Directes d'Arnau
- **Desenvolupament Integral de l'Entorn VR:** Disseny i programació d'una plataforma interactiva de Realitat Virtual a Unity 3D, combinant el sistema **HTC Vive Pro**, càmeres estereoscòpiques **Stereolabs ZED 2i / ZED Mini** i el sensor de mans **Leap Motion**.
- **Modelatge Físic i Interacció Tèxtil:** Integració de física realista de teixits deformables en temps real, permetent als usuaris subjectar, estirar i doblegar peces de roba virtuals de forma intuïtiva mitjançant comandaments manuals o les pròpies mans.
- **Tancament del Bucle Percepció-Acció:** Creació d'una arquitectura que aprofita la retroalimentació visual de la persona mentre registra amb precisió matemàtica l'estat tridimensional exacte de cada vèrtex de la malla virtual, eliminant qualsevol biaix per oclusió.
- **Etiquetatge Semàntic Automàtic:** Disseny d'una representació topològica innovadora de baixa dimensió capaç d'etiquetar i segmentar automàticament els estats del teixit durant el procés de manipulació sense intervenció manual.
- **Publicació del Conjunt de Dades:** Generació i alliberament d'un *dataset* obert amb 19 categories diferents de manipulació tèxtil, presentat a la conferència internacional de màxim prestigi **IEEE ICRA 2023** (Londres) i a **CCIA 2022** (com a primer autor).

### Resultats i Impacte
- Solució pionera a la bretxa entre la retroalimentació visual humana i la traçabilitat de geometries deformables complexes per a robots.
- Publicació a la conferència mundial líder en robòtica (IEEE ICRA 2023) i autoria principal a CCIA 2022.
- Distinció de Treball de Fi de Grau amb màxima qualificació (10/10, Matrícula d'Honor) a la UPC ETSEIB.

### Maquinari i Tecnologies
- **Maquinari:** Casc i comandaments HTC Vive Pro, càmeres Stereolabs ZED 2i i ZED Mini, sensor Leap Motion.
- **Entorn de Programari:** Unity 3D, C++, C#, MATLAB, ROS 2, SteamVR.
