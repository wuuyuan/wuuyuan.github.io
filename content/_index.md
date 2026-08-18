---
# Leave the homepage title empty to use the site title
title: ''
date: 2026-08-18
type: landing

design:
  spacing: '6rem'

sections:
  - block: resume-biography-3
    content:
      username: admin
      text: ''
      button:
        text: Download CV
        url: uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      css_class: hbx-bg-gradient
      avatar:
        size: medium
        shape: circle
  - block: markdown
    content:
      title: 'Research'
      subtitle: ''
      text: |-
        I am an **embodied foundation model researcher**. The core of the work is simulation-based post-training of vision–language–action (VLA) and world-model policies for robot foundation models.

        Physics simulation is the substrate that makes that post-training possible, along three connected lines:

        1. **Embodied post-training.** Distributed PPO/GRPO and related RL pipelines for VLA, world-model, and world-action-model policies, with simulators as rollout and evaluation engines for generalizable dexterous manipulation.
        2. **Implicit world models.** DMD/Koopman latent next-state prediction over high-fidelity physical fields, enabling model-based RL in latent space.
        3. **Explicit physics.** High-fidelity FEM/FVM/ALE solvers for fluid–structure–electrical–acoustic interaction and large-deformation flexible bodies, used as data engines and evaluation environments — including tactile and contact-rich robot simulation.

        Please [email me](mailto:liushuai0902@sjtu.edu.cn) if you would like to collaborate.
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Featured Publications
      count: 0
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: paper-row
      columns: 1
      fill_image: false
      show_date: false
      show_read_time: false
      show_read_more: false
  - block: collection
    content:
      title: Recent Publications
      text: ''
      count: 0
      filters:
        folders:
          - publications
        exclude_featured: true
    design:
      view: paper-row
      columns: 1
      fill_image: false
      show_date: false
      show_read_time: false
      show_read_more: false
  - block: collection
    id: talks
    content:
      title: Talks
      filters:
        folders:
          - events
    design:
      view: card
  - block: collection
    id: news
    content:
      title: Recent News
      subtitle: ''
      text: ''
      page_type: blog
      count: 5
      filters:
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ''
      offset: 0
      order: desc
    design:
      view: card
      spacing:
        padding: [0, 0, 0, 0]
---
