# Model Training

This module documents the complete training workflow used to build the face-swapping models employed throughout the project. The training process is based on DeepFaceLab and uses the synthetic dataset generated in the previous stage.

The objective of this stage is to fine-tune a pretrained SAEHD model using the custom synthetic dataset while preserving facial identity, improving expression consistency, and enabling robust real-time deployment through DeepFaceLive.

---

## Module Structure

```
03_model_training/
│
├── README.md
├── training_pipeline.md
├── training_configuration.md
├── training_logs.md
├── deepfacelab.md
├── deepfacelive.md
└── figures/
```

---

## Documentation

| Document | Description |
|-----------|-------------|
| **training_pipeline.md** | Complete model training workflow. |
| **training_configuration.md** | Hardware, hyperparameters, and training settings. |
| **training_logs.md** | Monitoring metrics, checkpoints, convergence, and training observations. |
| **deepfacelab.md** | DeepFaceLab workflow and SAEHD training process. |
| **deepfacelive.md** | Real-time deployment using DeepFaceLive. |

---

## Training Workflow

The complete workflow consists of five major stages:

1. Dataset preparation
2. DeepFaceLab preprocessing
3. SAEHD model fine-tuning
4. Model export
5. Real-time deployment using DeepFaceLive

---

## Figures

### Training Architecture

<p align="center">
<img src="figures/deployment_flow.png" width="900">
</p>

---

### DeepFaceLive Processing

<p align="center">
<img src="figures/deepfacelive_pipeline.png" width="900">
</p>

---

### User Interface

<p align="center">
<img src="figures/interface_overview.png" width="900">
</p>

---

### Input / Output Example

<p align="center">
<img src="figures/input_output_example.png" width="900">
</p>

---

### Real-Time Inference

<p align="center">
<img src="figures/realtime_demo.png" width="900">
</p>

---

## Summary

This module provides complete documentation of the model training process, from synthetic dataset preparation to pretrained model fine-tuning and deployment for real-time face swapping applications.
