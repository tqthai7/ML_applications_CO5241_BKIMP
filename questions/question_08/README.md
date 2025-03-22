# 📌 Question 8: Gradient Descent for Logistic Regression

## 🔍 Problem Overview
In this task, we compute the **gradient vector** for one step of gradient descent optimization in logistic regression. We also explore how **regularization** modifies these gradients and why it is necessary for this dataset.

## 🏗️ Methodology

### 1️⃣ Compute Gradient Vector
The gradient for logistic regression is given by:

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?%5Cnabla%20J(%5Ctheta)%20=%20%5Cfrac{1}{m}%20%5Csum_{i=1}^{m}%20(%5Chat{y}_i%20-%20y_i)%20x_i" alt="Gradient">
</div>

where:
- ![\hat{y}_i](https://latex.codecogs.com/svg.latex?\hat{y}_i) is the predicted probability from the sigmoid function
- ![y_i](https://latex.codecogs.com/svg.latex?y_i) is the actual label (`Low = 1`, `High = 0`)
- ![x_i](https://latex.codecogs.com/svg.latex?x_i) represents input features (`Age`, `CreditScore`)
- ![m](https://latex.codecogs.com/svg.latex?m) is the number of training samples

Using the prediction from **Question 7**, we compute the gradient update for one iteration of **gradient descent**:

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\theta_j%20=%20\theta_j%20-%20\alpha%20\nabla%20J(\theta)" alt="Gradient Descent Update">
</div>

where ![\alpha](https://latex.codecogs.com/svg.latex?\alpha) is the learning rate.

### 2️⃣ Effect of Regularization
Regularization modifies the gradient update to prevent overfitting:

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\nabla%20J_{reg}(\theta)%20=%20\frac{1}{m}%20\sum_{i=1}^{m}%20(\hat{y}_i%20-%20y_i)%20x_i%20+%20\lambda%20\theta" alt="Regularized Gradient">
</div>

where ![\lambda](https://latex.codecogs.com/svg.latex?\lambda) is the regularization parameter.

#### 🔹 Why Regularization?
- **Reduces overfitting** by penalizing large weights
- **Improves generalization** when dataset is small
- **L2 regularization (Ridge regression)** is commonly used in logistic regression

## 📊 Expected Outcome
- Compute the **gradient update** for logistic regression
- Explain how **regularization** affects gradient updates and improves model generalization
