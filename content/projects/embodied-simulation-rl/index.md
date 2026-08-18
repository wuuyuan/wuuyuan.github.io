---
title: Embodied Simulation and RL Post-Training
date: 2026-06-01
summary: Tactile/embodied simulation engines and simulation-based reinforcement learning post-training for robot foundation models.
tags:
  - embodied AI
  - tactile simulation
  - RL post-training
---

The third line takes physics simulation into **embodied AI**.

On the data/simulation side, GPU-parallel engines (Genesis, Newton, Warp, Isaac Lab) are used for contact-rich synthetic data, tactile-grasp simulation, and sim-to-real / real-to-sim calibration. Equivalent-thickness flexible-body formulations reduce mesh cost while keeping rates high enough for online RL.

On the model side, the same simulation substrate is used for distributed reinforcement-learning post-training of vision–language–action and world-model policies, including rollout, inference, and multi-node training pipelines for dexterous manipulation.
