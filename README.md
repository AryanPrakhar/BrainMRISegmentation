# Brain MRI Tumor Segmentation

This project implements a deep learning pipeline for detecting and segmenting brain tumors in MRI images.

## Overview

The system uses a two-stage approach:

1. A classification model to detect the presence of tumors
2. A segmentation model to localize and outline tumors when detected

Key components:

- Data preprocessing and visualization 
- ResNet50-based classification model
- ResUNet segmentation model
- Custom loss functions (Focal Tversky loss)
- Evaluation metrics and result visualization

## Dataset

The project uses the LGG MRI Segmentation dataset, containing brain MRI images and corresponding tumor mask annotations.

## Models

### Classification Model
- Based on ResNet50 architecture 
- Detects presence/absence of tumors

### Segmentation Model  
- Custom ResUNet architecture
- Generates pixel-wise tumor masks

## Usage

The main notebook `BrainMRIseg.ipynb` contains the full pipeline:

1. Data loading and preprocessing
2. Model training (classification and segmentation)  
3. Evaluation and visualization of results

## Results

- Classification accuracy: 93.75%
- Segmentation Tversky score: 85.10%

Combining classification and segmentation can potentially reduce false positives and provide more detailed information about tumor presence and location.

Sample segmentation results are visualized in the notebook.

## Requirements

- TensorFlow 2.x
- Keras
- OpenCV
- scikit-image
- pandas
- matplotlib

## Future Work

- Experiment with other architectures
- Implement additional data augmentation
- Explore multi-class segmentation for different tumor types
