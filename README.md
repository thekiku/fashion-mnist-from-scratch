# Fashion-MNIST Classifier 

A complete implementation of a feedforward neural network built entirely from scratch using NumPy for classifying the Fashion-MNIST dataset.

The purpose of this project is to understand how image classification works internally by implementing every major component of a neural network manually instead of relying on high-level deep learning frameworks such as TensorFlow or PyTorch. Every layer, activation function, loss function, optimizer, and training step has been implemented from first principles using only NumPy.

The project demonstrates the complete workflow of image classification, from preprocessing Fashion-MNIST images to training, evaluating, saving, loading, and performing inference on previously unseen images.

---

# Architecture

The overall pipeline consists of three main stages:

1. **Image Preprocessing**
   - Input images are converted to grayscale (if required).
   - Images are resized to **28 × 28** pixels.
   - Each image is flattened into a vector of **784 input features** (28 × 28 = 784), where each feature represents a single pixel intensity.

2. **Feedforward Neural Network**
   - The flattened image is passed through two fully connected hidden layers with **ReLU** activation.
   - The final output layer contains **10 neurons**, one for each Fashion-MNIST class.
   - A **Softmax** activation converts the output scores into class probabilities.

3. **Training**
   - The network is trained using **Categorical Cross-Entropy Loss**.
   - Parameters are updated using the **Adam optimizer** with learning-rate decay and L2 regularization.

### Overall Pipeline

<img width="6724" height="2524" alt="image" src="https://github.com/user-attachments/assets/d00edbea-095a-4be2-9b9f-54e663e7639f" />


The figure above illustrates how an input image is preprocessed into a 784-dimensional feature vector before being passed through the neural network to produce probabilities for each clothing category.

### Model Configuration

<img width="4352" height="2910" alt="image" src="https://github.com/user-attachments/assets/623ce34c-8f48-45a1-9ab1-0121b3ea831e" />


The implementation uses the following architecture:

```
Input Layer      : 784 neurons (28×28 pixels)
Hidden Layer 1   : 128 neurons + ReLU
Hidden Layer 2   : 128 neurons + ReLU
Output Layer     : 10 neurons + Softmax
Optimizer        : Adam
Loss Function    : Categorical Cross-Entropy
Regularization   : L2
```

The hidden layer sizes are configurable and can be changed easily. For this implementation, **128 neurons** were chosen for both hidden layers as a balance between model capacity and computational efficiency.

---

## Features

- Fully Connected (Dense) Layers
- Forward Propagation
- Backpropagation
- ReLU Activation
- Softmax Activation
- Categorical Cross-Entropy Loss
- Combined Softmax and Cross-Entropy Optimization
- L1 Regularization
- L2 Regularization
- Adam Optimizer
- Learning Rate Decay
- Accuracy Calculation
- Mini-Batch Training
- Model Saving
- Model Loading
- Prediction on Unseen Images
- Fashion-MNIST Image Classification
- Custom Image Testing

---

## Dataset

The project uses the **Fashion-MNIST** dataset, consisting of grayscale images of clothing items across 10 classes.

<img width="1186" height="497" alt="image" src="https://github.com/user-attachments/assets/c5732729-cb50-424a-952b-67f5dae2739e" />

Classes include:

- T-shirt/Top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle Boot

The dataset is included in this repository under the `fashion_mnist_images` directory, allowing the project to run without requiring any additional downloads.

---

## Tech Stack

- Python
- NumPy
- OpenCV
- NNFS

---

## Project Structure

```text
fashion-mnist-from-scratch/
│
├── .gitignore
├── LICENSE
├── README.md
├── requirements.txt
│
├── fashion_mnist_images/
│   ├── train/
│   └── test/
│
├── load_data.py
├── main.py
├── train.py
├── test.py
└── test_image.png
```

---

## Getting Started

Clone the repository.

```bash
git clone https://github.com/thekiku/fashion-mnist-from-scratch.git
```

Move into the project directory.

```bash
cd fashion-mnist-from-scratch
```

Install the required dependencies.

```bash
pip install -r requirements.txt
```

Train the model.

```bash
python train.py
```

Test the trained model on a custom image.

```bash
python test.py
```

---

## What This Project Demonstrates

This project demonstrates the complete workflow of training a neural network for image classification without using any deep learning framework.

Every component is implemented manually, including dense layer computations, forward propagation, backpropagation, gradient descent using the Adam optimizer, L1/L2 regularization, learning rate decay, model serialization, and inference on unseen images.

Rather than treating neural networks as black boxes, this implementation exposes every mathematical operation involved during both training and prediction, providing a deeper understanding of how modern deep learning systems classify images.

---

## Learning Reference

This implementation closely follows the concepts presented in:

**Neural Networks from Scratch in Python**

**Authors:** Harrison Kinsley and Daniel Kukieła

---

## Current Status

This repository contains a complete NumPy implementation of a feedforward neural network trained on the Fashion-MNIST dataset. It serves as both a personal learning project and a practical demonstration of the core algorithms behind modern image classification systems.

---

## Requirements

- Python 3.10+
- NumPy
- OpenCV
- NNFS

Install all dependencies with:

```bash
pip install -r requirements.txt
```

---

## License

This project is released under the MIT License.
