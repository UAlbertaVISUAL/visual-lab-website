---
title: A Comparison of Deep Learning Models for Automatic Left-Ventricular Segmentation in 3D Echocardiography
description: A comparison of five deep-learning models for automatic left-ventricular segmentation from 3D echocardiography.
authors:
  - name: "Ishani DasGupta"
    affiliation: "Department of Computing Science, University of Alberta, Edmonton, Canada"
  - name: "Nilanjan Ray"
    affiliation: "Department of Computing Science, University of Alberta, Edmonton, Canada"
  - name: "Kumaradevan Punithakumar"
    affiliation: "Department of Radiology & Diagnostic Imaging, University of Alberta, Edmonton, Canada"
---

# {{ page.title }}

{% include section.html %}

{% include figure.html
  image="images/project_images/2025_Ishani_LVSeg_3dEcho_Comparison/project-image-ishani-2025-ISBI_lv_seg.png"
  caption="Project overview image"
  width="100%"
%}

## YEAR:
2025

## VENUE:
ISBI 2025

## KEYWORDS:
Echocardiography, Neural Networks, Transformers, Left Ventricle, Image Segmentation

## Abstract

Echocardiography is a non-invasive, non-ionizing, and cost-effective medical imaging modality that uses ultrasound waves to evaluate cardiac function. Left ventricle (LV) analysis is crucial for diagnosing cardiac diseases. Segmentation of the LV from echocardiography images is a challenging, time-consuming process requiring manual contouring from experts and is prone to inter-observer variability.

Five different deep-learning models are evaluated for automatic LV segmentation from 3D echocardiography. The models were compared using overlap and distance metrics: Dice score, Jaccard index, and Hausdorff distance. Volumetric analysis was used to examine the accuracy of the predictions from the deep learning models against the expert-annotated ground truth volumes.

The comparison between these models provides a foundation for further development of accurate and efficient automated LV segmentation methods, particularly approaches that can leverage the temporal consistency of echocardiography scans.

## Team

- **Ishani DasGupta** (Department of Computing Science, University of Alberta, Edmonton, Canada)
- **Nilanjan Ray** (Department of Computing Science, University of Alberta, Edmonton, Canada)
- **Kumaradevan Punithakumar** (Department of Radiology & Diagnostic Imaging, University of Alberta, Edmonton, Canada)

## Links

- [Publication](https://ieeexplore.ieee.org/document/10981267)
- [Paper PDF](https://drive.google.com/file/d/1Mgaj3O7I86YnRryE8PZ9bFDAF9Jcgepk/view)
- [Poster PDF](https://drive.google.com/file/d/1JZxG87O2M3pbbMjp-t_0_bzpwNNc8sjJ/view)

{% include tags.html tags="echocardiography, neural networks, transformers, left ventricle, image segmentation" %}
