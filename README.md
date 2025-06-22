# mri-based-brain-tumor-classifier
MRI-Based Brain Tumor Classification Using Convolutional Neural Networks and KNN algorithm

📋 Overview
This project explores the classification of brain tumors using two machine learning approaches: Convolutional Neural Networks (CNNs) and k-Nearest Neighbors (KNN). The primary objective is to support medical professionals by providing automated, accurate classification of brain tumors to improve diagnostic efficiency and treatment planning.

The models are trained on a combined dataset of ~7,000 MRI brain scans and classify images into one of four tumor types:

Glioma

Meningioma

Pituitary

No Tumor

💡 Motivation

Assist in the early detection and classification of brain tumors.

Analyze key patterns and features of tumor types.

Improve understanding and accessibility of complex medical diagnoses.

Answer key questions:

What characteristics are commonly found in each tumor type?

What is the most common tumor type in the dataset?

📁 Dataset

Sourced from Figshare, SARTAJ, and Br35H datasets.

Total images: ~7,000 MRIs

Pre-labeled into 4 categories.

Already split into training and testing subsets.

Preprocessing
Images were resized to reduce dimensionality (pixel count).

Data loaded and structured using NumpyDataset for compatibility.

Feature normalization and batch shuffling applied.

📚 Related Work

[Source 1: BMC Medical Imaging (2024)]
A hybrid deep CNN approach achieving 93–99% accuracy on similar classification tasks.

[Source 2: Kaggle MRI Classification Notebook]
A CNN-based notebook utilizing pretrained models on the same dataset.

⚙️ Models

1. Convolutional Neural Network (CNN)
Deep learning model capable of extracting hierarchical spatial features from medical images.

Architecture:
Convolution + Pooling → Residual Block → Convolution + Pooling → Residual Block → Convolution + Pooling

Batch Normalization, ReLU activations, MaxPooling used throughout.

Trained for 20 epochs, with:

Batch Size: 100

Optimizer: Adam

Learning Rate: 0.0001

2. k-Nearest Neighbors (KNN)
A simple, non-parametric classification model used as a baseline.

Implemented using sklearn.neighbors.

k-value tuned via testing accuracy from k = 1 to 91 (step 3).

Final selection based on accuracy plateau and runtime efficiency.

📊 Results

📈 CNN Performance:
Training Accuracy: 94.3%

Testing Accuracy: 89.9%

ROC Curve & Confusion Matrix provided in visualizations

📉 KNN Performance:
Best Test Accuracy: 71.77% (at k=3)

Accuracy Range: 57% – 75%

Much slower and less accurate than CNN

📸 Visualizations

Loss & Accuracy graphs (initial/final CNN)

Tumor prediction samples

KNN performance across varying k

CNN Confusion Matrix & ROC Curve

🧪 Limitations & Future Work

Currently limited to 4 tumor types; real-world models should include more.

Accuracy, while strong, is not on par with production-ready models used in hospitals.

Future improvements:

Larger datasets with broader tumor representation.

Real-time model updating.

Transfer learning with pretrained models like ResNet, VGG, or DenseNet.

🔗 References
Srinivasan et al. (2024). A hybrid deep CNN model for brain tumor image multi-classification. BMC Med Imaging. DOI link

Brain Tumor MRI Classification on GitHub
