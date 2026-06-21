#  Exploring LeNet-5 Architecture

This notebook is my exploration of **LeNet-5**, one of the earliest and most influential Convolutional Neural Networks (CNNs) proposed by Yann LeCun.

The primary objective of this project was to understand the internal working of CNNs, explore the LeNet-5 architecture layer by layer, and gain intuition about concepts such as feature extraction, pooling, and overfitting.

---

## About LeNet-5

LeNet-5 was introduced by **Yann LeCun in 1998** for handwritten digit recognition. It is considered one of the foundational architectures in Deep Learning and inspired many modern CNN architectures.

It consists of convolutional layers for feature extraction, pooling layers for dimensionality reduction, and fully connected layers for classification.

---

##  Architecture

| Layer | Configuration | Output Shape |
| :--- | :--- | :--- |
| Input | 32 × 32 × 1 Grayscale Image | 32 × 32 × 1 |
| C1 | Convolution (6 filters, 5×5), Tanh | 28 × 28 × 6 |
| S2 | Average Pooling (2×2, stride 2) | 14 × 14 × 6 |
| C3 | Convolution (16 filters, 5×5), Tanh | 10 × 10 × 16 |
| S4 | Average Pooling (2×2, stride 2) | 5 × 5 × 16 |
| Flatten | Converts feature maps into vector | 400 |
| C5 | Fully Connected Layer (120 neurons) | 120 |
| F6 | Fully Connected Layer (84 neurons) | 84 |
| Output | Dense Layer (10 neurons, Softmax) | 10 |

### Architecture Flow

```text
Input (32×32×1)
        │
        ▼
Conv2D (6 filters, 5×5)
        │
        ▼
Average Pooling (2×2)
        │
        ▼
Conv2D (16 filters, 5×5)
        │
        ▼
Average Pooling (2×2)
        │
        ▼
Flatten
        │
        ▼
Dense (120)
        │
        ▼
Dense (84)
        │
        ▼
Output Dense (10, Softmax)
```

---

##  What I Learned

During this exploration, I learned:

- The difference between **Artificial Neural Networks (ANNs)** and **Convolutional Neural Networks (CNNs)**.
- How convolutional layers use filters to extract meaningful features from images.
- How pooling layers reduce the spatial dimensions while preserving important information.
- The purpose of the **Flatten** layer in converting feature maps into vectors.
- How to build, train, and evaluate CNN models using **TensorFlow/Keras**.

---



## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Google Colab

---
## GOOGLE COLAB NOTEBOOK

View the complete notebook here:

https://colab.research.google.com/drive/1v8D_657Ih8k_htIh5vcKRYHlqZeYpWDW?usp=sharing

---

## AUTHOR

**SAKSHITHA**

- B.Tech Student

**Date** 21 June 2026


