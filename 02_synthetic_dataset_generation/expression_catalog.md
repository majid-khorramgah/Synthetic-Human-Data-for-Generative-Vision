# Expression Catalog

## Overview

This document provides a catalog of the facial expression presets used during the generation of the synthetic face dataset.

Rather than relying on a single expression package, the rendering pipeline combines multiple DAZ Studio expression libraries to maximize facial diversity while preserving identity consistency.

The catalog includes both female and male expression presets used throughout the rendering process.

---

# Expression Statistics

| Property | Value |
|----------|------:|
| Female Expression Presets | 210 |
| Male Expression Presets | 227 |
| **Total Expression Presets** | **437** |

The expression presets were applied to two fixed synthetic identities throughout the dataset generation pipeline.

---

# Expression Categories

The available expression presets can be grouped into several semantic categories.

## 1. Head Pose and Morph Adjustment

These presets introduce controlled geometric variations of the head and jaw.

Examples include:

- +10
- +20
- +30
- +40
- +50
- -10
- -20
- -30
- -40
- -50
- -60
- Neutral (0)

These presets slightly modify head orientation and facial geometry while maintaining identity consistency.

---

## 2. Emotional Expressions

The dataset covers a broad range of emotional facial states.

Included categories include:

- Angry
- Happy
- Joy
- Sad
- Fear
- Surprise
- Disgust
- Contempt
- Desire
- Romantic
- Cute
- Playful
- Empathy
- Distrust
- Judgemental
- Seriousness
- Wicked

Most emotional categories contain multiple intensity levels (01–05), increasing expression diversity.

---

## 3. Extreme Facial Expressions

Several presets intentionally represent uncommon or exaggerated facial configurations.

Examples include:

- Scream
- Choking
- Coughing
- Chewing
- Crying
- Breath Taking
- Crazed
- Insanity
- Lunatic
- Hostile
- Savage
- Terror
- Ulgh

These expressions are particularly valuable for studying challenging facial configurations in generative models.

---

## 4. Mouth and Jaw Configurations

The rendering pipeline includes numerous mouth-related presets.

Examples include:

- Mouth Open Horizontal
- Mouth Open Horizontal and Vertical
- Talking
- Chewing
- Scream
- Open Wide

These configurations generate significant variation in lip shape, jaw opening, teeth visibility, and oral articulation.

---

## 5. Eye and Eyebrow Expressions

The catalog also includes presets affecting the eye region.

Examples include:

- Wink
- Sleepy
- Eyeglasses
- Fear
- Distrust

These expressions increase diversity around the eye muscles and eyelids.

---

## 6. Facial Muscle Actions

Several presets emphasize localized muscle movements.

Examples include:

- Pain
- Nervous
- Determined
- Humiliated
- Forehead Wrinkles

These expressions introduce subtle facial muscle deformation beyond basic emotional states.

---

## 7. Occlusion and Interaction Poses

A limited number of presets include partial facial interaction or occlusion.

Examples include:

- Right Hand on Face
- Water Bottle Pose
- Eyeglasses

These configurations simulate partial facial occlusions that are frequently encountered in real-world images.

---

## 8. Facial Hair Variations (Male)

The male character additionally includes several facial hair configurations.

Examples include:

- Full Beard
- Goatee
- Fu Manchu
- Napoleon III
- Officer
- Pioneer
- Stubbled
- Mutton Chops

These presets increase appearance diversity without changing the underlying facial identity.

---

# Coverage Summary

The complete expression catalog provides variation in:

- facial emotions;
- mouth articulation;
- jaw opening;
- eyebrow movement;
- eye movement;
- facial muscle deformation;
- facial accessories;
- partial facial occlusion;
- facial hair configuration;
- subtle and extreme facial expressions.

This diversity enables systematic generation of facial images covering many situations that are difficult to collect consistently from real-world photographs.

---

# Complete Expression List

The following sections contain the complete list of expression presets used during dataset generation.

## Female Expression Presets

*(Insert the complete list of the 210 female presets here.)*

---

## Male Expression Presets

*(Insert the complete list of the 227 male presets here.)*

---

# Summary

The rendering pipeline incorporates a total of **437 expression presets** distributed across multiple semantic categories.

Instead of relying on random expression generation, the dataset intentionally combines emotional expressions, facial muscle actions, mouth configurations, occlusion poses, and appearance modifiers to provide broad yet reproducible facial diversity for synthetic data generation.
