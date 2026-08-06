# Limitations of Existing Human Datasets

## Introduction

Public human image datasets have significantly advanced computer vision research by providing large-scale collections of facial images captured under real-world conditions. These datasets remain essential for benchmarking recognition, generation, reconstruction, and analysis methods.

However, datasets collected from natural environments inevitably exhibit practical limitations when the objective is to perform controlled experiments on representation learning and generative models.

The following limitations motivate the development of a controllable synthetic human dataset.

---

# Limited Viewpoint Coverage

Most public datasets contain a large number of frontal or near-frontal faces.

Extreme viewpoints are generally less common and often unevenly distributed across identities.

Examples include:

* full profile views;
* low-angle views;
* high-angle views;
* extreme head rotations;
* upward-looking faces;
* downward-looking faces.

This imbalance limits systematic evaluation across the full viewing sphere.

---

# Limited Facial Expression Diversity

Although many datasets include smiling, neutral, or several common expressions, comprehensive coverage of facial muscle configurations is often limited.

Expressions such as:

* subtle eyebrow movements;
* asymmetric facial expressions;
* extreme mouth opening;
* exaggerated emotional expressions;
* transitional expressions;

may be underrepresented or inconsistently distributed across identities.

---

# Limited Mouth, Teeth, and Tongue Variations

Many face datasets primarily contain closed-mouth or partially open-mouth images.

Images clearly showing:

* different mouth openings;
* visible teeth;
* tongue positions;
* detailed oral cavity appearance;

are typically much less common and difficult to obtain under controlled conditions.

These attributes are particularly important for facial animation and generative modeling.

---

# Illumination Imbalance

Lighting conditions in public datasets are determined by the original capture environment.

Consequently, illumination may vary unpredictably across:

* lighting direction;
* light intensity;
* shadow patterns;
* color temperature;
* indoor and outdoor scenes.

Researchers generally cannot control these factors independently.

---

# Pose and Head Orientation

Head pose is naturally coupled with other visual factors.

Datasets may contain:

* limited pitch variation;
* limited roll variation;
* limited yaw variation;

while combinations of these rotations are often sparsely represented.

---

# Occlusion

Real-world images frequently include occlusions caused by:

* hair;
* eyeglasses;
* hands;
* masks;
* hats;
* scarves;
* surrounding objects.

While valuable for robustness evaluation, these occlusions reduce the availability of clean and controlled facial observations.

---

# Image Quality Variability

Public datasets typically contain images acquired under diverse conditions.

As a result, image quality may vary considerably due to:

* motion blur;
* camera blur;
* compression artifacts;
* sensor noise;
* inaccurate focus;
* low resolution;
* overexposure;
* underexposure.

These variations introduce uncontrolled factors during training and evaluation.

---

# Annotation Limitations

Many datasets provide identity labels or a limited set of facial attributes.

However, detailed annotations describing all semantic factors are often unavailable, incomplete, or inconsistent.

Examples include:

* precise head pose;
* lighting parameters;
* camera geometry;
* facial muscle configuration;
* mouth state;
* tongue visibility;
* teeth visibility.

---

# Lack of Independent Control

Perhaps the most important limitation is that semantic attributes cannot usually be manipulated independently.

For example, changing facial expression while keeping identity, lighting, viewpoint, camera parameters, and all other visual properties unchanged is generally impossible using naturally collected datasets.

This makes controlled scientific experimentation considerably more difficult.

---

# Motivation for a Controllable Synthetic Dataset

The purpose of this project is not to replace existing public datasets.

Instead, it aims to complement them by creating a controllable synthetic dataset in which visual factors can be systematically adjusted while maintaining full experimental reproducibility.

Such control enables more rigorous investigation of representation learning, generative modeling, and generalization than is typically possible using unconstrained real-world image collections alone.
