---
layout: splash
permalink: /
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/vortex1.jpg
  caption: "Photo credit: [**ShopiFlyers**](https://twitter.com/ShopiFlyers/status/1013415498317484032)"
excerpt: "I'm a Ph.D. candidate in Aerospace Engineering at the University of Illinois at Urbana-Champaign (UIUC). Feel free to explore my personal site to know more about my research and interests!"
intro: 
  - excerpt: 'I am a passionate researcher with broad interests in engineering and computational science. Before beginning my Ph.D., I had graduated with B.Tech. in Mechanical Engineering from Indian Institute of Technology (IIT) Gandhinagar and M.S. in Aerospace Engineering from UIUC. My current interests lie in the intersection of computational fluid dynamics, aerodynamics, high-performance computing and data-driven reduced order modeling to develop novel models for enabling faster simulation of fluid flows eventually leading to faster aerodynamic design, optimization and control.'
feature_row:
  - image_path: assets/images/vortex.jpg
    image_caption: "Image courtesy of [Unsplash](https://unsplash.com/)"
    alt: "placeholder image 1"
    title: "Placeholder 1"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
  - image_path: /assets/images/vortex.jpg
    alt: "placeholder image 2"
    title: "Placeholder 2"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/images/vortex.jpg
    title: "Placeholder 3"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
feature_row2:
  - image_path: /assets/images/vortex.jpg
    alt: "placeholder image 2"
    title: "Placeholder Image Left Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Left aligned with `type="left"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row3:
  - image_path: /assets/images/vortex.jpg
    alt: "placeholder image 2"
    title: "Placeholder Image Right Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Right aligned with `type="right"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row4:
  - image_path: /assets/images/vortex.jpg
    alt: "placeholder image 2"
    title: "Placeholder Image Center Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Centered with `type="center"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}

{% include feature_row id="feature_row3" type="right" %}

{% include feature_row id="feature_row4" type="center" %}
