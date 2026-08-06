# Training Pipeline

This document describes the complete model training workflow used in this project. The pipeline starts from the synthetic dataset generation stage and ends with deployment inside DeepFaceLive for real-time face swapping.

---

# Pipeline Overview

The complete workflow consists of six sequential stages.

```
Synthetic Dataset
        │
        ▼
Dataset Preparation
        │
        ▼
Face Extraction
        │
        ▼
Model Training (DeepFaceLab)
        │
        ▼
Model Export
        │
        ▼
Real-Time Inference (DeepFaceLive)
```

Each stage is described below.

---

# Stage 1 — Synthetic Dataset Preparation

The training process begins with the synthetic human dataset generated in DAZ Studio.

Dataset characteristics include:

- 100,000 rendered images
- 50,000 female images
- 50,000 male images
- 1024 × 1024 resolution
- Fixed identity for each gender
- 437 expression presets
- Multiple camera angles
- Multiple lighting conditions
- Occlusion simulations
- Mouth-open variations
- Head rotation variations

The objective of this dataset is to expose the model to situations that are uncommon in publicly available face datasets.

---

# Stage 2 — Dataset Organization

Before training, all rendered images are organized into separate source and destination datasets.

Typical directory structure:

```
workspace/

    data_src/

    data_dst/

    aligned/

    model/

    previews/
```

Images are grouped by identity while preserving naming consistency across expression presets.

This organization simplifies later stages including face extraction, alignment, and model training.

---

# Stage 3 — Face Extraction

The rendered images are processed using the DeepFaceLab extraction pipeline.

The extraction stage performs:

- Face detection
- Landmark estimation
- Face alignment
- Square crop generation
- Metadata generation

The output of this stage is an aligned faceset that serves as the input for neural network training.

---

# Stage 4 — Dataset Verification

Before training, the aligned facesets are manually inspected.

Verification includes:

- Missing faces
- Incorrect alignment
- Blurred renders
- Rendering artifacts
- Broken expressions
- Incorrect crops
- Duplicate samples

Removing problematic samples improves convergence during training.

---

# Stage 5 — Model Training

Training is performed using DeepFaceLab.

The neural network learns the mapping between the source identity and destination identity while preserving:

- facial geometry
- eye movement
- mouth motion
- facial expressions
- pose consistency
- illumination consistency

The model is trained for a large number of iterations until convergence.

Training periodically generates preview images for visual inspection.

Typical training cycle:

```
Dataset

↓

Forward Pass

↓

Loss Computation

↓

Backpropagation

↓

Weight Update

↓

Preview Generation

↓

Repeat
```

---

# Stage 6 — Checkpoint Saving

During training, model checkpoints are saved automatically.

Each checkpoint contains:

- network weights
- optimizer state
- iteration count
- preview samples

This allows interrupted training sessions to resume without restarting.

---

# Stage 7 — Model Evaluation

Model quality is evaluated visually using preview images.

The evaluation focuses on:

- facial identity preservation
- expression transfer
- mouth reconstruction
- eye reconstruction
- profile consistency
- color consistency
- artifact reduction

Training continues until visual quality stabilizes.

---

# Stage 8 — Model Export

Once training converges, the trained model is exported for inference.

Export includes:

- neural network weights
- inference configuration
- optimized runtime model

The exported model is compatible with DeepFaceLive.

---

# Stage 9 — Real-Time Deployment

The exported model is loaded into DeepFaceLive.

The real-time inference pipeline consists of:

```
Camera

↓

Face Detection

↓

Face Landmark Detection

↓

Face Alignment

↓

Neural Network Inference

↓

Face Reconstruction

↓

Color Transfer

↓

Frame Blending

↓

Video Output
```

This enables live face swapping using the trained model.

---

# Training Objectives

The synthetic dataset was specifically designed to improve model robustness under challenging facial conditions.

Target scenarios include:

- extreme head rotation
- low-angle views
- high-angle views
- open mouth
- visible teeth
- visible tongue
- blinking
- asymmetric expressions
- strong lighting
- colored lighting
- facial occlusions
- profile views
- partial face visibility

These situations are frequently underrepresented in conventional face datasets.

---

# Expected Outcome

The final trained model is expected to provide:

- improved facial consistency
- better expression reconstruction
- more stable identity preservation
- higher robustness to pose variations
- improved mouth and eye rendering
- smoother temporal consistency
- reduced visual artifacts
- better real-time performance

---

# Related Documents

- training_configuration.md
- deepfacelab.md
- deepfacelive.md
- training_logs.md

---

# Figure

```
figures/training_pipeline.png
```

The accompanying figure illustrates the complete training workflow from synthetic dataset generation to real-time deployment.
