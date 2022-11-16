---
# An instance of the Portfolio widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: portfolio

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 70

title: Codes
subtitle: ''

content:
  # Page type to display. E.g. project.
  page_type: code

  # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
  filter_default: 1

  # Filter toolbar (optional).
  # Add or remove as many filters (`filter_button` instances) as you like.
  # To show all items, set `tag` to "*".
  # To filter by a specific tag, set `tag` to an existing tag name.
  # To remove the toolbar, delete the entire `filter_button` block.
  filter_button:
    - name: All
      tag: '*'
    - name: 21cm Theory
      tag: Theory
    - name: Structure Formation
      tag: hmf
    - name: Analysis Pipelines
      tag: pipeline
    - name: Tools
      tag: tool
    - name: Collaborative
      tag: Collaborative
    - name: My Codes
      tag: Mine



design:
  # Choose how many columns the section has. Valid values: '1' or '2'.
  columns: '1'

  # Toggle between the various page layout types.
  #   1 = List
  #   2 = Compact
  #   3 = Card
  #   5 = Showcase
  view: showcase
  #showcase

  # For Showcase view, flip alternate rows?
  flip_alt_rows: true
---
