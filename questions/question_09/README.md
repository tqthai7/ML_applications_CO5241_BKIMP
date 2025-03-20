# 📌 Question 9: Perceptron Classification for T1

## 🔍 Problem Overview
In this task, we design a **perceptron model** to classify test case **T1**. We perform input **normalization**, compute the **prediction**, and explain why normalization is necessary for neural networks.

## 🏗️ Methodology
### 1️⃣ Perceptron Model
A perceptron makes a classification decision using:
\[
\hat{y} = \text{sign}(w \cdot x + b)
\]
where:
- \( w = [0.3, 0.4] \) (weight vector)
- \( x \) (normalized input features for `Age` and `CreditScore`)
- \( b = 0.1 \) (bias)
- **sign function** outputs either `1` (Low Risk) or `-1` (High Risk)

### 2️⃣ Normalize Input Features
Feature normalization ensures numerical stability and faster convergence. We use **min-max scaling**:
\[
x' = \frac{x - x_{min}}{x_{max} - x_{min}}
\]
Given test case **T1**:
- Age = 37, CreditScore = 705
- Normalized values: \([0.375, 0.583]\)

### 3️⃣ Compute Perceptron Output
The perceptron computes:
\[
z = w_1 \cdot x_1 + w_2 \cdot x_2 + b
\]
Applying the sign function determines the classification.

### 4️⃣ Why Normalization is Necessary
- Prevents features with larger magnitudes from dominating
- Improves weight updates during training
- Enhances model stability in multi-layer networks

## 📊 Expected Outcome
- Compute the perceptron prediction for **T1**
- Explain why **normalization** is critical for neural networks