# Household Object Classification

> A deep learning project focused on classifying common household objects using computer vision, with potential applications in intelligent home robotics.

---

## Project Overview

This project uses transfer learning to classify household furniture images into five categories. The project is inspired by intelligent robot vacuum systems that need to recognize objects in indoor environments.

- **Objective:** Develop an image classifier capable of recognizing five furniture categories.
- **Domain:** Computer Vision, Deep Learning, Smart Home Robotics
- **Key Techniques:** Image Classification, Transfer Learning, ResNet34, Data Augmentation

---

## Project Structure

```text
├── data/                 # Dataset information
├── code/                 # Jupyter notebooks
├── reports/              # Results and visualizations
├── .gitignore
└── README.md             # Project documentation
```

---

## Data

- **Source:** [Furniture Detector — Kaggle](https://www.kaggle.com/datasets/akkithetechie/furniture-detector)
- **Categories:** Bed, Chair, Sofa, Swivel Chair, Table
- **Original Dataset:** 4,447 images
- **Cleaned Dataset:** 4,444 images after removing exact duplicates and conflicting labels
- **Training Set:** 3,556 images (80%)
- **Validation Set:** 888 images (20%)

The dataset contains fewer table images than the other four categories.

---

## Analysis

I used the Fastai library to fine-tune a pretrained ResNet34 convolutional neural network.

The analysis includes:

1. **Data Exploration:** Examined the dataset structure, class distributions, and sample images.
2. **Data Cleaning:** Identified and removed duplicate images and conflicting labels.
3. **Preprocessing:** Resized images to 460 × 460 pixels and applied data augmentation to produce 224 × 224 images.
4. **Model Training:** Fine-tuned a pretrained ResNet34 model using transfer learning.
5. **Model Evaluation:** Evaluated validation accuracy, error rate, confusion matrix, and highest-loss predictions.
6. **External Testing:** Tested the model on an image downloaded from outside the Kaggle dataset.

---

## Results

The ResNet34 model achieved:

| Metric | Result |
|---|---|
| Validation Accuracy | **97.30%** |
| Validation Error Rate | **2.70%** |
| Validation Images | 888 |
| Correct Predictions | 864 |

The confusion matrix showed that most misclassifications occurred between **chairs and swivel chairs**, which have similar visual features.

The model also correctly classified an external chair image from Wikimedia Commons with a displayed confidence score of **100.00%**.

These results demonstrate strong classification performance on the validation dataset, although additional external testing would help assess real-world generalization.

---

## Notebook

The complete analysis, including code, visualizations, and model evaluation, is available here:

- [Google Colab Notebook](https://colab.research.google.com/drive/1swLhB3S5_2C4kONI1eiwiWWJ7TvIYzir)
- [GitHub Notebook](code/household_object_classification.ipynb)

To reproduce the analysis, open the notebook in Google Colab, select a GPU runtime if available, and run the cells in order. The notebook downloads the dataset directly from Kaggle.

---

## Future Work

The long-term goal is to extend this project to **object detection and semantic mapping**, allowing intelligent home robots to recognize multiple household objects and identify their locations within indoor environments.
