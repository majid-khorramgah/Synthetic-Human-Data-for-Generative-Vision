# Synthetic Dataset Generation

## Overview

This directory presents the design and implementation of the controllable synthetic human dataset developed for this research project.

Unlike publicly available face datasets collected from real-world photographs or videos, this dataset was generated entirely within a controlled virtual environment. The primary objective is to enable systematic experiments in which individual visual factors can be manipulated while maintaining reproducibility.

The dataset serves as the experimental foundation for investigating representation learning and generalization in generative vision models.

---

# Objectives

The synthetic dataset was designed with the following objectives:

* create a fully reproducible data generation pipeline;
* maintain consistent synthetic identities;
* generate large numbers of facial images under controlled conditions;
* support experiments in generative modeling and representation learning;
* provide a scalable framework for future identity expansion.

Rather than maximizing dataset size, the emphasis is placed on controllability and experimental consistency.

---

# Current Dataset

The current version of the dataset contains:

* **100,000 synthetic facial images**
* **50,000 images of one synthetic female identity**
* **50,000 images of one synthetic male identity**

Both identities were generated using the same rendering pipeline while producing a broad range of facial expressions.

This simplified configuration intentionally limits identity diversity, providing a controlled baseline for future experiments.

---

# Dataset Characteristics

The dataset is designed to provide:

* consistent synthetic identities;
* diverse facial expressions;
* reproducible image generation;
* controlled rendering conditions;
* high-quality facial images suitable for generative model training.

Future versions of the dataset will progressively introduce additional synthetic identities while preserving the same controlled generation methodology.

---

# Repository Structure

This directory is organized as follows:

* **project_overview.md** – Overall design philosophy and dataset objectives.
* **daz_studio_pipeline.md** – Human generation workflow using DAZ Studio.
* **rendering_configuration.md** – Rendering parameters and configuration.
* **automation_pipeline.md** – Automation workflow for large-scale image generation.
* **dataset_statistics.md** – Dataset composition and summary statistics.
* **metadata.md** – Metadata structure and file organization.
* **samples/** – Representative examples from the generated dataset.

---

# Research Perspective

This synthetic dataset is not intended to replace existing public face datasets.

Instead, it provides a controllable experimental environment in which semantic factors can be manipulated systematically, enabling research questions that are difficult to investigate using naturally collected images.

The dataset therefore represents an experimental platform for studying representation learning rather than an end product in itself.

---

# Next Steps

The synthetic dataset described in this directory is subsequently used for training generative vision models, evaluating learned representations, and investigating how controllable synthetic identity diversity influences generalization.
