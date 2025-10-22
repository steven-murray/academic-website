---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: steven
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/cv.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      # Apply a gradient background
      # css_class: hbx-bg-gradient
      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded


  # - block: collection
  #   id: papers
  #   content:
  #     title: Featured Publications
  #     filters:
  #       folders:
  #         - publication
  #       featured_only: true
  #   design:
  #     view: article-grid
  #     columns: 2

  # # - block: collection
  # #   content:
  # #     title: Recent Publications
  # #     text: ''
  # #     filters:
  # #       folders:
  # #         - publications
  # #       exclude_featured: false
  # #   design:
  # #     view: citation
  
  # - block: collection
  #   id: talks
  #   content:
  #     title: Recent & Upcoming Talks
  #     filters:
  #       folders:
  #         - event
  #   design:
  #     view: article-grid
  #     columns: 3
  
  # - block: collection
  #   id: projects
  #   content:
  #     title: My Projects
  #     filters:
  #       folders:
  #         - project
  #     #count: 4
  #   design:
  #     view: article-grid
  #     columns: 3

  # - block: collection
  #   id: software

  #   content:
  #     title: Software

  #     # Page type to display. E.g. project.
  #     filters:
  #       folders:
  #         - software

  #     count: 6

  #   design:
  #     view: article-grid
  #     columns: 3
          
  # - block: collection
  #   id: posts
  #   content:
  #     title: Recent Posts
  #     subtitle: ''
  #     text: ''
  #     # Page type to display. E.g. post, talk, publication...
  #     page_type: post
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 5
  #     # Filter on criteria
  #     filters:
  #       author: ''
  #       category: ''
  #       tag: ''
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ''
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: article-grid
  #     # Number of columns (for grid/card views)
  #     columns: 3
---
