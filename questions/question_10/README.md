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
![x = [0.375, 0.583]](https://latex.codecogs.com/svg.latex?x%20=%20[0.375,%200.583])

#### **Hidden Layer Calculation**
![Z_1 = W_1 \cdot x + b_1](https://latex.codecogs.com/svg.latex?Z_1%20=%20W_1%20\cdot%20x%20+%20b_1)

![A_1 = \sigma(Z_1)](https://latex.codecogs.com/svg.latex?A_1%20=%20\sigma(Z_1))

Given:
![W_1 = \begin{bmatrix} 0.3 & 0.5 \\ 0.4 & -0.2 \end{bmatrix}](https://latex.codecogs.com/svg.latex?W_1%20=%20\begin{bmatrix}%200.3%20&%200.5%20\\%200.4%20&%20-0.2%20\end{bmatrix})

![b_1 = \begin{bmatrix} 0.1 \\ -0.1 \end{bmatrix}](https://latex.codecogs.com/svg.latex?b_1%20=%20\begin{bmatrix}%200.1%20\\%20-0.1%20\end{bmatrix})

Apply the **sigmoid activation function**:
![\sigma(z) = \frac{1}{1 + e^{-z}}](https://latex.codecogs.com/svg.latex?\sigma(z)%20=%20\frac{1}{1%20+%20e^{-z}})

#### **Output Layer Calculation**
![Z_2 = W_2 \cdot A_1 + b_2](https://latex.codecogs.com/svg.latex?Z_2%20=%20W_2%20\cdot%20A_1%20+%20b_2)

![A_2 = \sigma(Z_2)](https://latex.codecogs.com/svg.latex?A_2%20=%20\sigma(Z_2))

Given:
![W_2 = [0.6, -0.4]](https://latex.codecogs.com/svg.latex?W_2%20=%20[0.6,%20-0.4])

![b_2 = 0.2](https://latex.codecogs.com/svg.latex?b_2%20=%200.2)

We obtain the final prediction ![A_2](https://latex.codecogs.com/svg.latex?A_2), which represents the probability of **Low Risk (1)**.

---

### 2️⃣ Backpropagation (Error Gradients)
If the target label for T1 is **Low Risk (1)**, we compute:

#### **Error Calculation**
![E = - [y \log(A_2) + (1 - y) \log(1 - A_2)]](https://latex.codecogs.com/svg.latex?E%20=%20-%20[y%20\log(A_2)%20+%20(1%20-%20y)%20\log(1%20-%20A_2)])

where ![y = 1](https://latex.codecogs.com/svg.latex?y%20=%201) (Low Risk).

#### **Gradient Calculation for Weights**
Using chain rule:

![\delta_2 = (A_2 - y)](https://latex.codecogs.com/svg.latex?\delta_2%20=%20(A_2%20-%20y))

![\nabla W_2 = \delta_2 \cdot A_1](https://latex.codecogs.com/svg.latex?\nabla%20W_2%20=%20\delta_2%20\cdot%20A_1)

![\delta_1 = \delta_2 \cdot W_2 \cdot \sigma'(Z_1)](https://latex.codecogs.com/svg.latex?\delta_1%20=%20\delta_2%20\cdot%20W_2%20\cdot%20\sigma'(Z_1))

![\nabla W_1 = \delta_1 \cdot x](https://latex.codecogs.com/svg.latex?\nabla%20W_1%20=%20\delta_1%20\cdot%20x)

---

### 3️⃣ Learning Rate Update (Gradient Descent)
![W = W - \alpha \nabla W](https://latex.codecogs.com/svg.latex?W%20=%20W%20-%20\alpha%20\nabla%20W)

with ![\alpha = 0.1](https://latex.codecogs.com/svg.latex?\alpha%20=%200.1).

---

## 📊 Expected Outcome
- Perform **forward pass** for `T1`
- Compute **backpropagation gradients** for all weights
- Explain how error propagates backward to adjust weights
