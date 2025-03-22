# 📌 Question 9: Perceptron Classification for T1

## 🔍 Problem Overview
In this task, we design a **perceptron model** to classify test case **T1**. We perform input **normalization**, compute the **prediction**, and explain why normalization is necessary for neural networks.

## 🏗️ Methodology

### 1️⃣ Perceptron Model
A perceptron makes a classification decision using:

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\hat{y}%20=%20\text{sign}(w%20\cdot%20x%20+%20b)" alt="Perceptron Equation">
</div>

where:
- ![w = [0.3, 0.4]](https://latex.codecogs.com/svg.latex?w%20=%20[0.3,%200.4]) (weight vector)
- ![x](https://latex.codecogs.com/svg.latex?x) (normalized input features for `Age` and `CreditScore`)
- ![b = 0.1](https://latex.codecogs.com/svg.latex?b%20=%200.1) (bias)
- **Sign function** outputs either `1` (Low Risk) or `-1` (High Risk)

### 2️⃣ Normalize Input Features
Feature normalization ensures numerical stability and faster convergence. We use **min-max scaling**:

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?x'%20=%20\frac{x%20-%20x_{min}}{x_{max}%20-%20x_{min}}" alt="Min-Max Normalization">
</div>

Given test case **T1**:
- Age = 37, CreditScore = 705
- Normalized values: ![[0.375, 0.583]](https://latex.codecogs.com/svg.latex?[0.375,%200.583])

### 3️⃣ Compute Perceptron Output
The perceptron computes:

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?z%20=%20w_1%20\cdot%20x_1%20+%20w_2%20\cdot%20x_2%20+%20b" alt="Perceptron Output">
</div>

Applying the **sign function** determines the classification.

### 4️⃣ Why Normalization is Necessary
- Prevents features with larger magnitudes from dominating
- Improves weight updates during training
- Enhances model stability in multi-layer networks

## 📊 Expected Outcome
- Compute the **perceptron prediction** for **T1**
- Explain why **normalization** is critical for neural networks
