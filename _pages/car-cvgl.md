---
title: "CAR-CVGL: Conditional Height-Aware BEV Representation for Cross-View Geo-Localization"
permalink: /car-cvgl/
author_profile: false
classes: wide
---

<p align="center">
  <strong>British Machine Vision Conference (BMVC), 2026</strong>
</p>

<p align="center">
  Nikolaos Poulopoulos,
  Alexandros Gkillas,
  Christos Anagnostopoulos,
  Aris Lalos,
  Huu Le,
  Duong V. Nguyen
</p>

<p align="center">
  <a href="/files/car-cvgl-bmvc2026.pdf" class="btn btn--primary">Paper</a>
  <a href="https://arxiv.org/abs/XXXX.XXXXX" class="btn">arXiv</a>
  <a href="https://github.com/USERNAME/CAR-CVGL" class="btn">Code</a>
</p>

---

![CAR-CVGL overview](/images/car-cvgl/teaser.png)

## Abstract

This paper addresses the problem of cross-view geo-localization, where the
goal is to estimate the vehicle pose by matching ground observations to aerial
imagery. Existing methods typically learn feature alignment implicitly and
often discard height information during bird's-eye-view (BEV) construction,
limiting robustness and introducing ambiguity.

To overcome these limitations, we propose a transformer-based framework that
reformulates cross-view geo-localization as an explicit conditional alignment
problem in BEV space. Our method introduces a conditional height-aware feature
selection mechanism, where satellite BEV features condition the selection of
the most relevant height-wise ground features prior to BEV pooling, preserving
informative 3D structure and reducing ambiguity.

In addition, we propose a spatial cross-attention module that directly couples
ground and satellite BEV features through direct cross-view feature exchange,
enabling more robust alignment under challenging conditions.

Experiments on FordAV and KITTI benchmarks indicate consistent improvements
over state-of-the-art methods. In particular, our approach achieves superior
performance under cross-area evaluation, demonstrating improved generalization
across unseen geographic regions and appearance variations, while reducing
localization error by **33.8%** compared to the previous state of the art on
FordAV.

Furthermore, we introduce a lightweight variant, **CAR-Lite**, which achieves
**8.55 FPS** while maintaining competitive localization accuracy.

## Method

![CAR-CVGL architecture](/images/car-cvgl/method.png)

CAR-CVGL formulates cross-view geo-localization as explicit conditional
alignment between ground-view and satellite representations in BEV space.

The framework contains two key components:

1. **Conditional Height-Aware Feature Selection** — satellite BEV features
   guide the selection of relevant height-wise ground features before BEV
   pooling, preserving informative 3D structure.

2. **Spatial Cross-Attention** — ground and satellite BEV representations
   exchange information directly, improving cross-view feature alignment.

## Results

CAR-CVGL achieves state-of-the-art performance on the **FordAV** and **KITTI**
cross-view geo-localization benchmarks.

In particular, CAR-CVGL reduces localization error by **33.8%** over the
previous state of the art on FordAV under cross-area evaluation.

CAR-Lite provides a computationally efficient alternative, running at
**8.55 FPS** while retaining competitive localization accuracy.

## Citation

If you find our work useful, please consider citing:

```bibtex
@inproceedings{poulopoulos2026carcvgl,
  title     = {CAR-CVGL: Conditional Height-Aware BEV Representation for Cross-View Geo-Localization},
  author    = {Poulopoulos, Nikolaos and
               Gkillas, Alexandros and
               Anagnostopoulos, Christos and
               Lalos, Aris and
               Le, Huu and
               Nguyen, Duong V.},
  booktitle = {British Machine Vision Conference},
  year      = {2026}
}
