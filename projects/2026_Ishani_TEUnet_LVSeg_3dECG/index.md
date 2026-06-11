---
title: Time-Embedding U-Net for Temporally Consistent Left Ventricular Segmentation in 3D Echocardiography
description: A temporal U-Net approach for improving left ventricular segmentation consistency in 3D echocardiography.
authors:
  - name: "Ishani DasGupta"
    affiliation: "Department of Computing Science, University of Alberta, Edmonton, Canada"
  - name: "Nilanjan Ray"
    affiliation: "Department of Computing Science, University of Alberta, Edmonton, Canada"
  - name: "Kumaradevan Punithakumar"
    affiliation: "Department of Radiology & Diagnostic Imaging, University of Alberta, Edmonton, Canada"
---

<!--
  Copy this file to projects/<new-slug>/index.md and replace all sample content.
  Keep image paths repo-root-relative, e.g. images/project_images/<new-slug>/image-name.jpg.
-->

# {{ page.title }}

{% include section.html %}

{% include figure.html
  image="images/project_images/2026_Ishani_TEUnet_LVSeg_3dECG/project-image-ishani-2026-TEunet_lv_seg.png"
  caption="Key Result Image"
  width="100%"
%}

## YEAR: 
2026

## KEYWORDS: 
Echocardiography, Neural Networks, Transformers, Time-embedding, Left-Ventricle, Image-Segmentation


## Abstract

<!-- Replace with a concise summary of the problem, approach, and contribution. -->
Three-dimensional (3D) echocardiography is an inherently noisy modality, but allows for capture of temporally complex cardiac motions. Existing segmentation methods often treat cardiac frames independently, which can lead to inconsistent predictions over time. We present Time-Embedding U-Net (TE U-Net), a temporal extension of the U-Net architecture that incorporates explicit time embeddings and temporal context to improve frame-to-frame consistency in left ventricular segmentation from 3D echocardiography. Our approach leverages both spatial and temporal information to produce smoother and more anatomically coherent segmentations across cardiac cycles. Experimental results demonstrate improved temporal consistency while maintaining strong segmentation performance, highlighting the promise of temporal modeling for robust cardiac image analysis.

## Team

- **Ishani DasGupta** (Department of Computing Science, University of Alberta, Edmonton, Canada)
- **Nilanjan Ray** (Department of Computing Science, University of Alberta, Edmonton, Canada)
- **Kumaradevan Punithakumar** (Department of Radiology & Diagnostic Imaging, University of Alberta, Edmonton, Canada)

## Links

<!-- Keep only the links that apply to your project. -->
- [DOI](https://ieeexplore.ieee.org/document/11515394)
- [Paper PDF](https://drive.google.com/file/d/1uqiE7wD92Y2sKqLjgU5GixzSbpvLaa17/view?usp=drive_link)
- [Oral Presentation](https://drive.google.com/file/d/1oNKMqLL9PDjyywGz1Pi_6jYRgGKgLUsw/view)




<!-- Optional project tags shown as badges. -->
{% include tags.html tags="Echocardiography, Neural Networks, Transformers, Time-embedding, Left-Ventricle, Image-Segmentation" %}
