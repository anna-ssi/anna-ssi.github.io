---
# Leave the homepage title empty to use the site title
title: Shushan Arakelyan's homepage
date: 2023-08-06
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Bio
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: shushan
  - block: collection
    id: featured
    content:
      title: Featured Publications
      text: |-
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      columns: '2'
      view: card
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Student Researcher
          company: Microsoft Research
          company_url: ''
          company_logo: ''
          location: Seattle, WA, USA/Remote
          date_start: '2022-09-01'
          date_end: '2023-03-01'
          description: Working on large language models for code and their generalization. The resulting paper is currently under review.
        - title: Software Engineering Intern
          company: Google
          company_url: ''
          company_logo: ''
          location: London, UK
          date_start: '2018-05-01'
          date_end: '2018-08-01'
          description: Worked on Google Assistant. Researched and developed methods for descriptions of user profiles for use with recommender systems. The resulting paper appeared in SIGIR'19.
        - title: Machine Learning Research Engineer
          company: Qube
          company_url: ''
          company_logo: ''
          location: Yerevan, Armenia
          date_start: '2016-10-01'
          date_end: '2017-08-01'
          description: Researching, designing and prototyping state of the art algorithms for computer graphics, image processing, 3D optimization and face reenactment from RGB input.
        - title: Software Engineering Intern
          company: Google
          company_url: ''
          company_logo: ''
          location: New York, NY, USA
          date_start: '2015-06-01'
          date_end: '2015-09-01'
          description: Worked on Google Cloud Logging Infrastructure
        - title: Software Engineer
          company: OneMarketData
          company_url: ''
          company_logo: ''
          location: Yerevan, Armenia
          date_start: '2013-04-01'
          date_end: '2015-05-01'
          description: Worked on company’s OneTick line
        - title: Junior C++ Engineer
          company: Questrade
          company_url: ''
          company_logo: ''
          location: Yerevan, Armenia
          date_start: '2012-08-01'
          date_end: '2013-03-01'
          description: Worked on company’s trading platform front end - a transaction processing application.
    design:
      columns: '2'
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      email: first name at isi dot edu
      contact_links:
        - icon: twitter
          icon_pack: fab
          name: DM Me
          link: 'https://twitter.com/sharakelyan'
      # Automatically link email and phone or display as text?
      autolink: false
      # Email form provider
    design:
      columns: '2'
---
