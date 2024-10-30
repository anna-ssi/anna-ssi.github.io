---
title: ''
date: 2024-09-25
type: landing

design:
  # Default section spacing
  spacing: "5rem"

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
  - block: resume-experience
    id: exp
    content:
      username: anna
    design:
      # Hugo date format
      date_format: 'January 2006'
      # Education or Experience section first?
      is_education_first: true
  - block: resume-skills
    content:
      title: Skills & Hobbies
      username: anna
    design:
      show_skill_percentage: false
      title_align: center

  - block: resume-languages
    content:
      title: Languages
      username: anna
    design:
      show_skill_percentage: false
---
