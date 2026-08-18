---
title: Embodied Foundation Models and Simulation RL
date: 2026-06-01
summary: Simulation-based reinforcement learning post-training for robot foundation models, with tactile and contact-rich simulation as the substrate.
tags:
  - embodied AI
  - tactile simulation
  - RL post-training
---

The core line is **embodied foundation models**: simulation-based reinforcement-learning post-training of vision–language–action and world-model policies for generalizable dexterous manipulation.

On the model side, GPU-parallel simulators drive distributed PPO/GRPO pipelines, including rollout, inference, and multi-node training. On the data/simulation side, Genesis, Newton, Warp, and Isaac Lab generate contact-rich synthetic data and tactile-grasp streams, with equivalent-thickness flexible-body formulations that keep rates high enough for online RL.

High-fidelity physics is the substrate, not the destination — it supplies the data engine, the evaluator, and the sim-to-real / real-to-sim loop for robot foundation models.
