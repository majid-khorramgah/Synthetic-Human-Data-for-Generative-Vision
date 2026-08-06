# Rendering Configuration

## Overview

All synthetic images were rendered using **DAZ Studio** with a standardized rendering pipeline to maximize consistency while maintaining sufficient visual diversity for deep learning applications.

The rendering configuration was designed to generate high-resolution facial images under controlled conditions while systematically varying pose, facial expression, and illumination.

---

# Rendering Engine

| Parameter | Value |
|-----------|------|
| Software | DAZ Studio |
| Renderer | NVIDIA Iray |
| Output Format | PNG (Lossless) |
| Resolution | 1024 × 1024 pixels |
| Color Space | RGB |
| Bit Depth | 8-bit |

---

# Camera Configuration

A fixed focal length was used throughout the dataset to avoid geometric distortion.

Camera viewpoints were sampled over the complete head pose range.

Included viewpoints:

- Frontal
- Left
- Right
- Upward (High Angle)
- Downward (Low Angle)

In addition, intermediate yaw, pitch and roll rotations were rendered to produce smooth pose transitions.

---

# Lighting Configuration

Multiple illumination presets were created to simulate common real-world lighting environments.

The rendering pipeline includes:

- Front White Light
- Left Side Light
- Right Side Light
- Top Light
- Bottom Light
- Warm Lighting
- Cool Lighting
- Colored Lighting

Lighting intensity and direction were intentionally varied while preserving facial visibility.

The goal was to improve robustness against illumination changes during model training.

---

# Facial Expressions

Expressions were generated using multiple commercial DAZ Studio expression packs together with native Genesis 8 controls.

Dataset statistics:

- Female expression presets: **210**
- Male expression presets: **227**
- Total expression categories: **437**

The generated expressions include:

- Neutral
- Happy
- Angry
- Sad
- Fear
- Surprise
- Disgust
- Contempt
- Pain
- Talking
- Screaming
- Mouth Open
- Tongue Movement
- Eye Closure
- Eye Wink
- Crying
- Coughing
- Chewing
- Choking
- Sleepy
- Crazy
- Playful
- Romantic
- Nervous
- Serious
- and many additional subtle facial variations.

---

# Pose Sampling

Each expression preset was rendered from **215 predefined camera positions**.

The sequence gradually changes the head orientation, creating smooth transitions between viewpoints while preserving facial identity.

This approach provides continuous pose coverage rather than a small number of discrete camera angles.

---

# Character Consistency

Only one female identity and one male identity were used throughout dataset generation.

This design intentionally isolates:

- pose variation
- facial expression variation
- lighting variation

without introducing identity-related variability.

Such isolation simplifies controlled evaluation of facial reconstruction and deepfake training.

---

# Image Quality

The following properties were kept constant for every render:

- High-resolution facial textures
- Physically based skin materials
- Stable camera calibration
- Consistent image framing
- Lossless PNG export
- Fixed image dimensions

No post-processing filters or artificial image degradation were applied.

---

# Rendering Pipeline

Each rendered sample follows the same sequence:

1. Load Genesis 8 character.
2. Apply facial expression preset.
3. Apply pose rotation.
4. Configure lighting preset.
5. Render using NVIDIA Iray.
6. Export PNG image.
7. Store image with deterministic filename.

---

# Output Statistics

| Property | Value |
|----------|------:|
| Resolution | 1024 × 1024 |
| Female Images | 50,000 |
| Male Images | 50,000 |
| Total Images | 100,000 |
| Female Expression Categories | 210 |
| Male Expression Categories | 227 |
| Total Expression Categories | 437 |
| Camera Positions per Expression | 215 |
| Image Format | PNG |

---

# Design Objective

The rendering configuration was designed to maximize diversity while preserving complete control over the generation process.

Unlike real-world image collections, every rendering parameter—including identity, pose, facial expression, lighting, and camera configuration—can be reproduced exactly, making the dataset suitable for controlled experiments, benchmarking, and synthetic data generation research.
