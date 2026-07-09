# How CNN Sees: Visualizing and Exploring Feature Maps & Filters

This notebook explores how a Convolutional Neural Network (CNN) processes images internally by visualizing convolutional filters and feature maps using the pre-trained VGG16 model.

## What is CNN Visualization?

When we use a CNN for image classification, it predicts the output, but we often don't know what happens inside the network.

CNN visualization helps us understand:

- What features each convolution layer learns
- How filters detect patterns in an image
- How feature maps change from one layer to another
- How the network gradually recognizes objects

Instead of treating CNNs as a black box, this project explains how they interpret visual information.

## Model Used

**VGG16**

VGG16 is a deep Convolutional Neural Network consisting of 16 learnable layers. It is pre-trained on the ImageNet dataset and is widely used for feature extraction and image classification tasks.

## What I Did

- Loaded the pre-trained VGG16 model.
- Loaded and preprocessed an input image.
- Extracted convolutional filters from the first layer.
- Visualized the learned filters.
- Built an intermediate model to obtain feature maps.
- Displayed feature maps from different convolution layers.
- Observed how image representations change throughout the network.

## What I Learned

- CNNs learn features automatically during training.
- Early layers detect edges, lines, and textures.
- Middle layers recognize shapes and patterns.
- Deeper layers capture high-level object features.
- Feature maps provide insight into what each convolution layer focuses on.
- Visualizing filters and feature maps makes CNNs easier to understand and interpret.

## Tools Used

- Python
- TensorFlow
- Keras
- VGG16
- NumPy
- Matplotlib

## Colab Link

https://colab.research.google.com/drive/1Lyw03SY5BLpu4yqsD9ilseQ1LoKubgY-?usp=sharing

## Author

Sakshitha  
B.Tech CSE | SR University  
09/07/2026
