---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '3rem'

sections:
  # Hero section - clean intro only
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: View Projects
        url: projects/
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      # Clean gradient background for readability
      background:
        gradient_start: '#1e3a8a'
        gradient_end: '#0f172a'
        text_color_light: true

      # Name heading sizing to accommodate long or short names
      name:
        size: md # Options: xs, sm, md, lg (default), xl

      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded

  - block: markdown
    content:
      title: 'My Work'
      subtitle: ''
      text: |-
        I work on geospatial data science projects combining remote sensing, machine learning, and data visualization. My research focuses on using satellite imagery and spatial data to address challenges in agriculture, climate change, and environmental monitoring.

        From mapping paddy fields using multi-temporal satellite imagery to analyzing urban land cover patterns, I enjoy solving real-world problems with data and technology.

        Please reach out to collaborate!
    design:
      columns: '1'

  - block: collection
    id: publications
    content:
      title: Publications
      subtitle: ''
      text: 'Peer-reviewed research in agricultural remote sensing and machine learning.'
      count: 5
      filters:
        folders:
          - publications
        publication_type: ''
    design:
      view: citation
      columns: 1

  - block: collection
    id: projects
    content:
      title: Featured Projects
      subtitle: ''
      text: 'Explore my portfolio of geospatial data science, machine learning, and data visualization projects.'
      sort_by: 'Params.weight'
      sort_ascending: true
      filters:
        folders:
          - projects
    design:
      view: article-grid
      columns: 3
      fill_image: false
---
