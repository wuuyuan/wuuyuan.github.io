---
title: Genie Sim 4.0
date: 2026-11-02
summary: GenieSim Team release of a simulation platform that connects physics simulation, evaluation, and model improvement for embodied intelligence.
tags:
  - embodied AI
  - simulation
  - RL post-training
---

**GenieSim Team.** *Genie Sim: Towards the Next Generation of Embodied Intelligence.*

Genie Sim 4.0 is a simulation platform for embodied intelligence. It keeps simulation, evaluation, and model improvement on one loop: scenes are simulated, tasks are scored, and policies are trained against those same tasks. The release covers reinforcement-learning post-training of robot foundation models, physics-simulation engines for rigid and deformable interaction, and the RL infrastructure that runs rollout and training together. It also reports gains in foundation-model capability and in fine manipulation. Those capability gains are results of the team.

Physics simulation is the substrate of the loop. Engines for contact, deformation, and robot dynamics supply the states a policy trains on and the scenes a benchmark scores. RL post-training then uses that simulator as the environment: the model acts, the scene steps, and the update is driven by task success. The infrastructure under that update — parallel rollout, inference, and multi-node training — is what makes the loop large enough for a foundation model.

I was part of the GenieSim Team while interning at AgiBot from June to October 2026. My work was the simulation-based RL post-training, the physics simulation used for that training, and the RL infrastructure for rollout, inference, and multi-node training.

- [Project page](https://agibot-world.com/genie-sim)
- [Code](https://github.com/AgibotTech/genie_sim)
- [Technical report](https://agibot-world.com/genie-sim/report/)
