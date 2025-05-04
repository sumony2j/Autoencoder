# Autoencoder

## Autoencoder Architectures on MNIST using TensorFlow

This repository demonstrates various types of **Autoencoders** implemented using **TensorFlow** and trained on the **MNIST** handwritten digits dataset.

---

## 🔍 What is an Autoencoder?

An **Autoencoder** is a type of neural network designed to learn a compressed representation of input data in an unsupervised manner. It consists of two main parts:

- **Encoder**: Compresses the input into a lower-dimensional latent space.
- **Decoder**: Reconstructs the input from this compressed representation.

Autoencoders are widely used for:

- Dimensionality reduction
- Image compression
- Denoising
- Anomaly detection

---

## 🧠 Autoencoder Variants Implemented

All the following models are implemented in the `Autoencoder.ipynb` notebook:

### 1. Vanilla Autoencoder

A simple feedforward neural network with:

- **Input layer**: 784 units (flattened 28x28 MNIST image)
- **Encoding layer**: 64 units
- **Decoding layer**: 784 units

This model demonstrates basic compression and reconstruction using a single hidden layer.

---

### 2. Multi-layer Autoencoder (Deep Autoencoder)

A deeper architecture that captures more complex features:

- **Input layer**: 784 units
- **Encoder layer 1**: 256 units
- **Encoder layer 2**: 128 units
- **Latent (bottleneck) layer**: 64 units
- **Decoder layer 1**: 128 units
- **Decoder layer 2**: 256 units
- **Output layer**: 784 units

This model gradually reduces and expands the data through multiple hidden layers.

---

### 3. Convolutional Autoencoder

A convolutional architecture designed for image data, preserving spatial features:

- **Input**: 28x28x1 (grayscale image)
- **Encoder**:
  - Convolution + Pooling layers with increasing filters (64 → 128 → 64)
- **Latent space**: compressed feature maps
- **Decoder**:
  - Convolution + Upsampling layers with filters (64 → 128 → 256)
  - Final convolution layer to reconstruct the output image

This model is more effective for learning spatial hierarchies in image data.

---

## 📊 Dataset

All models are trained and evaluated on the **MNIST** dataset, consisting of 60,000 training images and 10,000 test images of handwritten digits, each sized 28x28 pixels.

---

## 🧩 Requirements

To run the notebook, install the following Python packages:

```bash
pip install tensorflow numpy pandas matplotlib
```
---

## 🛠️ Framework

- Implemented using **TensorFlow 2.x**
- Jupyter notebook: `Autoencoder.ipynb`

---

## ✅ Summary

This project showcases different Autoencoder architectures—ranging from basic to deep to convolutional—all implemented within one notebook. It illustrates how well different model structures can compress and reconstruct image data from the MNIST dataset.
