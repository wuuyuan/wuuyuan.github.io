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
        I build **simulation-to-learning systems** for physical and embodied AI.

        The work has three connected lines:

        1. **Explicit physics.** High-fidelity FEM/FVM/ALE solvers for fluid–structure–electrical–acoustic interaction and large-deformation flexible bodies, used as data engines and evaluation environments.
        2. **Implicit world models.** DMD/Koopman latent next-state prediction over high-fidelity physical fields, enabling model-based RL in latent space.
        3. **Learning-based control.** Multimodal reinforcement learning, learned sensor–actuator gain networks, and sim-to-real transfer — recently extended to simulation-based post-training of embodied foundation models.

        Please [email me](mailto:liushuai0902@sjtu.edu.cn) if you would like to collaborate.
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: citation
      columns: 1
  - block: collection
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: true
    design:
      view: citation
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
