# Training Configuration

## Overview

The objective of this training stage was to improve the robustness of an existing DeepFaceLab model using a large-scale synthetic human face dataset generated in DAZ Studio.

Instead of training a model from scratch, a pretrained DeepFaceLab model was selected as the initialization point. The pretrained model already contained general facial representations, allowing the training process to focus on learning the additional pose, expression, lighting, and occlusion variations provided by the synthetic dataset.

---

# Base Model

Training was initialized from a pretrained DeepFaceLab SAEHD model.

Advantages of using a pretrained model include:

- Faster convergence
- Stable optimization
- Better facial identity preservation
- Reduced training time
- Improved reconstruction quality

Rather than replacing the original knowledge of the network, the synthetic dataset extends and refines the learned facial representations.

---

# Training Dataset

The training dataset consists of synthetic human faces rendered in DAZ Studio.

Dataset characteristics include:

- Male and female subjects
- 437 expression presets
- 215 camera viewpoints per preset
- Controlled head rotations
- Multiple lighting environments
- Facial occlusions
- High-resolution renders

The dataset contains more than 90,000 rendered facial images covering a wide range of facial appearances.

---

# Image Resolution

Although the synthetic images were rendered at

```
1024 × 1024
```

the training process was performed using

```
512 × 512
```

face crops.

This resolution provided a practical balance between image quality and GPU memory consumption. Training at higher resolutions was not feasible due to the VRAM limitations of the available hardware.

---

# Training Hardware

| Component | Specification |
|-----------|---------------|
| GPU | NVIDIA GeForce RTX 4090 |
| VRAM | 24 GB |
| Image Resolution | 512 × 512 |
| Framework | DeepFaceLab |

Even with a 24 GB RTX 4090, training at resolutions higher than 512×512 significantly reduced the feasible batch size and overall training efficiency. Therefore, 512×512 was selected as the optimal training resolution.

---

# Training Duration

The pretrained model was fine-tuned for approximately

**3,000,000 iterations**

using the synthetic dataset.

A long training schedule was intentionally adopted to allow the network to gradually learn the additional facial variations introduced by the synthetic renders while preserving the identity reconstruction capability of the pretrained model.

---

# Training Strategy

The optimization process focuses on improving robustness under conditions that are often underrepresented in conventional datasets.

These include:

- Large head rotations
- Extreme facial expressions
- Open-mouth poses
- Teeth visibility
- Tongue visibility
- Facial occlusions
- Eyeglasses
- Facial hair
- Lighting variations
- Camera distance changes

---

# Expected Improvements

The fine-tuned model is expected to provide improved performance in:

- Facial identity preservation
- Expression reconstruction
- Mouth synthesis
- Eye reconstruction
- Pose generalization
- Illumination robustness
- Partial face occlusion handling

Compared with the original pretrained model, the additional synthetic training data significantly increases the diversity of facial appearances observed during optimization, improving generalization to challenging real-world scenarios.
