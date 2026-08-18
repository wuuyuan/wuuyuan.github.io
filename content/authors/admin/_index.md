---
# Display name
title: Shuai Liu (Jesse)

# Name pronunciation (optional)
name_pronunciation: ''

# Full name (for SEO)
first_name: Shuai
last_name: Liu

# Pronouns (optional)
pronouns: he/him

# Status emoji
status:
  icon: ''

# Is this the primary user of the site?
superuser: true

# Highlight the author in author lists? (true/false)
highlight_name: true

# Role/position/tagline
role: Embodied Foundation Model Researcher

# Organizations/Affiliations to display in Biography blox
organizations:
  - name: Shanghai Jiao Tong University
    url: https://www.sjtu.edu.cn/

# Social network links
profiles:
  - icon: at-symbol
    url: 'mailto:liushuai0902@sjtu.edu.cn'
    label: E-mail Me
  - icon: brands/github
    url: https://github.com/wuuyuan
  - icon: brands/linkedin
    url: https://www.linkedin.com/in/shuai-liu-922a73373
  - icon: academicons/google-scholar
    url: https://scholar.google.com/citations?user=PIY1ibQAAAAJ&hl=en
  - icon: academicons/orcid
    url: https://orcid.org/0009-0001-4325-0646

interests:
  - Embodied foundation models
  - VLA / world models
  - RL post-training
  - Physics-based simulation
  - Tactile simulation
  - GPU computing

education:
  - area: PhD Mechanical Engineering
    institution: Shanghai Jiao Tong University
    icon: ""
    date_start: 2022-09-01
    date_end: 2027-06-30
    summary: |
      Expected June 2027. Research on embodied foundation models — simulation-based post-training of VLA and world-model policies, with high-fidelity physics simulation as the data and evaluation substrate. 12 SCI papers (5 first-author, including *J. Fluid Mech.*, *Phys. Fluids*, and *J. Sound Vib.*). National Scholarship (2025).
  - area: B.Eng. Mechanical Engineering (Honors / Elite Class)
    institution: Xi'an Jiaotong University
    icon: ""
    date_start: 2018-09-01
    date_end: 2022-06-30
    summary: |
      GPA 90.89/100 (top 3.5%). SMC First-Class Scholarship and Outstanding Student Award.

work:
  - position: Research Intern, RL Post-Training for Robot Foundation Models
    company_name: AgiBot
    company_url: 'https://www.agibot.com/'
    logo: logos/agibot.png
    logo_bg: light
    icon: ''
    date_start: 2026-06-01
    date_end: ''
    summary: |
      Developing scalable, simulation-based reinforcement learning post-training for embodied manipulation with vision–language–action (VLA) and world-model architectures. Contributing to distributed PPO/GRPO training pipelines, including rollout, inference, and multi-node training for generalizable dexterous manipulation.
  - position: Research Intern, Embodied-AI Simulation Engines
    company_name: Lightwheel
    company_url: 'https://lightwheel.ai/'
    logo: logos/lightwheel.png
    logo_bg: dark
    icon: ''
    date_start: 2026-01-01
    date_end: 2026-04-30
    summary: |
      Built embodied-AI simulation and synthetic-data pipelines with Genesis, Newton, and NVIDIA Warp, improving throughput by 2.6× for contact-rich pretraining data, policy evaluation, and sim-to-real alignment. Led a high-performance tactile simulator in Newton and NVIDIA Isaac Lab with equivalent-thickness flexible-body formulations (5–10× mesh reduction, over 50 Hz tactile-grasp throughput). Built a closed-loop sim-to-real / real-to-sim pipeline coupling FEM sensing, rigid–flexible contact, and IPC.
  - position: Research Intern, GPU Computing Infrastructure
    company_name: Synopsys
    company_url: 'https://www.synopsys.com/'
    logo: logos/synopsys.jpg
    logo_bg: brand
    icon: ''
    date_start: 2025-07-01
    date_end: 2025-10-31
    summary: |
      Optimized GPU solver operators and linear-algebra libraries for physics simulation with shared-memory tiling and register-level acceleration, achieving about 1.3× average speedup on production workloads across H100/L40 clusters. Optimized batched GEMM kernels with a two-stage shared-memory pipeline (about 1.2× average, up to 1.5×).

# Skills
skills:
  - name: Embodied models and post-training
    items:
      - name: VLA / world models
        description: Vision–language–action models, world models, and simulation-based RL post-training
        icon: cpu-chip
      - name: Reinforcement learning
        description: PPO, GRPO, model-based RL, and sim-to-real policy transfer
        icon: chart-bar
  - name: Simulation
    items:
      - name: Physics solvers
        description: FEM / FVM / ALE, IPC, fluid–structure–acoustic coupling, OpenFOAM, preCICE
        icon: cube
      - name: Robot simulation
        description: Genesis, Newton, Warp, Isaac Sim/Lab, tactile and deformable-body simulation
        icon: cube-transparent
  - name: Computing
    items:
      - name: Systems
        description: C/C++, Python, PyTorch, CUDA, MPI/OpenMP, multi-GPU training
        icon: code-bracket

languages:
  - name: Chinese
    percent: 100
  - name: English
    percent: 90

# Awards.
awards:
  - title: National Scholarship for Doctoral Students
    url: ''
    date: '2025-12-01'
    awarder: Ministry of Education of the People's Republic of China
    icon: hero/academic-cap
    summary: |
      Awarded for doctoral research in physics-based simulation and learning-based control.
  - title: National First Prize, Intelligent Manufacturing
    url: ''
    date: '2021-12-01'
    awarder: 3rd China College Students Mechanical Engineering Innovation Competition
    icon: hero/trophy
    summary: |
      National First Prize and First Prize in Industrial Vision. Led robot–vision integration for a physical production line, including manipulator programming, automated grasping, vision-based detection and pose estimation, and a PLC/OPC UA perception–action loop.
---

Shuai Liu (Jesse) is an **embodied foundation model researcher** and a PhD candidate in Mechanical Engineering at Shanghai Jiao Tong University. He works on simulation-based post-training of vision–language–action (VLA) and world-model policies for robot foundation models, and on the physics simulators, tactile engines, and RL systems that make that post-training scale.

The physics line underneath — high-fidelity FEM/FVM/ALE solvers, DMD/Koopman latent world models, and multimodal RL — supplies data, evaluation environments, and control structure for embodied models. He has published 12 SCI papers, including 5 first-author papers in *J. Fluid Mech.*, *Phys. Fluids*, *J. Sound Vib.* (×2), and *Sensors and Actuators A*.
