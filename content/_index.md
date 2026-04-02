---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: hero
    id: about
    content:
      title: |
        Research Lab for
        **Advancing Science**
      text: |
        We are a leading research group focused on pushing the boundaries of knowledge through innovative research and collaboration. Our multidisciplinary team works on cutting-edge projects at the intersection of technology and science.
      primary_action:
        text: Join Our Team
        url: '#team'
        icon: hero/user-group
      secondary_action:
        text: View Publications
        url: '#publications'
        icon: hero/academic-cap
      announcement:
        text: "We are hiring PhD students and postdocs!"
        link:
          text: "Apply now"
          url: "/opportunities"
    design:
      # For full-screen, add `min-h-screen` below
      css_class: ""
      background:
        # Option A: Modern gradient mesh (recommended for 2025/2026)
        gradient_mesh:
          enable: true
          style: "waves"
          animation: "pulse"
          intensity: "medium"
          colors:
            - "primary-500/30"
            - "blue-600/20"
            - "indigo-600/15"
        
        # Option B: Team/lab image (uncomment to use instead of gradient mesh)
        # image:
        #   filename: "team-lab-hero.jpg"
        #   filters:
        #     brightness: 0.6
        #     contrast: 1.1

  - block: stats
    content:
      items:
        - statistic: "50+"
          description: Publications in top-tier journals
          sub_metric: Nature, Science, Cell, PNAS
          icon: hero/document-text
        - statistic: "15"
          description: Brilliant researchers and scientists
          sub_metric: From 8 countries worldwide
          icon: hero/user-group
        - statistic: "$5M"
          description: Active research funding
          sub_metric: NSF, NIH, DOE grants
          icon: hero/currency-dollar
        - statistic: "12"
          description: Active research projects
          sub_metric: Across 3 major domains
          icon: hero/beaker
    design:
      layout: cards
      # Section background color (CSS class)
      css_class: "bg-gradient-to-b from-primary-50 to-white dark:from-primary-900/20 dark:to-gray-800"
      spacing:
        padding: ["3rem", 0, "3rem", 0]

  - block: research-areas
    content:
      title: Research Focus Areas
      subtitle: Pushing the Boundaries of Science
      text: Our lab conducts cutting-edge research across multiple domains, combining computational methods with experimental validation
      items:
        - name: Computational Biology
          description: Developing state-of-the-art algorithms for genomic analysis, protein structure prediction, and systems biology modeling
          icon: hero/beaker
          gradient: from-green-400 to-emerald-600
          status: active
          topics:
            - Genomics
            - Proteomics
            - Bioinformatics
            - Systems Biology
            - Drug Discovery
          team_size: 12
          publications: 45+
          funding: $2.5M NSF/NIH
          cta:
            text: Explore Projects
            url: /research/computational-biology
            
        - name: Machine Learning
          description: Advancing deep learning methods for scientific discovery, with focus on interpretable AI and physics-informed neural networks
          icon: hero/cpu-chip
          gradient: from-purple-400 to-pink-600
          status: active
          topics:
            - Deep Learning
            - Computer Vision
            - NLP
            - Graph Neural Networks
            - Explainable AI
          team_size: 8
          publications: 32+
          funding: $1.8M NSF
          cta:
            text: View Research
            url: /research/machine-learning
            
        - name: Materials Science
          description: Designing novel materials through computational modeling and machine learning-guided discovery
          icon: emoji/atom_symbol
          gradient: from-blue-400 to-indigo-600
          status: emerging
          topics:
            - Nanomaterials
            - Quantum Materials
            - Energy Storage
            - Catalysis
          team_size: 6
          publications: 28+
          funding: $1.2M DOE
          cta:
            text: Learn More
            url: /research/materials-science
      cta:
        text: Active Research Projects
        url: /#research
        icon: hero/arrow-right
    design:
      layout: cards
      css_class: "bg-gradient-to-b from-gray-50 to-white dark:from-gray-900 dark:to-gray-800"
      spacing:
        padding: ["5rem", 0, "5rem", 0]

  - block: cta-image-paragraph
    content:
      items:
        - title: 'State-of-the-Art Research Environment'
          text: |
            Our laboratory features cutting-edge equipment and modern research facilities designed to support breakthrough discoveries. From advanced computational clusters to precision instrumentation, we provide our researchers with the tools they need to push the boundaries of science.
          image: pexels-polina-tankilevitch-3735769.jpg
          feature_icon: hero/check-circle
          features:
            - 'High-Performance Computing: 500+ core GPU cluster for AI/ML research'
            - 'Advanced Instrumentation: Precision equipment for materials characterization'
            - 'Safety & Compliance: Full safety protocols and regulatory compliance'
          button:
            text: 'Virtual Lab Tour'
            url: '/facilities'

        - title: 'Collaborative Innovation Culture' 
          text: |
            Breakthrough research happens through collaboration. Our open lab environment fosters cross-disciplinary partnerships, knowledge sharing, and mentorship between senior researchers and emerging scientists. Every team member contributes to our collective mission of advancing scientific understanding.
          image: pexels-canvastudio-3153198.jpg
          feature_icon: hero/users
          features:
            - 'Cross-Disciplinary Teams: Biologists, engineers, and computer scientists working together'
            - 'Knowledge Sharing: Weekly seminars and collaborative research meetings'
            - 'Mentorship Program: Structured guidance for PhD students and postdocs'
          button:
            text: 'Join Our Community'
            url: '/opportunities'
    design:
      css_class: "bg-white dark:bg-gray-800"
      spacing:
        padding: ["4rem", 0, "4rem", 0]

  - block: team-showcase
    id: team
    content:
      title: Meet Our Team
      subtitle: 'World-class researchers pushing the boundaries of science'
      text: 'Our diverse team of researchers brings together expertise from multiple disciplines to tackle the most challenging problems in computational biology and machine learning.'
      user_groups:
        - Principal Investigators
        - Postdoctoral Researchers
        - PhD Students
      sort_by: 'Params.last_name'
      sort_ascending: true
      cta:
        text: View All Team Members
        url: /authors
        icon: user-group
    design:
      show_role: true
      show_organizations: false
      show_interests: true
      show_social: true
      # Section background color
      css_class: "bg-gray-50 dark:bg-gray-900"
      # Reduce spacing
      spacing:
        padding: ["3rem", 0, "3rem", 0]

  - block: collection
    id: projects
    content:
      title: Active Research Projects
      subtitle: ''
      text: ''
      filters:
        folders:
          - projects
      count: 0  # Number of items to show (0 = all)
      # Default filter UI (for future release)
      #default_button_index: 0
      # Filter toolbar (optional)
      # Add or remove as many filters as you like
    #   buttons:
    #     - name: All
    #       tag: '*'
    #     - name: Machine Learning
    #       tag: ML
    #     - name: Biology
    #       tag: Biology
    #     - name: Materials
    #       tag: Materials
    design:
      view: article-grid
      columns: 2

  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
      count: 5
    design:
      view: citation

  - block: collection
    id: featured
    content:
      title: Featured Research
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2

  - block: collection
    id: events
    content:
      title: Events
      subtitle: Join Us for Research Presentations & Seminars
      text: Stay connected with our research community through talks, workshops, and collaborative events
      filters:
        folders:
          - events
        exclude_past: false  # Show both past and future events
      count: 3
      sort_by: Date
      sort_ascending: false
    design:
      view: card
      # columns: 3
      show_date: true
      show_read_time: false
      show_read_more: true
      css_class: "bg-gradient-to-b from-white to-gray-50 dark:from-gray-800 dark:to-gray-900"
      spacing:
        padding: ["4rem", 0, "4rem", 0]

  - block: collection
    id: news
    content:
      title: Lab News & Updates
      subtitle: ''
      text: ''
      # Page type to display. E.g. post, talk, publication...
      page_type: blog
      # Choose how many pages you would like to display (0 = all pages)
      count: 3
      # Filter on criteria
      filters:
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ''
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: card
      columns: 1

  - block: logos
    content:
      title: Collaborators & Partners
      subtitle: Leading the way together
      text: We work with top universities, research institutes, and industry leaders to advance scientific discovery
      logos:
        - name: MIT
          image: partners/placeholder-logo.svg
          url: https://mit.edu
          external: true
          description: Massachusetts Institute of Technology
        - name: Stanford University
          image: partners/placeholder-logo.svg
          url: https://stanford.edu
          external: true
          description: Stanford Research Collaboration
        - name: Google Research
          image: partners/placeholder-logo.svg
          url: https://research.google
          external: true
          description: AI & Machine Learning Partnership
        - name: National Science Foundation
          image: partners/placeholder-logo.svg
          url: https://nsf.gov
          external: true
          description: Research Funding Partner
        - name: Microsoft Research
          image: partners/placeholder-logo.svg
          url: https://www.microsoft.com/research
          external: true
          description: Computing Research Collaboration
        - name: NIH
          image: partners/placeholder-logo.svg
          url: https://nih.gov
          external: true
          description: National Institutes of Health
      cta:
        text: Become a Partner
        url: /#contact
        icon: hero/user-plus
    design:
      display_mode: grid
      show_pattern: false
      css_class: "bg-gradient-to-b from-white to-gray-50 dark:from-gray-800 dark:to-gray-900"
      spacing:
        padding: ["4rem", 0, "4rem", 0]

  - block: contact-info
    id: contact
    content:
      title: Contact Us
      subtitle: Get in touch with our research team
      visit_title: Visit Our Lab
      connect_title: Connect With Us
      address:
        lines:
          - Smith Laboratory
          - Department of Computer Science
          - University of Excellence
          - 123 Science Drive
          - Excellence City, EC 12345
          - United States
      office_hours:
        - "Monday - Friday: 9:00 AM - 5:00 PM"
        - "Lab Meetings: Fridays 2:00 PM"
      email: lab@example.edu
      phone: "+1 (555) 123-4567"
      social:
        - icon: brands/x
          url: https://twitter.com/SmithLabResearch
        - icon: brands/linkedin
          url: https://linkedin.com/company/smith-lab
        - icon: brands/github
          url: https://github.com/smith-lab
      prospective:
        title: Prospective Members
        text: Interested in joining our lab? We're always looking for motivated researchers at all levels.
        button:
          text: View Open Positions
          url: /opportunities
      map_url: https://maps.google.com/?q=University+of+Excellence
      show_form: false
    design:
      css_class: "bg-gradient-to-b from-gray-50 to-white dark:from-gray-900 dark:to-gray-800"
      spacing:
        padding: ["5rem", 0, "5rem", 0]

  - block: cta-card
    content:
      title: Join Our Research Team
      text: We are always looking for talented and motivated researchers to join our lab. We have openings for PhD students, postdoctoral researchers, and research scientists.
      button:
        text: View Open Positions
        url: /opportunities
    design:
      card:
        # Card background color (CSS class)
        css_class: 'bg-primary-300 dark:bg-primary-700'
        css_style: ''
---