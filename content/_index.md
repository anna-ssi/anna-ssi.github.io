---
title: 'Anna Hakhverdyan's homepage'
date: 2024-09-25
type: landing

sections:
  - block: resume-biography
    id: about
    content:
      # The user's folder name in content/authors/
      username: admin
    design:
      spacing:
        padding: [0, 0, 0, 0]
      biography:
        style: 'text-align: justify; font-size: 0.8em;'
        
  - block: collection
    id: pubs
    content:
      title: Publications
      text: |-
      filters:
        folders:
          - publication
    design:
      columns: '1'
      view: citation
---
