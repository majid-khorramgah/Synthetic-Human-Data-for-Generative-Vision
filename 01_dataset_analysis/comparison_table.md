# Comparison of Existing Face Datasets

This table summarizes representative face datasets that are commonly used in face recognition, generative modeling, and deepfake research. The comparison focuses on characteristics relevant to this project rather than providing an exhaustive survey.

| Dataset         |    Images / Videos |   Identities | Resolution | Controlled Conditions | Primary Application   |
| --------------- | -----------------: | -----------: | ---------- | --------------------- | --------------------- |
| FFHQ            |      70,000 images |       ~7,000 | 1024×1024  | No                    | GAN Training          |
| CelebA          |     202,599 images |       10,177 | Various    | No                    | Face Attributes       |
| CelebA-HQ       |      30,000 images |       10,177 | 1024×1024  | No                    | Image Generation      |
| VGGFace2        |       3.31M images |        9,131 | Various    | No                    | Face Recognition      |
| LFW             |      13,233 images |        5,749 | Various    | No                    | Face Verification     |
| VoxCeleb2       | 1M+ frames (video) |        6,112 | Various    | No                    | Audio-Visual Learning |
| FaceForensics++ |      1,000+ videos |     Multiple | Various    | No                    | Deepfake Detection    |
| DFDC            |    100,000+ videos | 3,426 actors | Various    | No                    | Deepfake Detection    |

---

# Example DeepFakeVFX Facesets

The following examples illustrate the characteristics of community-created facesets available through DeepFakeVFX.

| Faceset           | Images | Resolution | Face Type | XSeg   |
| ----------------- | -----: | ---------: | --------- | ------ |
| Edward Norton     | 67,044 |        512 | WF        | Custom |
| Hannah Stein      | 30,078 |        512 | WF        | None   |
| Tom Selleck       | 26,245 |       1024 | Head      | None   |
| Jennifer Lawrence | 20,699 |        512 | WF        | Custom |
| Dasha Taran       | 24,036 |        512 | WF        | None   |

These facesets are primarily designed for DeepFaceLab training and typically contain images of a **single individual** collected from videos or photographs. Image quality, pose distribution, lighting, and facial expressions depend on the available source material rather than a controlled acquisition process.

---

# Synthetic Dataset Used in This Project

| Property             | Value                                               |
| -------------------- | --------------------------------------------------- |
| Dataset Type         | Synthetic Human Faces                               |
| Total Images         | **100,000**                                         |
| Female Images        | **50,000**                                          |
| Male Images          | **50,000**                                          |
| Synthetic Identities | **2 (1 female, 1 male)**                            |
| Facial Expressions   | Extensive variation                                 |
| Identity Consistency | Fully controlled                                    |
| Rendering Pipeline   | DAZ Studio                                          |
| Purpose              | Representation Learning & Generative Model Research |

---

# Key Differences

Unlike public face datasets or community facesets, the synthetic dataset developed in this project was generated under a fully controllable rendering pipeline.

Rather than maximizing the number of identities, the current version intentionally maintains only two synthetic identities while varying facial expressions under reproducible conditions. This design enables controlled experiments in which changes in facial appearance can be studied without introducing uncontrolled identity variation.

Future versions of the dataset will progressively increase the number of synthetic identities to investigate how identity diversity influences representation learning and generalization.
