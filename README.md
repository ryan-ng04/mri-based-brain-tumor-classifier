# mri-based-brain-tumor-classifier
MRI-Based Brain Tumor Classification Using Convolutional Neural Networks and KNN algorithm

## 📌 Overview

This project classifies brain tumors in MRI images using two models:

- 🧠 **Convolutional Neural Network (CNN)**
- 🔍 **k-Nearest Neighbors (k-NN)**

The goal is to support medical professionals in diagnosing brain tumors more efficiently and accurately. The models were trained on a dataset of ~7,000 MRI scans labeled into four categories:
- Glioma
- Meningioma
- Pituitary Tumor
- No Tumor

---

## 🎯 Objectives

- Accurately classify MRI scans into tumor types
- Identify visual characteristics of each tumor class
- Evaluate performance differences between CNN and k-NN
- Understand which tumor type is most common in the dataset

---

## 📁 Dataset

The dataset combines contributions from:

- Figshare
- SARTAJ MRI dataset
- Br35H dataset

Each MRI image is labeled into one of the four categories. The dataset was pre-split into training and testing sets and underwent preprocessing, including:

- Image resizing to reduce dimensionality
- Conversion to NumPy arrays (`NumpyDataset`)
- Batch shuffling and normalization

---

## 📚 Related Work

1. **BMC Medical Imaging (2024):** A hybrid deep CNN model for tumor classification with 93–99% accuracy  
2. **Kaggle Contributor Notebook:** Used a pretrained CNN on the same dataset  
3. **CSCI 4521 Coursework:** Provided base CNN architecture and data handling patterns

---

## 🔧 Models

### 🧠 CNN

CNNs are deep learning models ideal for medical image classification. This project uses a custom CNN architecture featuring:

- Three convolutional layers with increasing channel depth
- Two residual blocks to preserve features
- Batch Normalization, ReLU activation, and MaxPooling

**Training Configuration:**
- Epochs: `20`
- Batch size: `100`
- Optimizer: `Adam`
- Learning rate: `0.0001`

---

### 🔍 k-NN

Used as a baseline for comparison. Implemented via `sklearn.neighbors.KNeighborsClassifier`.

- Evaluated `k` values from `1` to `91` (step size = 3)
- Selected best `k` based on test accuracy
- Additional analysis on values: `k = 1, 3, 5, 7, 9`

---

## 📊 Results

- CNN:
    - Testing Accuracy: 89.9%
    - Training Accuracy: 94.3%
- KNN:
    - Testing Accuracy = 71.8% at k =3
    - 
- CNN significantly outperforms k-NN in both accuracy and runtime.
- k-NN performance plateaus quickly and is unsuitable for large-scale image data.

---

## 📈 Visualizations

- CNN loss & accuracy graphs (initial and final)
- ROC curve and confusion matrix (CNN)
- k-NN accuracy vs. k-value plots

📂 Available in the `visuals/` directory.

---

## ⚠️ Limitations

- Only classifies four tumor types
- Accuracy may not be sufficient for clinical use
- Trained on limited datasets without real-time updates

**Future Improvements:**
- Train on more diverse tumor categories
- Explore transfer learning with ResNet or VGG
- Add live inference or model deployment via web app

---
