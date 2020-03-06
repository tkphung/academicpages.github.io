---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* **PhD** Biomedical Engineering, University of Virginia, 2020
* **BS** Biomedical Engineering & Mathematical Sciences, University of Memphis, 2014

Research Interests
======
* Cardiovascular and Pulmonary Biomechanics
* Computational Modeling
* Data Visualization
* Science Communication

Technical Skills
======
* MATLAB
* Finite-element methods (FEBio)
* Image processing

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>

Teaching & Mentoring
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

  <!-- [PDF Version](http://dpananos.github.io/files/DEMETRI_CV.pdf) -->
