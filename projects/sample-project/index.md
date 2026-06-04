---
title: Project Template (Example)
description: Reusable template page for adding detailed project writeups.
# Header image shown behind the global top banner for this page.
header: images/project_images/sample-project/placeholder.png
---

<!--
  Copy this file to projects/<new-slug>/index.md and replace all sample content.
  Keep image paths repo-root-relative, e.g. images/project_images/<new-slug>/image-name.jpg.
  Then add a matching entry in _data/projects.yaml with:
    - title/subtitle/description/tags (project card text shown on /projects)
    - image (project card thumbnail)
    - link: projects/<new-slug> (opens this detail page)
-->

# {{ page.title }}

{% include section.html background=page.header %}
<!--
  section.html creates a new section break. The "background" argument controls this
  section's background image (separate from the global page header above).
-->

{% include figure.html
  image="images/project_images/sample-project/placeholder.png"
  caption="Replace with your project overview image and caption."
  width="100%"
%}
<!--
  figure.html controls the main image block:
    - image: the displayed image path
    - caption: visible text under image
    - width / height: image sizing
-->

## Abstract

<!-- Replace with a concise summary of the problem, approach, and contribution. -->
Provide a 1-3 paragraph abstract describing the motivation, methodology, and impact of the project.

## Team

<!-- Add people and roles as needed. -->
- **Principal Investigator:** Dr. Example Name
- **Student Researchers:** Student One, Student Two
- **Collaborators:** Collaborator Lab / Organization

## Links

<!-- Keep only the links that apply to your project. -->
- [Project page](https://example.com)
- [Paper / DOI](https://doi.org/example)
- [Code repository](https://github.com/UAlbertaVISUAL/visual-lab-website)
- [Dataset](https://example.com/dataset)

## Methods

<!-- Describe model architecture, data processing, experiments, or workflow. -->
Summarize the core technical methods, tools, and experimental setup used by the project.

## Results

<!-- Summarize key findings, performance, figures, and outcomes. -->
Highlight the main outcomes, quantitative results, and practical significance.

## Citation

<!-- Replace with your project's preferred citation text or BibTeX. -->
```bibtex
@misc{sample_project_template,
  title  = {Project Template (Example)},
  author = {UAlberta VISUAL Lab},
  year   = {2026},
  note   = {Replace with your real citation details}
}
```

<!-- Optional project tags shown as badges. -->
{% include tags.html tags="sample, template, project-page" %}
