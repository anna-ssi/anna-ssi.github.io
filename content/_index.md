---
title: 'Home'
date: 2024-09-25
type: landing

sections:
  - block: resume-biography
    content:
      # The user's folder name in content/authors/
      username: admin
    design:
      spacing:
        padding: [0, 0, 0, 0]
      biography:
        style: 'text-align: justify; font-size: 0.8em;'
        
  - block: collection
    id: featured
    content:
      title: Publications
      text: 
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      columns: '1'
      view: citation
---
