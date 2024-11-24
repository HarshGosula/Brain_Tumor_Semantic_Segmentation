# Brain_Tumor_Semantic_Segmentation

## Overview
This repository contains an implementation of brain tumor semantic segmentation using a 3D U-Net architecture. The model performs automated segmentation of brain tumors from multimodal MRI scans using the BraTS (Brain Tumor Segmentation) dataset, achieving a Dice coefficient of 0.8018 and IoU of 0.7013.

## Model Performance
- **Dice Coefficient**: 0.8018
- **IoU (Intersection over Union)**: 0.7013

These metrics indicate robust segmentation performance:
- The Dice coefficient of 0.8018 shows strong overlap between predicted and ground truth segmentations
- The IoU of 0.7013 demonstrates effective region prediction and minimal false positives/negatives

## Model Architecture
The implementation uses a 3D U-Net architecture, which is specifically designed for volumetric medical image segmentation. Key features include:
- 3D convolutional layers for processing volumetric data
- Skip connections to preserve fine spatial information
- Deep supervision for improved gradient flow
- Batch normalization for stable training

## Dataset
This project uses the Brain Tumor Segmentation (BraTS) dataset, which is the standard benchmark for state-of-the-art brain tumor segmentation methods.

### Dataset Characteristics:
- **Source**: BraTS Challenge Dataset
- **Modalities**: Four MRI sequences
  - T1-weighted (T1)
  - T1-weighted with gadolinium contrast enhancement (T1ce)
  - T2-weighted (T2)
  - Fluid Attenuated Inversion Recovery (FLAIR)
- **Image Dimensions**: 240 × 240 × 155 (default)
- **Segmentation Labels**:
  - Label 0: Background
  - Label 1: Necrotic and Non-enhancing Tumor Core (NCR/NET)
  - Label 2: Peritumoral Edema (ED)
  - Label 4: Enhancing Tumor (ET)
 ## Requirements
```
python>=3.6
pytorch>=1.7.0
numpy
nibabel  # for reading medical images
scikit-learn
matplotlib
SimpleITK  # for preprocessing
```

## Installation
```
git clone https://github.com/HarshGosula/Brain_Tumor_Semantic_Segmentation.git

```

