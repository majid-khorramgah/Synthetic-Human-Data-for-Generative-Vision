# Dataset Statistics

## Overview

The synthetic facial dataset was created to provide a large-scale, highly controlled collection of facial images for deepfake training, face reenactment, facial animation, and computer vision research.

Unlike conventional datasets collected from photographs or videos, every image in this dataset was generated using a reproducible 3D rendering pipeline, ensuring complete control over facial expression, head pose, camera position, and illumination.

---

# Dataset Summary

| Property | Value |
|----------|------:|
| Total Images | **100,000** |
| Female Images | **50,000** |
| Male Images | **50,000** |
| Characters | **2 (1 Female, 1 Male)** |
| Female Expression Categories | **210** |
| Male Expression Categories | **227** |
| Total Expression Categories | **437** |
| Camera Positions per Expression | **215** |
| Image Resolution | **1024 × 1024** |
| Image Format | PNG |
| Rendering Engine | NVIDIA Iray |
| Software | DAZ Studio |

---

# Dataset Composition

The dataset consists of two balanced subsets.

| Subset | Images |
|---------|-------:|
| Female | 50,000 |
| Male | 50,000 |

Both subsets were generated using identical rendering settings to eliminate rendering bias while preserving gender-specific facial geometry.

---

# Expression Statistics

A total of **437 unique facial expression categories** were generated.

| Category | Count |
|----------|------:|
| Female Expressions | 210 |
| Male Expressions | 227 |
| Total | 437 |

The expression library covers:

- Neutral
- Happiness
- Anger
- Sadness
- Fear
- Surprise
- Disgust
- Contempt
- Pain
- Joy
- Romantic
- Playful
- Serious
- Nervous
- Talking
- Screaming
- Mouth Open
- Tongue Movement
- Crying
- Chewing
- Choking
- Sleepy
- Crazy
- Subtle facial movements
- Eye movements
- Forehead wrinkle variations
- Many additional expression presets

---

# Camera Statistics

Every expression preset was rendered from **215 predefined camera viewpoints**.

The viewpoints span continuous rotations across the three rotational axes:

| Axis | Description |
|------|-------------|
| Yaw | Left ↔ Right |
| Pitch | Up ↔ Down |
| Roll | Head Tilt |

Representative viewpoints include:

- Frontal
- Left profile
- Right profile
- High angle
- Low angle
- Intermediate rotations

This dense sampling produces smooth pose transitions rather than isolated viewpoints.

---

# Lighting Statistics

Eight lighting configurations were used throughout dataset generation.

| Lighting Preset |
|----------------|
| Front White |
| Left Side |
| Right Side |
| Top |
| Bottom |
| Warm |
| Cool |
| Colored |

Lighting intensity and direction were varied while preserving facial visibility.

---

# Character Statistics

The dataset intentionally contains only two identities.

| Character | Count |
|-----------|------:|
| Female Identity | 1 |
| Male Identity | 1 |

This design isolates the effects of facial pose, illumination, and expression without introducing identity variability.

---

# Image Properties

Every rendered image shares the following properties:

| Property | Value |
|----------|------|
| Resolution | 1024 × 1024 |
| Color Space | RGB |
| Compression | Lossless |
| Background | Uniform |
| Renderer | NVIDIA Iray |
| File Format | PNG |

---

# Dataset Diversity

Although only two identities were used, the dataset achieves substantial visual diversity through controlled variation of rendering parameters.

| Variable | Diversity Source |
|----------|------------------|
| Identity | Male / Female |
| Facial Expression | 437 Categories |
| Head Pose | 215 Camera Positions |
| Lighting | 8 Presets |
| Facial Orientation | Continuous Rotation |
| Mouth Configuration | Closed / Open / Wide Open / Tongue Variants |
| Eye State | Open / Closed / Wink / Asymmetric |
| Facial Muscle Activation | Mild to Extreme |
| Accessories (Selected Presets) | Glasses, Hand-on-Face, Water Bottle Pose |

---

# Dataset Scale

The rendering pipeline generated approximately:

- **100,000 rendered images**
- **437 facial expression categories**
- **215 camera viewpoints**
- **8 lighting presets**
- **1024 × 1024 resolution**

making this dataset considerably more structured than most publicly available synthetic facial datasets.

---

# Intended Applications

The dataset is suitable for:

- Deepfake model training
- Face swapping
- Face reenactment
- Facial animation
- Expression transfer
- Talking-head generation
- Face reconstruction
- Facial landmark research
- Pose robustness evaluation
- Synthetic data augmentation
- Computer vision benchmarking

---

# Key Characteristics

- **100,000 high-resolution synthetic facial images**
- **Balanced female and male subsets**
- **437 expression categories**
- **215 camera viewpoints per expression**
- **Eight controlled lighting conditions**
- **Lossless PNG images**
- **1024 × 1024 resolution**
- **Fully reproducible rendering pipeline**
- **Consistent facial identity**
- **Controlled experimental design**
