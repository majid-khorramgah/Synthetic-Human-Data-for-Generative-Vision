# DAZ Studio Pipeline

## Overview

This document describes the complete workflow used to generate the synthetic facial image dataset presented in this repository.

The objective of the pipeline is to create a reproducible and controllable facial dataset for experiments in generative vision, representation learning, and deepfake model training.

Unlike datasets collected from photographs or videos, every image in this dataset is generated inside a virtual 3D environment, allowing individual visual attributes to be systematically controlled.

---

# Pipeline Overview

The synthetic data generation workflow consists of the following stages:

1. Character selection
2. Facial expression generation
3. Camera configuration
4. Lighting configuration
5. Rendering
6. Dataset organization

Each stage is independently configurable while remaining fully reproducible.

---

# Character Selection

The dataset was generated using the official DAZ Studio base characters:

- Genesis 8 Female
- Genesis 8 Male

These characters were intentionally selected because they are official DAZ Studio assets and do not depend on third-party commercial character models.

Using the standard Genesis characters ensures that the complete rendering pipeline can be reproduced without relying on copyrighted celebrity assets or proprietary face models.

The current version of the dataset contains:

- one synthetic female identity
- one synthetic male identity

Identity remains fixed throughout the rendering process while other visual factors are varied.

---

# Facial Expression Pipeline

Facial diversity is introduced through multiple DAZ Studio expression libraries.

The rendering pipeline incorporates expression presets from several independent collections, including:

- Bee Sting
- Causam3D
- Expression Smoother
- Feelings
- Godin i3D
- i3D
- IT Roy
- Neikdian
- Open Wide
- Tongue Control HD
- Valery3D
- V100 Expressions – The Gold Collection

Instead of relying on a single expression pack, multiple libraries are combined to maximize facial variation.

### Expression Statistics

| Character | Expression Presets |
|-----------|-------------------:|
| Genesis 8 Female | 210 |
| Genesis 8 Male | 227 |
| **Total** | **437** |

These expression presets cover a broad spectrum of facial configurations, including:

- neutral expressions;
- smiling;
- anger;
- sadness;
- surprise;
- fear;
- eyebrow movements;
- eye movements;
- mouth opening;
- wide-open mouth;
- visible upper teeth;
- visible lower teeth;
- tongue movements;
- asymmetric expressions;
- exaggerated facial expressions.

Using multiple expression libraries substantially increases facial diversity while preserving identity consistency.

---

# Camera Configuration

To improve viewpoint diversity, virtual cameras were positioned around the synthetic character.

The rendered dataset includes:

- frontal view;
- left profile;
- right profile;
- three-quarter view;
- high-angle view;
- low-angle view;
- combinations of yaw, pitch, and roll rotations.

The objective is to improve viewpoint coverage under controlled conditions.

---

# Lighting Configuration

Multiple lighting configurations were used throughout the rendering process.

Lighting parameters include controlled variation of:

- illumination direction;
- light intensity;
- shadow placement;
- scene brightness.

Unlike naturally collected datasets, lighting conditions are fully reproducible.

---

# Rendering Configuration

All facial images were rendered at:

**1024 × 1024 pixels**

A fixed rendering resolution simplifies preprocessing and provides consistent image quality throughout the dataset.

---

# Dataset Composition

The current dataset contains:

| Property | Value |
|----------|------:|
| Total Images | 100,000 |
| Female Images | 50,000 |
| Male Images | 50,000 |
| Female Identity | 1 |
| Male Identity | 1 |
| Expression Presets | 437 |
| Resolution | 1024 × 1024 |

The rendering pipeline intentionally begins with two fixed identities to establish a controlled experimental baseline before scaling to larger synthetic identity sets.

---

# Design Motivation

The pipeline was designed after observing several common failure cases in existing deepfake systems.

Particular attention was given to generating facial images that include:

- high-angle viewpoints;
- low-angle viewpoints;
- large head rotations;
- diverse facial expressions;
- open-mouth configurations;
- visible teeth;
- tongue visibility;
- controlled illumination conditions.

These visual conditions are difficult to obtain systematically from naturally collected datasets but can be reproduced consistently within a synthetic rendering environment.

---

# Pipeline Characteristics

The proposed generation pipeline provides several important advantages:

- fully reproducible rendering;
- controllable facial appearance;
- consistent synthetic identities;
- large facial expression diversity;
- systematic camera placement;
- controlled illumination;
- scalable dataset generation.

These characteristics make the pipeline suitable for controlled experiments in generative vision and representation learning.

---

# Summary

The DAZ Studio pipeline establishes a reproducible framework for generating controllable synthetic human faces.

The current implementation contains 100,000 rendered images generated from two synthetic identities using 437 facial expression presets, multiple camera viewpoints, controlled lighting configurations, and a fixed rendering resolution of 1024 × 1024 pixels.

Future versions of the pipeline will extend the number of synthetic identities while preserving the same generation methodology.
