---
title: Home
carousels:
  - images: 
    - image: /images/carousel/1.webp
    - image: /images/carousel/2.webp
    - image: /images/carousel/3.webp
    - image: /images/carousel/4.webp
---

# Welcome to the Englert Lab Website!

Studying lung mechanotransduction to identify novel therapies for ICU patients.

{% include section.html %}

{% include carousel.html height="50" unit="%" duration="10" number="1" %}

## Highlights

{% capture text %}

The Englert Lab is part of the [Division of Pulmonary, Critical Care, and Sleep Medicine](https://medicine.osu.edu/departments/internal-medicine/pulmonary) and the [Davis Heart and Lung Research Institute](https://medicine.osu.edu/departments/davis-heart-lung-research-institute) at [The Ohio State University Wexner Medical Center](https://wexnermedical.osu.edu/).  The goal of our research group is to identify the mechanisms that lead to lung injury in the intensive care unit to develop molecularly-targeted therapies for these patients.  To facilitate this precision-based medicine strategy, we employ a multidisciplinary approach that spans the fields of molecular biology, biomedical engineering, and nanomedicine. To achieve our goals we use high fidelity models of the lung microenvironment, preclinical models of critical illness, and biospecimens from clinical studies.  This translational approach.  We are known for our collaborative approach and commitment to scientific rigor and integrity.  Another key mission of the Englert Lab is to train future generations of lung scientists. 

{%
  include button.html
  link="research"
  text="See our publications"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="research"
  title="Our Research"
  text=text
%}

{% capture text %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

{%
  include button.html
  link="projects"
  text="Browse our projects"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="projects"
  title="Our Projects"
  flip=true
  style="bare"
  text=text
%}

{% capture text %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

{%
  include button.html
  link="team"
  text="Meet our team"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="team"
  title="Our Team"
  text=text
%}
