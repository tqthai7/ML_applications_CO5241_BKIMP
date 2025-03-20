# 📌 Question 10: Neural Network Forward & Backpropagation for Loan Risk Classification

## 🔍 Problem Overview
In this task, we perform a **forward pass** for a neural network classifying **T1**, then calculate the **backpropagation gradients** if the prediction is incorrect. The network structure consists of:
- **2 input neurons** (normalized `Age` and `CreditScore`)
- **1 hidden layer** with **2 neurons** (sigmoid activation)
- **1 output neuron** (sigmoid activation for `RiskLevel` classification)

## 🏗️ Methodology
### 1️⃣ Forward Pass Computation
#### **Input Layer (Normalized Values for T1)**
\[ x = [0.375, 0.583] \]

#### **Hidden Layer Calculation**
\[
Z_1 = W_1 \cdot x + b_1
\]
\[
A_1 = \sigma(Z_1)
\]
Given:
\[
W_1 = \begin{bmatrix} 0.3 & 0.5 \\ 0.4 & -0.2 \end{bmatrix}, \quad b_1 = \begin{bmatrix} 0.1 \\ -0.1 \end{bmatrix}
\]
Apply the **sigmoid activation function**:
\[
\sigma(z) = \frac{1}{1 + e^{-z}}
\]

#### **Output Layer Calculation**
\[
Z_2 = W_2 \cdot A_1 + b_2
\]
\[
A_2 = \sigma(Z_2)
\]
Given:
\[
W_2 = [0.6, -0.4], \quad b_2 = 0.2
\]
We obtain the final prediction \( A_2 \), which represents the probability of **Low Risk (1)**.

### 2️⃣ Backpropagation (Error Gradients)
If the target label for T1 is **Low Risk (1)**, we compute:

#### **Error Calculation**
\[
E = - [y \log(A_2) + (1 - y) \log(1 - A_2)]
\]
where \( y = 1 \) (Low Risk).

#### **Gradient Calculation for Weights**
Using chain rule:
\[
\delta_2 = (A_2 - y)
\]
\[
\nabla W_2 = \delta_2 \cdot A_1
\]
\[
\delta_1 = \delta_2 \cdot W_2 \cdot \sigma'(Z_1)
\]
\[
\nabla W_1 = \delta_1 \cdot x
\]

### 3️⃣ Learning Rate Update (Gradient Descent)
\[
W = W - \alpha \nabla W
\]
with \( \alpha = 0.1 \).

## 📊 Expected Outcome
- Perform **forward pass** for `T1`
- Compute **backpropagation gradients** for all weights
- Explain how error propagates backward to adjust weights