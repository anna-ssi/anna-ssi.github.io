---
title: 'Home'
date: 2024-09-25
type: landing

sections:
  - block: resume-biography-3
    content:
      # The user's folder name in content/authors/
      username: anna
      text: ""
    design:
      spacing:
        padding: ['60px', '0', '60px', '0']
      biography:
        style: 'text-align: justify; font-size: 1em;'
  - block: markdown
    id: research
    content:
      title: 'Current Research Projects'
      subtitle: ''
      text: |-
        Use this area to speak to your mission. I'm a research scientist in the Moonshot team at DeepMind. I blog about machine learning, deep learning, and moonshots.

        I apply a range of qualitative and quantitative methods to comprehensively investigate the role of science and technology in the economy.
        
    design:
      columns: '1'
      style: 'text-align: justify; font-size: .8em;'
  - block: collection
    id: pubs
    content:
      title: Publications
      text: ""
      filters:
        folders:
          - publication
    design:
      view: citation
---
