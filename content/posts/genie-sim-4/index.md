---
title: 'Genie Sim 4.0'
summary: 'What Genie Sim 4.0 is for, what I worked on during the AgiBot internship, and which results belong to the GenieSim Team.'
date: '2026-11-02'
authors:
  - admin
tags:
  - Embodied AI
  - Simulation
  - Reinforcement Learning
---

Genie Sim 4.0 is public. The report is titled *Genie Sim: Towards the Next Generation of Embodied Intelligence*, and it is signed by the GenieSim Team. I was part of that team while interning at AgiBot, from June through October 2026. This note says what the platform is for, which pieces I worked on, and which results belong to the team. A shorter page, with the same links, is the [project card](/projects/genie-sim/).

## What the platform is for

Robot foundation models are trained in stages. After vision and language, a policy still has to learn contact, timing, and whether a grasp holds. Simulation is where that stage can be repeated. Genie Sim 4.0 keeps simulation, evaluation, and model improvement on one loop: a scene is where data are collected, where a policy is rolled out, and where the same task can be scored again after training.

That loop works when the simulator, the benchmark, and the trainer agree on what a step is. The release treats them as parts of one platform. Physics supplies the interaction. Evaluation supplies the question asked of the policy. The training stack has to consume both at the scale a foundation model requires. The public project page and the technical report describe the platform in full, including the measurements. This note stays at the level of the loop itself.

## What I worked on

My share was the training side of that loop. Three pieces, all in service of post-training.

The first is simulation-based RL post-training. A robot foundation model already carries a prior from demonstration and earlier training. Post-training is the stage that lets interaction move the policy: the model proposes an action, the simulator steps, and a reward says whether the task advanced. For manipulation, the trainer has to stay stable while the policy, the camera, and the scene change underneath it.

The second is the physics simulation used for that training. Post-training is only as useful as the contact it rolls out. The simulator has to expose rigid and deformable interaction at a rate the trainer can call, and it has to reset cleanly, so that one environment's episode does not decide the next. I worked on the simulation this training loop calls.

The third is the RL infrastructure around rollout, inference, and multi-node training. A large policy does not sit inside the simulator process. Inference produces an action chunk, simulation advances, and the next observation comes back. Across machines, that exchange has to overlap with stepping, or the GPUs wait. Scheduling environments, keeping inference busy while another environment steps, and scaling the update past a single node are the plumbing under the algorithm, whether the update is PPO or GRPO.

## What the team reports

Foundation-model capability in the release is a team result. Genie Sim 4.0 is aimed at policies that follow instructions, hold up as the scene changes, and keep working as the set of tasks grows. The comparisons behind that claim live in the technical report. I was on the team that built the stack those comparisons use. The headline capability is the team's.

Fine manipulation is a team result as well. Contact-rich skills — aligning small parts, using tools, keeping a grasp while the rest of the arm moves — are part of what the platform is meant to train and to measure. They depend on the simulator and on the post-training loop. They also depend on benchmarking, data collection, and model work distributed across the team. The release reports progress on that front. That progress is the team's, and the report is the place to read it.

## Links

- [Project page](https://agibot-world.com/genie-sim)
- [Code](https://github.com/AgibotTech/genie_sim)
- [Technical report](https://agibot-world.com/genie-sim/report/)
