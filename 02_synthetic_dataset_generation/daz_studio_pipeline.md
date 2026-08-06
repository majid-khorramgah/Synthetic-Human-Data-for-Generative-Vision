# DAZ Studio Pipeline

## Overview

The synthetic dataset presented in this project was generated using **DAZ Studio** as the primary 3D character creation and rendering platform.

The objective of the pipeline was to create a reproducible dataset with controllable facial appearance while avoiding copyright restrictions associated with third-party characters.

The complete workflow was designed to generate large numbers of facial images under controlled conditions for subsequent training and evaluation of generative vision models.

---

# Base Characters

The dataset was built using the official DAZ Studio base characters:

* **Genesis 8 Male**
* **Genesis 8 Female**

These standard characters are freely distributed by DAZ 3D and provide a suitable foundation for academic and research-oriented synthetic data generation.

Using official base assets ensures a transparent and reproducible pipeline while avoiding dependence on copyrighted commercial character models.

---

# Facial Expression Generation

Facial expressions were generated using the **V100 Expressions – The Gold Collection** expression package.

This package provides a broad range of facial muscle configurations that can be applied consistently to synthetic characters.

The generated images include a diverse collection of facial expressions, ranging from neutral poses to more expressive facial movements, enabling richer supervision for generative model training.

---

# Camera Configuration

To improve viewpoint diversity, images were rendered from multiple virtual camera positions.

The rendering pipeline includes:

* frontal views;
* left and right profile views;
* low-angle views;
* high-angle views;
* intermediate viewpoints;
* combinations of yaw, pitch, and roll rotations.

This controlled camera setup provides significantly greater viewpoint coverage than can typically be obtained from naturally collected photographs.

---

# Lighting Configuration

Multiple virtual lighting conditions were incorporated into the rendering process.

Lighting variations include changes in:

* light direction;
* light intensity;
* illumination angle;
* shadow distribution.

The objective is to expose the learning algorithm to a wider range of appearance conditions while maintaining complete control over the rendering environment.

---

# Image Resolution

All rendered facial images were generated at a resolution of:

**1024 × 1024 pixels**

The chosen resolution provides sufficient facial detail for training high-quality generative models while remaining computationally practical for large-scale experiments.

---

# Motivation for the Pipeline

Preliminary observations of existing deepfake models revealed several challenging situations in which visual quality often degrades.

These situations include:

* extreme head rotations;
* low-angle and high-angle views;
* uncommon facial expressions;
* visible teeth;
* tongue visibility;
* partial facial occlusions;
* challenging illumination conditions.

These observations motivated the creation of a synthetic dataset capable of systematically generating such conditions under controlled settings.

---

# Current Dataset

The first version of the dataset contains:

* **100,000 rendered facial images**
* **50,000 images of one synthetic female identity**
* **50,000 images of one synthetic male identity**

Both identities were rendered using the same generation pipeline while varying facial expressions, camera viewpoints, and lighting conditions.

This controlled configuration serves as the initial stage of a broader research roadmap investigating synthetic identity diversity.

---

# Future Extensions

The current pipeline has been designed for scalability.

Future versions of the dataset will extend the rendering process by incorporating:

* additional synthetic identities;
* more extensive facial expression libraries;
* facial occlusions (e.g., glasses, masks, hands, and hair);
* broader illumination environments;
* additional rendering configurations;
* larger-scale synthetic datasets for representation learning and generalization studies.

---

# Summary

DAZ Studio provides a flexible and reproducible environment for generating synthetic facial data with precise control over semantic attributes.

The resulting pipeline forms the foundation of the synthetic dataset used throughout this project and supports systematic experimentation that would be difficult to reproduce using unconstrained real-world image collections.
