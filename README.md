# Household Object Classification

> A deep learning project focused on classifying common household objects, with potential applications in intelligent home robotics.

---

## Project Overview

This project explores image classification techniques to recognize common household objects. The long-term goal is to support intelligent robot vacuum systems that can identify objects and eventually build semantic maps of indoor environments.

- **Objective:** Classify household objects into five categories using deep learning.
- **Domain:** Computer Vision, Deep Learning, Smart Home Robotics
- **Key Techniques:** Image Classification, CNN, Transfer Learning, Data Augmentation

---

## Project Structure

```text
├── data/                 # Dataset information
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Results and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** [Furniture Image Dataset - Kaggle](https://www.kaggle.com/datasets/udaysankarmukherjee/furniture-image-dataset)
- **Description:** The dataset contains images of five household object categories:
  - Almirah (Wardrobe)
  - Chair
  - Fridge
  - Table
  - TV

---

## Analysis

The project will follow these steps:

1. **Data Exploration:** Examine class distributions, image dimensions, and sample images.
2. **Preprocessing:** Resize images and prepare training and validation datasets.
3. **Model Training:** Fine-tune a pretrained ResNet34 model using Fastai.
4. **Evaluation:** Evaluate performance using accuracy and a confusion matrix.
5. **Model Improvement:** Experiment with data augmentation and training configurations.

---

## Results

Results will be added after model training and evaluation.

---

## Future Work

Extend the image classification model to object detection and semantic mapping for intelligent robot vacuum applications.
