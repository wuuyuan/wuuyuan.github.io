---
title: 'Why Simulation Is the Substrate for Embodied Foundation Models'
summary: An opening note on this blog — how physics simulation, world models, and RL post-training fit together, and the series I plan to write.
date: '2026-09-11'
authors:
  - admin
tags:
  - Embodied AI
  - World Models
  - Reinforcement Learning
  - Simulation
---

This blog collects notes on embodied foundation models — the vision–language–action (VLA) and world-model policies that sit between raw sensor streams and robot actuation — and on the infrastructure that makes them trainable. Most posts will orbit one claim:

> Physics simulation is the substrate that post-training for embodied models is built on.

That is a strong statement, so let me unpack it, then sketch the series I intend to write here.

## Three roles for simulation

In the current paradigm, robot foundation models are *post-trained* rather than purely pre-trained: a policy is first aligned with internet-scale vision–language data, then fine-tuned with interaction data so that it can *act*. Simulation enters that pipeline in three distinct roles.

1. **Data engine.** High-fidelity physics simulators generate the contact-rich, dexterous manipulation data that is too slow, expensive, or dangerous to collect on real hardware — tactile signals, deformable-object states, and failure cases included.
2. **Rollout and evaluation environment.** Reinforcement learning needs millions of environment steps. The simulator is the rollout engine for PPO/GRPO-style post-training and the scoring environment for sim-to-real evaluation.
3. **Inductive bias.** A world model learned over simulated dynamics carries physics structure into the policy — continuity, contact constraints, and momentum conservation — which transfers better than structure learned from web video alone.

## What the post-training objective looks like

The backbone of current embodied post-training is an on- or off-policy objective over trajectories $\tau = (s_0, a_0, r_0, \dots)$ collected from the simulator:

$$
J(\theta) = \mathbb{E}_{\tau \sim \pi_\theta}\left[\sum_{t=0}^{T} \gamma^t \, r_t\right] - \beta\,\mathrm{KL}\left(\pi_\theta \,\|\, \pi_{\mathrm{ref}}\right),
$$

where the KL term keeps the fine-tuned policy from drifting away from the pre-trained VLA. GRPO replaces the learned value function with group-wise reward normalization, which is one reason it has become the default for multi-GPU rollout of large policies.

A minimal rollout loop captures the whole idea:

```python
for rollout in range(num_rollouts):
    obs = env.reset()
    for step in range(horizon):
        action = policy(obs)          # VLA head
        obs, reward, done = env.step(action)
        buffer.add(obs, action, reward, done)
        if done:
            break
advantages = group_normalize(buffer.returns())   # GRPO
policy.update(buffer, advantages)                # policy gradient
```

Everything interesting is hidden in `env` — that is where the physics, the contact models, and the tactile sensing live.

## Planned series

- **Embodied post-training.** PPO/GRPO at scale: rollout parallelism, advantage normalization, and why simulation throughput, not model size, is often the bottleneck.
- **Implicit world models.** DMD/Koopman latent next-state prediction over physical fields, and model-based RL in latent space.
- **Explicit physics engines.** FEM/FVM/ALE solvers for fluid–structure–acoustic interaction and deformable bodies — the substrate underneath the data engines.
- **Engineering notes.** CUDA kernel optimization, multi-node training, and sim-to-real alignment: the unglamorous work that determines whether any of the above runs at all.

Posts will be in English for the most part, with occasional Chinese write-ups on the same topics. You can subscribe to the [RSS feed](/posts/index.xml) if you prefer to read that way.
