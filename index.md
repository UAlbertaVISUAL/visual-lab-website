---
---

# UAlbertaVISUAL's Website

Welcome to the **VISUAL (Video, Image, Signal Understanding and Learning) Laboratory** at the University of Alberta. Led by **Dr. Nilanjan Ray**, our lab is a part of the Department of Computing Science.

### Our Mission
We are dedicated to advancing the frontiers of computer vision, image analysis, and visual recognition. Our research leverages deep learning and continuous optimization to solve complex problems in:

* **Medical Imaging:** Automated segmentation and tracking in MRI, CT, and other modalities.
* **Visual Recognition:** Object detection, tracking, and semantic segmentation.
* **ADEPT:** Developing Architectures for Differentiable End-to-end Programming and Training.

We bridge the gap between theoretical machine learning and practical, high-impact applications in healthcare and autonomous systems.

{% include section.html %}

## Highlights

{% capture text %}

Take a look at some of our most recent publications

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
  image="images/2025_group_photo.jpg"
  link="team"
  title="Our Members"
  text=text
%}
