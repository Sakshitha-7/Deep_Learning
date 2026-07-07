# Dog vs Cat Image Classification using Convolutional Neural Networks (CNN)

This notebook is my exploration of **Convolutional Neural Networks (CNNs)** through the classic **Dog vs Cat Image Classification** problem.

The primary objective of this project was to understand the complete workflow of image classification using CNNs, identify the problem of **overfitting**, and explore how techniques like **Batch Normalization** and **Dropout** improve a model's ability to generalize to unseen data.

Rather than focusing only on achieving high accuracy, this project emphasizes understanding why a model performs the way it does and how architectural improvements can lead to better real-world performance.

---

# About the Project

Dog vs Cat Classification is a binary image classification task where the model predicts whether an input image belongs to a **dog** or a **cat**.

In this notebook, I developed and compared **two CNN models**:

- **Model 1:** A baseline CNN architecture built from scratch.
- **Model 2:** An improved CNN architecture incorporating **Batch Normalization** and **Dropout** to reduce overfitting.

After training both models, I compared their performance using training and validation metrics and finally tested the improved model on unseen images.

---

# Model 1: Initial CNN Architecture

The first CNN model serves as a baseline architecture to understand how convolutional neural networks learn image features and to observe common issues such as overfitting.

### Architecture

| Layer | Configuration |
|--------|---------------|
| Input | 256 × 256 × 3 RGB Image |
| Conv2D | 32 Filters (3×3), ReLU |
| MaxPooling2D | 2 × 2 |
| Conv2D | 64 Filters (3×3), ReLU |
| MaxPooling2D | 2 × 2 |
| Conv2D | 128 Filters (3×3), ReLU |
| MaxPooling2D | 2 × 2 |
| Flatten | Converts Feature Maps into Vector |
| Dense | 128 Neurons, ReLU |
| Output | Dense (1 Neuron, Sigmoid) |

---

# Understanding Overfitting

After training the first model, the training accuracy increased rapidly while the validation accuracy remained significantly lower.

This indicates **overfitting**, where the model memorizes the training data instead of learning features that generalize well to unseen images.

To overcome this issue, I explored regularization techniques.

---

# Batch Normalization

Batch Normalization standardizes the inputs of each layer during training.

Benefits include:

- Faster convergence
- More stable training
- Reduced sensitivity to weight initialization
- Acts as a regularizer that helps improve generalization

---

# Dropout

Dropout randomly deactivates a fraction of neurons during training.

Benefits include:

- Prevents co-adaptation of neurons
- Reduces overfitting
- Improves the model's ability to generalize to unseen data

---

# Model 2: Improved CNN Architecture

The second model extends the baseline architecture by incorporating:

- Batch Normalization
- Dropout Layers

These improvements reduce overfitting while maintaining strong learning performance.

---

# Architecture Flow

```
Input Image
      │
      ▼
Image Preprocessing
      │
      ▼
Conv2D
      │
      ▼
Batch Normalization
      │
      ▼
ReLU
      │
      ▼
MaxPooling
      │
      ▼
Dropout
      │
      ▼
Repeat Convolution Blocks
      │
      ▼
Flatten
      │
      ▼
Dense Layer
      │
      ▼
Sigmoid Output
      │
      ▼
Dog / Cat Prediction
```

---

# Model Comparison

| Model | Training Accuracy | Validation Accuracy |
|--------|------------------:|--------------------:|
| Model 1 (Baseline CNN) | **98.94%** | **75.44%** |
| Model 2 (Batch Normalization + Dropout) | **96.71%** | **80.14%** |

Although Model 1 achieved a very high training accuracy, it suffered from **overfitting**, leading to poor validation performance.

By introducing **Batch Normalization** and **Dropout**, Model 2 achieved better generalization and improved validation accuracy, making it more reliable for predicting unseen images.

---

# Prediction on New Images

After training the improved model, I tested it on unseen images.

The model predicts:

- **1 → Dog**
- **0 → Cat**

This demonstrates how a trained CNN can perform binary image classification on new data.

---

# What I Learned

During this exploration, I learned:

- The difference between traditional Machine Learning and Deep Learning for image classification.
- How Convolutional Neural Networks automatically learn visual features from images.
- How convolutional layers extract edges, textures, and higher-level image features.
- The importance of Max Pooling in reducing spatial dimensions.
- How to preprocess image datasets using TensorFlow.
- How to build CNN architectures using TensorFlow/Keras.
- How to train and evaluate deep learning models.
- How to detect overfitting using training and validation curves.
- Why Batch Normalization improves training stability.
- How Dropout acts as a regularization technique.
- How to compare different CNN architectures.
- How to make predictions on unseen images using a trained model.

---

# Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Google Colab

---

# Future Improvements

- Apply Data Augmentation
- Experiment with deeper CNN architectures
- Implement Early Stopping
- Tune hyperparameters
- Compare with Transfer Learning models such as VGG16, ResNet50, and EfficientNet
- Deploy the model as a web application using Streamlit or Flask

---

# Google Colab Notebook

View the complete notebook here:

**https://colab.research.google.com/drive/1iblJrpPeOjoRtm_9CLstAYEPQcNiIDNM?usp=sharing**

---

# Author

**SAKSHITHA**

B.Tech Student

**Date:** 07 July 2026
