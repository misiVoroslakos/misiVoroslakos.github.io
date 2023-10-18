---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: 
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: misiV
  - block: features
    content:
      title: Skills
      items:
        - name: Electrophysiology
          description: Freely moving mice and rats <br><br> Neuropixels 2.0 <br> Silicon probes <br> Flexible probes
          icon: ephys_icon
          icon_pack: custom
        - name: Optogenetics
          description: Freely moving and head-fixed mice <br><br> Optrodes <br> μLED probe <br> Waveguide probe
          icon: optogenetics_icon
          icon_pack: custom
        - name: Brain stimulation
          description: Transcranial Electrical Stimulation <br><br> Mice <br> Rats <br> Humans
          icon: NIBS_icon
          icon_pack: custom
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Circuit Resonance
          tag: Circuit Resonance
          weight: 10
        - name: TES-fMRI
          tag: TES-fMRI
          weight: 20
        - name: Brain-body 
          tag: Brain-body
          weight: 30
        - name: ThermoMaze 
          tag: ThermoMaze
          weight: 40
        - name: Tool Development 
          tag: Tool Development
          weight: 50
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
#  - block: markdown
#    content:
#      title: Gallery
#      subtitle: ''
#      text: |-
#        {{< gallery album="demo" >}}
#    design:
#      columns: '1'
  #- block: collection
  #  id: publication
  #  content:
  #    title: Featured Publications
  #    filters:
  #      folders:
  #        - publication
    #    featured_only: true
    #design:
    #  columns: '2'
    #  view: card
  - block: collection
    id: publication
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  - block: collection
    id: talks
    content:
      title: Talks
      subtitle: This is a home for invited talks and workshops, each linked with accompanying materials.
      filters:
        folders:
          - event
    design:
      columns: '2'
      view: compact
  #- block: tag_cloud
  #  content:
  #    title: Popular Topics
  #  design:
  #    columns: '2'
  - block: contact
    id: contact
    content:
      title: Contact
      #subtitle:
      #text: |-
      #  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam mi diam, venenatis ut magna et, vehicula efficitur enim.
      # Contact (add or remove contact options as necessary)
      email: voroslakos@gmail.com
      phone: +1 734 263 3777
      #appointment_url: 'https://calendly.com'
      address:
        street: 435 E. 30th Street (Room 1323)
        city: New York
        region: NY
        postcode: '10016'
        country: United States
        country_code: US
      #directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
      #office_hours:
      #  - 'Monday 10:00 to 13:00'
      #  - 'Wednesday 09:00 to 10:00'
      #contact_links:
      #  - icon: twitter
      #    icon_pack: fab
      #    name: DM Me
      #    link: 'https://twitter.com/Twitter'
      #  - icon: skype
      #    icon_pack: fab
      #    name: Skype Me
      #    link: 'skype:echo123?call'
      #  - icon: video
      #    icon_pack: fas
      #    name: Zoom Me
      #    link: 'https://zoom.com'
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      #form:
      #  provider: netlify
      #  formspree:
      #    id:
      #  netlify:
          # Enable CAPTCHA challenge to reduce spam?
      #    captcha: false
    design:
      columns: '2'
---
