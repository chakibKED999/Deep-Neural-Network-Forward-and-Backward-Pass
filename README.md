# 🧠 Deep Neural Network From Scratch using NumPy

> A complete implementation of a Deep Neural Network entirely from scratch using NumPy, covering forward propagation, backpropagation, binary and multiclass classification, activation functions, loss functions, and gradient computation without using any deep learning framework.

![Python](https://img.shields.io/badge/Python-3.10-blue)
![NumPy](https://img.shields.io/badge/NumPy-Numerical_Computing-orange)
![DeepLearning](https://img.shields.io/badge/Deep_Learning-From_Scratch-green)
![NeuralNetwork](https://img.shields.io/badge/Neural_Network-Backpropagation-red)
![Master](https://img.shields.io/badge/Master-MIV-lightgrey)

---

# 📖 Overview

This project demonstrates how a modern **Deep Neural Network (DNN)** can be implemented entirely from scratch using only **NumPy**.

Rather than relying on high-level deep learning libraries such as PyTorch or TensorFlow, every major component of the learning process is manually developed, allowing a complete understanding of how neural networks operate internally.

The implementation includes:

- Deep network construction
- Forward propagation
- ReLU activation
- Sigmoid activation
- Softmax activation
- Binary classification
- Multiclass classification
- Negative Log-Likelihood Loss (NLL)
- Backpropagation
- Gradient computation

This project was developed as part of the **Master's Program in Image Processing & Artificial Intelligence (MIV)** at **USTHB**.

---

# ✨ Features

- 🧠 Fully connected Deep Neural Network
- 📈 Configurable number of hidden layers
- 🔥 ReLU activation implementation
- 🎯 Sigmoid function for binary classification
- 🌍 Softmax function for multiclass classification
- 📊 Binary Negative Log-Likelihood Loss
- 📊 Multiclass Negative Log-Likelihood Loss
- 🔄 Complete Forward Pass
- 🔁 Complete Backward Pass
- ⚙️ Manual gradient computation
- 📚 One-Hot Encoding
- 🚀 Pure NumPy implementation
- ❌ No TensorFlow
- ❌ No PyTorch
- ✅ Educational implementation

---

# 📑 Project Report

## Project Objective

The objective of this project is to understand and implement every component of a Deep Neural Network without relying on existing deep learning libraries.

Most modern AI frameworks automatically perform forward propagation, compute gradients, and update model parameters through automatic differentiation. Although convenient, these abstractions hide the mathematical principles behind deep learning.

This project recreates the complete learning pipeline from first principles, providing a clear understanding of:

- Neural network architecture
- Matrix-based computations
- Activation functions
- Loss computation
- Gradient propagation
- Optimization foundations

The implementation serves as an educational framework for learning how deep learning models function internally.

---

# 🧠 Why Build a Neural Network from Scratch?

Implementing a neural network manually offers several advantages:

- Better understanding of neural network mathematics
- Deeper knowledge of gradient descent
- Understanding of computational graphs
- Improved debugging skills
- Foundation for advanced deep learning research

Instead of treating neural networks as black boxes, this project exposes every mathematical operation involved during learning.

---

# 🏗️ Neural Network Architecture

The implemented model is a fully connected feed-forward neural network composed of:

- Input Layer
- Multiple Hidden Layers
- Output Layer

Each layer performs the following computation:

```
Linear Transformation

Z = W × X + b
```

followed by a nonlinear activation function.

The architecture supports an arbitrary number of hidden layers, making the implementation flexible for different experiments.

---

# 🔥 ReLU Activation

Hidden layers use the Rectified Linear Unit (ReLU):

```
ReLU(x) = max(0, x)
```

ReLU is widely used because it:

- reduces vanishing gradients
- accelerates convergence
- is computationally efficient
- introduces non-linearity

---

# 🎯 Binary Classification

For binary classification problems, the network predicts the probability of belonging to class 1.

The final output uses the **Sigmoid** activation:

```
σ(x)=1/(1+e^-x)
```

Output values lie between:

```
0 and 1
```

making them interpretable as probabilities.

---

# 🌍 Multiclass Classification

For multiclass problems, the project implements the **Softmax** activation.

Softmax transforms arbitrary output values (logits) into a valid probability distribution.

The probabilities satisfy:

- Positive values
- Sum equals 1

making them suitable for multi-class prediction.

---

# 📊 Loss Functions

Two loss functions are implemented.

## Binary Negative Log-Likelihood (Binary NLL)

Used for binary classification tasks.

Advantages:

- probabilistic interpretation
- stable optimization
- standard for binary classifiers

---

## Multiclass Negative Log-Likelihood

Used after Softmax for multiclass classification.

The implementation computes the likelihood of the correct class and minimizes its negative logarithm.

---

# 🔄 Forward Propagation

The forward pass computes predictions layer by layer.

Pipeline:

```
Input

↓

Linear Layer

↓

Activation Function

↓

Hidden Layer

↓

...

↓

Output Layer

↓

Prediction
```

Each layer stores intermediate activations required later during backpropagation.

---

# 🔁 Backpropagation

One of the most important parts of the project is the manual implementation of **Backpropagation**.

The algorithm computes gradients using the Chain Rule.

Gradients are propagated backward through every layer to determine how each parameter contributes to the prediction error.

The project computes gradients for:

- Weights
- Biases
- Activations
- Logits

without relying on automatic differentiation.

---

# 🧮 One-Hot Encoding

Multiclass labels are transformed into one-hot vectors.

Example:

```
Class 0 → [1 0 0]

Class 1 → [0 1 0]

Class 2 → [0 0 1]
```

This representation is required for Softmax-based classification.

---

# ⚙️ Mathematical Components

The project manually implements:

- Matrix multiplication
- Linear layers
- ReLU activation
- Sigmoid activation
- Softmax activation
- Binary likelihood
- Binary NLL
- Multiclass likelihood
- Multiclass NLL
- Gradient computation
- Indicator function
- Forward propagation
- Backward propagation

---

# 🏗️ Pipeline

## 1️⃣ Network Initialization

- Create weights
- Initialize biases
- Define hidden layer dimensions

---

## 2️⃣ Forward Pass

For every layer:

- Linear transformation
- Activation function
- Save intermediate values

---

## 3️⃣ Prediction

Binary:

- Sigmoid

Multiclass:

- Softmax

---

## 4️⃣ Loss Computation

Binary:

- Binary Likelihood
- Binary NLL

Multiclass:

- Softmax
- Multiclass NLL

---

## 5️⃣ Backpropagation

Compute gradients using:

- Chain Rule
- Matrix calculus
- Stored activations

---

## 6️⃣ Gradient Computation

Calculate derivatives for:

- Weight matrices
- Bias vectors
- Hidden activations

These gradients form the basis for optimization algorithms such as Gradient Descent.

---

# 📂 Project Structure

```
Deep-Neural-Network-From-Scratch-Using-NumPy/

│
├── TP5.ipynb
│
├── README.md
│
└── images/
    └── architecture.png
```

---

# ▶️ Running the Project

Install dependencies:

```bash
pip install numpy matplotlib
```

Launch Jupyter Notebook:

```bash
jupyter notebook TP5.ipynb
```

or open the notebook in **Google Colab**.

---

# ✅ Strengths

- Complete neural network implementation
- Pure NumPy solution
- Educational approach
- Configurable architecture
- Supports binary classification
- Supports multiclass classification
- Manual backpropagation
- No external deep learning framework
- Easy to understand
- Lightweight implementation

---

# ⚠️ Limitations

- No GPU acceleration
- No automatic differentiation
- No optimizer implementation (Adam, SGD, RMSProp)
- Designed primarily for educational purposes
- Not optimized for very large datasets

---

# 🚀 Future Improvements

- Mini-batch Gradient Descent
- SGD Optimizer
- Adam Optimizer
- Dropout Regularization
- Batch Normalization
- Xavier Initialization
- He Initialization
- L2 Regularization
- Early Stopping
- Learning Rate Scheduling
- MNIST digit classification
- CIFAR-10 experiments
- Automatic gradient checking
- Model serialization

---

# 🛠️ Technologies Used

- Python
- NumPy
- Jupyter Notebook
- Linear Algebra
- Matrix Calculus
- Deep Learning Fundamentals

---

# 📚 References

- Michael Nielsen — Neural Networks and Deep Learning
- Ian Goodfellow, Yoshua Bengio & Aaron Courville — Deep Learning
- CS231n: Convolutional Neural Networks for Visual Recognition
- Stanford Machine Learning Course
- NumPy Documentation
- Deep Learning Specialization — Andrew Ng
- Bishop — Pattern Recognition and Machine Learning

---

# 👨‍🎓 Academic Context

This project was completed as part of the **Master's Degree in Image Processing & Artificial Intelligence (MIV)** at **USTHB (University of Science and Technology Houari Boumediene)**.

The objective is to gain a deep understanding of the mathematical foundations and implementation details behind modern deep learning algorithms by building every component of a neural network from first principles.
