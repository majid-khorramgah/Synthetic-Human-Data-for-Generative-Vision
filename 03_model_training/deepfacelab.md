# DeepFaceLab Training

## Overview

DeepFaceLab is the primary framework used for training the face-swapping model in this project.

Rather than training a model from scratch, an existing pretrained SAEHD model was fine-tuned using a large synthetic human face dataset generated in DAZ Studio. The objective was to improve robustness against pose variation, facial expressions, illumination changes, and partial facial occlusions.

---

# Why DeepFaceLab?

DeepFaceLab remains one of the most widely used open-source deepfake frameworks due to its modular training pipeline and high-quality reconstruction capabilities.

Its advantages include:

- Mature training pipeline
- Stable SAEHD architecture
- Flexible preprocessing
- High-quality face alignment
- Identity-preserving reconstruction
- Support for pretrained models
- Extensive community validation

These characteristics make it suitable for evaluating the contribution of a synthetic facial dataset.

---

# Training Workflow

The complete workflow consists of six major stages.

```

Raw Video
↓

Face Extraction
↓

Face Alignment
↓

Dataset Preparation
↓

Model Training
↓

Model Export

```

---

# 1. Face Extraction

Source and target videos are processed using the DeepFaceLab extraction tools.

The extraction stage detects:

- Face location
- Facial landmarks
- Face rotation
- Cropping region

Only aligned facial images are used during training.

---

# 2. Face Alignment

Extracted faces are geometrically normalized.

Alignment removes variations caused by:

- Camera rotation
- Scale
- Translation
- Head position

This produces consistent training samples.

---

# 3. Dataset Preparation

Two datasets are prepared.

## Source Dataset

Synthetic human faces generated in DAZ Studio.

Characteristics include:

- Male
- Female
- Hundreds of expressions
- Multiple head poses
- Controlled illumination
- Occlusions
- High-quality rendering

Approximately

- 437 expression presets
- 215 viewpoints per preset
- More than 90,000 images

---

## Target Dataset

The target identity is extracted from real videos using the standard DeepFaceLab extraction pipeline.

Target videos may include

- Interviews
- Movies
- Public footage
- Recorded videos

---

# 4. Model Initialization

Training begins from a pretrained SAEHD model.

Using a pretrained model significantly reduces convergence time while preserving the learned facial representation.

Instead of learning basic facial geometry from scratch, the network focuses on adapting to the additional diversity introduced by the synthetic dataset.

---

# 5. Fine-Tuning

The pretrained network is fine-tuned using the synthetic dataset.

Training parameters:

| Parameter | Value |
|-----------|-------|
| Model | SAEHD |
| Initialization | Pretrained |
| Training Resolution | 512 × 512 |
| Render Resolution | 1024 × 1024 |
| GPU | NVIDIA RTX 4090 (24 GB VRAM) |
| Iterations | ~3,000,000 |

Training at resolutions above 512×512 was limited by GPU memory requirements, making 512×512 the most practical configuration for long-term optimization.

---

# Synthetic Data Contribution

The synthetic dataset introduces visual conditions that are difficult to capture consistently in real-world datasets.

Examples include:

- Extreme yaw angles
- Extreme pitch angles
- Roll rotations
- Mouth opening
- Teeth visibility
- Tongue visibility
- Facial hair
- Eyeglasses
- Hand occlusions
- Lighting variations
- Camera distance variation

These samples improve the diversity of the optimization process and reduce overfitting to limited facial conditions.

---

# Training Objective

The optimization process focuses on improving

- Identity preservation
- Facial geometry
- Expression reconstruction
- Mouth accuracy
- Eye consistency
- Texture quality
- Robustness to illumination
- Robustness to pose variation
- Robustness to partial occlusions

---

# Model Evaluation

Model quality is evaluated continuously using preview images generated during training.

The following characteristics are monitored:

- Identity similarity
- Expression consistency
- Mouth reconstruction
- Eye reconstruction
- Lighting adaptation
- Pose stability
- Artifact reduction

Training continues until the preview images stabilize and reconstruction quality no longer improves significantly.

---

# Limitations

Although synthetic data greatly improves model robustness, the final quality still depends on the availability of sufficient target identity data.

The pretrained model provides a stronger initialization, but creating a high-quality deepfake for a new individual still requires an adequate number of target images extracted from real videos.

---

# Summary

DeepFaceLab serves as the training framework for this project, while the primary contribution of the work lies in the construction of a large-scale synthetic facial dataset.

By combining a pretrained SAEHD model with more than ninety thousand synthetic facial images covering diverse poses, expressions, lighting conditions, and occlusions, the project aims to improve the generalization capability of deepfake models under challenging real-world scenarios.
