---
title: Time-Embedding U-Net for Temporally Consistent Left Ventricular Segmentation in 3D Echocardiography
description: Reusable template page for adding detailed project writeups.
header: images/project_images/sample-project/placeholder.png
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

{% include section.html background=page.header %}

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
Three-dimensional (3D) echocardiography is an inherently noisy modality, but allows for capture of temporally complex cardiac motions. Existing segmentation methods often treat cardiac frames independently, resulting in inconsistent delineations across the cardiac cycle, reduced segmentation accuracy, and, in turn, impacting the estimation of key clinical metrics. To address this, our work introduces temporal positional embeddings based on the cardiac cycle to improve 3D echocardiography segmentation. By encoding cardiac phase information into sinusoidal functions, we inject temporal embeddings into the bottleneck and decoder of a U-Net. Our approach (TU-Net) outperforms state-of-the-art models, including nnU-Net and Transformer baselines, UNETR and SwinUNETR. TU-Net achieved a Dice score of 84.7% along with improved temporal consistency, evaluated over two test cases with 18 and 16 frames across the cardiac cycle. Testing this on a lightweight U-Net, which is both efficient and suitable for clinical settings, demonstrates the significance of temporal information in enhancing segmentation quality without complex models. These results highlight the potential for further improvements, not only in 3D echocardiography but also in other dynamic medical imaging modalities.
## Team

- **Ishani DasGupta** (Department of Computing Science, University of Alberta, Edmonton, Canada)
- **Nilanjan Ray** (Department of Computing Science, University of Alberta, Edmonton, Canada)
- **Kumaradevan Punithakumar** (Department of Radiology & Diagnostic Imaging, University of Alberta, Edmonton, Canada)

## Links

<!-- Keep only the links that apply to your project. -->
- [Oral Presentation](https://drive.google.com/file/d/1oNKMqLL9PDjyywGz1Pi_6jYRgGKgLUsw/view)




<!-- Optional project tags shown as badges. -->
{% include tags.html tags="Echocardiography, Neural Networks, Transformers, Time-embedding, Left-Ventricle, Image-Segmentation" %}