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
      button:
        text: Download CV
        url: uploads/Anna_CV.pdf
    design:
      spacing:
        padding: ['60px', '0', '60px', '0']
      biography:
        style: 'text-align: justify; font-size: 1em;'
  - block: collection
    id: pubs
    content:
      title: Publications
      text: ""
      filters:
        folders:
          - publication
      exclude_featured: false
    design:
      view: citation
---
