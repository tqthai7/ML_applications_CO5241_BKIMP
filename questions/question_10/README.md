# 📌 Question 10: Neural Network Forward & Backpropagation for Loan Risk Classification

## 🔍 Problem Overview
In this task, we perform a **forward pass** for a neural network classifying **T1**, then calculate the **backpropagation gradients** if the prediction is incorrect. The network structure consists of:
- **2 input neurons** (normalized `Age` and `CreditScore`)
- **1 hidden layer** with **2 neurons** (sigmoid activation)
- **1 output neuron** (sigmoid activation for `RiskLevel` classification)

---

## 🏗️ Methodology

### 1️⃣ Forward Pass Computation

#### **Input Layer (Normalized Values for T1)**

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?x%20=%20[0.375,%200.583]" alt="Input Vector">
</div>

#### **Hidden Layer Calculation**

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?Z_1%20=%20W_1%20\cdot%20x%20+%20b_1" alt="Hidden Layer Pre-Activation">
</div>

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?A_1%20=%20\sigma(Z_1)" alt="Hidden Layer Activation">
</div>

Given:
<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?W_1%20=%20\begin{bmatrix}%200.3%20&%200.5%20\\%200.4%20&%20-0.2%20\end{bmatrix}" alt="Hidden Layer Weights">
</div>

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?b_1%20=%20\begin{bmatrix}%200.1%20\\%20-0.1%20\end{bmatrix}" alt="Hidden Layer Bias">
</div>

Apply the **sigmoid activation function**:
<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\sigma(z)%20=%20\frac{1}{1%20+%20e^{-z}}" alt="Sigmoid Function">
</div>

#### **Output Layer Calculation**

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?Z_2%20=%20W_2%20\cdot%20A_1%20+%20b_2" alt="Output Layer Pre-Activation">
</div>

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?A_2%20=%20\sigma(Z_2)" alt="Output Layer Activation">
</div>

Given:
<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?W_2%20=%20[0.6,%20-0.4]" alt="Output Layer Weights">
</div> 

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?b_2%20=%200.2" alt="Output Layer Bias">
</div>

We obtain the final prediction ![A_2](https://latex.codecogs.com/svg.latex?A_2), which represents the probability of **Low Risk (1)**.

---

### 2️⃣ Backpropagation (Error Gradients)
If the target label for T1 is **Low Risk (1)**, we compute:

#### **Error Calculation**
<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?E%20=%20-%20[y%20\log(A_2)%20+%20(1%20-%20y)%20\log(1%20-%20A_2)]" alt="Cross Entropy Loss">
</div>

where ![y = 1](https://latex.codecogs.com/svg.latex?y%20=%201) (Low Risk).

#### **Gradient Calculation for Weights**
Using chain rule:

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\delta_2%20=%20(A_2%20-%20y)" alt="Output Error Signal">
</div>

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\nabla%20W_2%20=%20\delta_2%20\cdot%20A_1" alt="Output Weight Gradient">
</div>

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\delta_1%20=%20\delta_2%20\cdot%20W_2%20\cdot%20\sigma'(Z_1)" alt="Hidden Layer Error Signal">
</div>

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\nabla%20W_1%20=%20\delta_1%20\cdot%20x" alt="Hidden Weight Gradient">
</div>

---

### 3️⃣ Learning Rate Update (Gradient Descent)
<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?W%20=%20W%20-%20\alpha%20\nabla%20W" alt="Gradient Descent Update">
</div>

with ![\alpha = 0.1](https://latex.codecogs.com/svg.latex?\alpha%20=%200.1).

---

## 📊 Expected Outcome
- Perform **forward pass** for `T1`
- Compute **backpropagation gradients** for all weights
- Explain how error propagates backward to adjust weights
