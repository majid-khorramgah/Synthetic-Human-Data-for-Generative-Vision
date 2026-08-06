# Timeline

This timeline outlines the current progress of the project and its planned research direction. As the repository evolves, new milestones and experimental results will be added.

---

## Phase 1 — Project Definition

**Status:** Completed

* Defined the research motivation.
* Reviewed the limitations of existing public human datasets.
* Established the long-term research objective of studying controllable synthetic human data for representation learning.

---

## Phase 2 — Synthetic Dataset Generation

**Status:** Completed

A controllable synthetic human dataset was created for the initial stage of the project.

Current dataset:

* **100,000 synthetic facial images**
* **50,000 images of one synthetic female identity**
* **50,000 images of one synthetic male identity**

For each identity, a wide range of facial expressions was generated while maintaining identity consistency. This controlled setup provides a reproducible environment for studying generative models before introducing larger identity diversity.

---

## Phase 3 — Generative Model Training

**Status:** In Progress

The generated dataset is being used to train generative vision models.

Current objectives include:

* evaluating training stability;
* analyzing learned facial representations;
* documenting experimental observations.

---

## Phase 4 — Experimental Evaluation

**Status:** Planned

The trained models will be evaluated through both qualitative and quantitative analyses, including reconstruction quality, identity consistency, and observed limitations.

---

## Phase 5 — Expanding Synthetic Identity Diversity

**Status:** Future Work

The current dataset contains two synthetic identities.

Future versions of the dataset will progressively increase the number of controllable synthetic identities, enabling systematic experiments on the effect of identity diversity.

Examples include:

* 10 identities
* 50 identities
* 100 identities
* 500+ identities

---

## Phase 6 — Representation Analysis

**Status:** Future Work

The learned representations will be analyzed using embedding extraction, clustering, similarity analysis, dimensionality reduction, and other representation learning techniques.

---

## Phase 7 — Generalization

**Status:** Future Work

The long-term objective is to understand how increasing controllable synthetic identity diversity influences representation learning and generalization in generative vision models.

Ultimately, this research aims to answer a central scientific question:

> **How much synthetic identity diversity is required before a generative model learns transferable human representations instead of memorizing individual identities?**
