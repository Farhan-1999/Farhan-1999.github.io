---
layout: archive
title: "Metadata-Guided Land Use Land Cover Segmentation with Remote Sensing Data for Developing Regions"
permalink: /research_publications/lulc
author_profile: true
---

![]({{ '/images/lulc_rough_model.png'}}){: .align-center style="width:10%;height:auto;}

Semantic segmentation for Land Use and Land Cover (LULC) mapping plays a crucial role in urban planning, sustainable development, and environmental monitoring. However, such LULC mapping is challenging in developing regions where built-up structures are mostly complex and unstructured. Traditional image-only semantic segmentation approaches often fail to capture these characteristics, especially in developing cities like Dhaka, Bangladesh. We propose a context-aware segmentation framework that utilizes text-based metadata of the region along with the satellite imagery. This multimodal framework is capable of distinguishing visually similar features due to the additional context provided as text. Experiments on Dhaka Division show that incorporating administrative metadata leads to substantial improvements over image-only baselines, proving the necessity for context-driven semantic segmentation for LULC mapping in complex urban and rural environments.

We,
- Built a multimodal dataset with images accompanied with their corresponding geographical metadata
- Aligning the image patches with metadata information so that metadata information correctly guides the image.
- Using textual and visual prompt tuning methods to gain better semantics as training progresses.

![]({{ '/images/patch.png'}}){: .align-center style="width:10%;height:auto;}