# Existing Human Datasets

## Introduction

Public human image datasets have been the foundation of modern computer vision research. They have enabled remarkable progress in face recognition, facial analysis, image synthesis, human reconstruction, and generative modeling.

Over the past decade, numerous datasets have been introduced, each designed to address specific research challenges. Some emphasize large-scale identity recognition, while others focus on facial attributes, image quality, video-based analysis, or deepfake detection.

Although these datasets differ in their objectives and construction methodologies, they collectively provide the benchmark data used by much of today's computer vision community.

This section provides a brief overview of several representative datasets that have significantly influenced research in human-centered computer vision.

---

# Representative Public Datasets

## FFHQ

**Flickr-Faces-HQ (FFHQ)** is one of the most widely used datasets for high-quality face generation.

It contains high-resolution facial images with substantial variation in age, ethnicity, accessories, background, and lighting, making it particularly suitable for generative modeling and image synthesis.

Common applications include:

* GAN training
* Image generation
* Face editing
* Latent space exploration

---

## CelebA and CelebA-HQ

CelebA is a large-scale celebrity face dataset containing identity labels and numerous facial attribute annotations.

Its high-quality extension, CelebA-HQ, has become a standard benchmark for generative models and facial image manipulation.

Common applications include:

* Attribute prediction
* Face editing
* Conditional image generation
* Representation learning

---

## VGGFace2

VGGFace2 was designed primarily for face recognition.

Compared with earlier datasets, it provides greater variation in pose, age, illumination, and expression for each identity.

Common applications include:

* Face recognition
* Face verification
* Face representation learning

---

## LFW

Labeled Faces in the Wild (LFW) is one of the earliest benchmarks for unconstrained face verification.

Although relatively small by today's standards, it played a significant role in evaluating face recognition algorithms under real-world conditions.

Common applications include:

* Face verification
* Benchmark evaluation

---

## VoxCeleb

VoxCeleb consists of videos collected from public interviews and online media.

Because it contains temporal information, it is widely used in tasks involving both facial appearance and speech.

Common applications include:

* Talking-face generation
* Audio-visual learning
* Speaker recognition
* Video-based face analysis

---

## FaceForensics++

FaceForensics++ is a benchmark specifically designed for manipulated facial media.

It contains both authentic and synthetically altered videos generated using multiple face manipulation techniques.

Common applications include:

* Deepfake detection
* Manipulation localization
* Digital media forensics

---

## DeepFake Detection Challenge (DFDC)

The DFDC dataset was released to encourage research on deepfake detection.

It contains a large collection of manipulated videos generated under diverse recording conditions.

Common applications include:

* Deepfake detection
* Robustness evaluation
* Forensic analysis

---

# Summary

These datasets have collectively driven major advances in computer vision and generative modeling. They provide valuable resources for training and evaluating modern learning algorithms across a wide range of tasks.

However, they were created with different objectives and therefore offer varying levels of control over important factors such as identity, facial expression, viewpoint, illumination, and other semantic attributes.

Understanding these differences is essential before designing a controllable synthetic human dataset for systematic scientific experimentation.

The limitations arising from existing public datasets are discussed in the next section: **limitations.md**.
