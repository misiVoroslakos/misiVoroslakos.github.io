---
# An instance of the About widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: Ephys setup

# Activate this widget? true/false
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 20
type: "post"
title: 'Building an electrophysiology setup'
# [design.spacing]
# Customize the section spacing. Order is top, right, bottom, left.
css_style: "padding-top: 20px; padding-bottom: 20px;"

# design:
#   background:
#       gradient_start: '#4bb4e3'
#       gradient_end: '#2b94c3'
#       gradient_angle: 180


# Choose the user profile to display
# This should be the username (folder name) of a profile in your `content/authors/` folder.
# See https://wowchemy.com/docs/get-started/#introduce-yourself
author: misiV

# Images may be added to a page by either placing them in your assets/media/
---
### Outline
1. Introduction
2. Equipment and considerations
3. Overview of technologies

### Introduction
Extracellular single-unit measures – which are not always available in animals and are rarely possible in humans – provides one of the most direct read-out of neural activity. The extracellular electrode can record ‘single-unit activity’ or ‘spikes’ of several neurons because each recording channel has a sensing range of 65 to 140 μm ([Gray, 1995](https://www.sciencedirect.com/science/article/pii/0165027095000852) and [Henze, 2000](https://journals.physiology.org/doi/epdf/10.1152/jn.2000.84.1.390)). Electrophysiological methods can measure the activity of individual neurons at high temporal resolution (millisecond scale).  <br /> 
I recommend watching [Prof. Kensall D. Wise talk](https://www.youtube.com/watch?v=G5mfF5yV_lA) at the University of Michigan. In this talk, Prof. Wise describes the Rocky Road to Neurotechnology from 1966 to 2016. <br /> 
I am only going to discuss how to use penetrating silicon-based microelectrodes to record extracellular spikes (single units) and local field potentials (LFP). A great review about electroencephalogram (EEG), electrocorticogram (ECoG), LFP and spikes can be found in [Buzsaki, 2012](https://www.nature.com/articles/nrn3241) and about state-of-the-art recording and stimulation tools for brain research in [Seymour, 2017](https://www.nature.com/articles/micronano201666) <br /> 
### Equipment and considerations
To record single units, we will need a microelectrode, a headstage (preamplifier), cable connecting the headstage to a data acquisition system and a recording PC (**Fig. 1.**). An input/output expander can record peripheral analog and digital devices (like camera TTL, valves opening for delivering water reward, etc.). If you want to read more about the difference between analog and digital signals, you can find a great summary at [Sparkfun](https://learn.sparkfun.com/tutorials/analog-vs-digital). Unfortunately, the naming convention is different from company to company (common 'other names' are in brackets). 
![screen reader text](ephys_setup_page_01.png "Figure 1. Components of an ephys setup")
<br />
## Ground and Reference
The signal is measured against a reference/ground. The ground can be a stainless-steel screw with a wire soldered to it, or a wire (platinum, stainless-steel). We typically place the ground over cerebellum and secure it in place using dental cement (**Fig. 2.**). You can watch [how to prepare a ground screw](https://www.youtube.com/watch?v=_XFqGOXRdm4) and find bill of materials in our [Bio-protocol paper](https://en.bio-protocol.org/en/bpdetail?id=4137&type=0). How to secure a ground screw? I think a Hungarian proverb can describe it best: "*So many houses, so many customs.*" In short, every lab does this differently, so I just show a couple of ones in **Fig. 2** that I used in the past. 
![screen reader text](ephys_setup_page_02.png "Figure 2. Ground/reference options")
And you might wonder, what about reference? Excellent question and I think [Andrew Klein's post](https://plexon.com/blog-post/point-of-reference/) is worth reading to better understand why you have ground and reference pins and wires on your Omnetics connector/probe PCB. 
<br />
## Probe anatomy
Once you have your ref/gnd, you can implant a probe to measure the neuronal activity. But which one? There are so many companies with so many different probes (Cambridge NeuroTech, Diagnostic Biochips, NeuroNexus, Neuropixels, Blackrok Neurotech, etc.). In short, it depends on where you want to record from and what your final analysis will be about. The questions that I would address before ordering a probe:
<br />
1. **Type of recordings:** acute / head-fixed acute / freely-moving chronic. Acute probes doesn't have a flexible cable, chronic ones have. In a chronic animal, you need to decouple the force that you apply to the Omnetics connector from the shanks while plugging in the headstage. 
<br />
2. **What is the depth of your brain region?** Most probes are 5 mm in length but 10 mm is also available (don't forget to count the skull and dental cement). This is the Length of the shanks.
<br />
3. **Do you need an angle?** In general, it is 'easy' to insert below 10 degrees. I think beyond 10 degrees, every 5 degrees will make insertion significantly more difficult. The more the shanks are, the more difficult insertion becomes (with a crazy angle some of your shanks will be in the brain while other will be in air, and the ones that are in the brain will always guide the other ones making the insertion challanging).
<br />
4. **What is the 3D structure of your region of interest?** As a rule of thumb it is good to have extra shanks to maximize your chances to have at least one shank inside the target region. How many shanks you need?
<br />
5. **Are you interested in more single units or recording the spatial profile of LFP across layers?** If you need more cells, try to squeeze in as many recording sites as possible into your brain region. Don't forget that drift can occur in both acute and chronic recordings. Drift means the physical movement of the brain relative to the probe. Your probe will be deeper than expected in most of the cases after the brain 'bounces' back. If you don't have some extra in dorso-ventral dimensions, then you can be below of your target and 'loose' all cells.  
![screen reader text](ephys_setup_page_04.png "Figure 3. Probe anatomy")
<br />
## Microdrives
**How to hold and move your probe once it is in the brain?** 
<br />
Acute probes can be attached to any commercial manipulators. Chronic probes are typically attached to a mechanical shuttle (called microdrive) that can move the probe in the 'z-axis'. There are many different microdrives available. An important thing to consider is the travel distance of the microdrive, how much you can move in the brain, and weight of the microdrive. 3D-printed plastic drives will be cheaper and lighter than metal ones. We have designed a [recoverable, metal microdrive](https://elifesciences.org/articles/65859) to improve probe reusability. 
<br />
### Overview of technologies
