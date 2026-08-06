# Metadata

This document describes the metadata organization, file naming convention, and directory structure used throughout the synthetic face dataset.

---

# Overview

The dataset was designed with a deterministic folder hierarchy and file naming convention, allowing every rendered image to be uniquely identified without requiring an external database.

Each image implicitly contains information about:

- Character gender
- Expression preset
- Camera viewpoint
- Rendering configuration
- Image resolution
- Dataset split (if applicable)

---

# Directory Structure

```
Dataset/

├── Female_Angry 01/
│   ├── Female_Angry 01_001.png
│   ├── Female_Angry 01_002.png
│   ├── ...
│   └── Female_Angry 01_215.png
│
├── Female_Happy 01/
│   └── ...
│
├── Male_Angry 01/
│   └── ...
│
└── ...
```

Each directory corresponds to a single facial-expression preset.

---

# Folder Naming Convention

Folder names follow the format

```
<Gender>_<Expression Preset>
```

Examples

```
Female_Angry 01

Female_Happy 03

Female_Scream

Male_Talking 02

Male_Chewing
```

Each folder contains images rendered from multiple predefined camera viewpoints while keeping every other rendering parameter identical.

---

# Image Naming Convention

Each rendered image follows

```
<FolderName>_<ViewIndex>.png
```

Example

```
Female_Angry 01_001.png

Female_Angry 01_107.png

Female_Angry 01_215.png
```

where

| Component | Description |
|-----------|-------------|
| Folder Name | Expression preset |
| View Index | Camera viewpoint identifier (001–215) |
| Extension | PNG |

---

# Camera View Index

The final numeric identifier represents the predefined camera position.

Example

| Index | Description |
|-------:|-------------|
|001|Beginning of camera trajectory|
|050|Left-side viewpoint|
|107|Frontal view|
|170|Right-side viewpoint|
|215|Final viewpoint|

A total of **215 fixed camera viewpoints** were used for every expression preset.

---

# Expression Metadata

Each expression preset represents one unique facial configuration generated inside DAZ Studio.

The complete dataset contains

- 210 Female presets
- 227 Male presets

for a total of

**437 facial-expression presets.**

Expression categories include

- Neutral
- Happy
- Sad
- Angry
- Fear
- Surprise
- Disgust
- Talking
- Screaming
- Mouth Open
- Tongue
- Pain
- Sleepy
- Playful
- Romantic
- Serious
- Wink
- Hand Interaction
- Eyeglasses
- Facial Hair (Male)

and many additional variations.

---

# Character Metadata

Only two base identities were used.

| Gender | Character |
|---------|-----------|
|Female|Genesis 8 Female|
|Male|Genesis 8 Male|

Identity remained constant throughout the rendering process while only facial expressions, camera viewpoints, and lighting conditions changed.

---

# Rendering Metadata

Each rendered image shares the same basic properties.

| Property | Value |
|----------|-------|
|Format|PNG|
|Resolution|1024 × 1024 pixels|
|Render Engine|DAZ Studio Iray|
|Background|Transparent / Black (depending on render stage)|
|Output|RGB|

---

# Metadata Availability

The current release stores metadata implicitly through the directory hierarchy and filename convention.

No external annotation files (JSON, XML, or CSV) are required to identify the semantic information associated with each rendered image.

Future releases may additionally provide machine-readable metadata files for large-scale dataset indexing and automated preprocessing.

---

# Summary

Every rendered image can be uniquely identified by combining

- Folder name
- Character gender
- Expression preset
- Camera viewpoint index
- Rendering configuration

This deterministic structure simplifies dataset management, reproducibility, automated preprocessing, and future expansion without introducing additional metadata dependencies.
