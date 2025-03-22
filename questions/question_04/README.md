# 📌 Question 4: Batch Gradient Descent for CreditScore Prediction

## 🔍 Problem Overview
In this task, we implement **batch gradient descent** to optimize the weights for predicting CreditScore using Age. The goal is to perform **one iteration** of gradient descent and interpret how the parameters update.

## 🏗️ Methodology
To find the optimal weights ![\theta_0](https://latex.codecogs.com/svg.latex?\theta_0) and ![\theta_1](https://latex.codecogs.com/svg.latex?\theta_1), we use the **Mean Squared Error (MSE) cost function**:

<div align="center">
    <img src="https://latex.codecogs.com/svg.latex?J(\theta_0,%20\theta_1)%20=%20\frac{1}{2m}%20\sum_{i=1}^{m}%20(y_i%20-%20(\theta_0%20+%20\theta_1%20x_i))^2" alt="MSE">
</div>

where:
- ![y_i](https://latex.codecogs.com/svg.latex?y_i) is the actual **CreditScore**
- ![x_i](https://latex.codecogs.com/svg.latex?x_i) is **Age**
- ![m](https://latex.codecogs.com/svg.latex?m) is the number of training samples
- ![\theta_0, \theta_1](https://latex.codecogs.com/svg.latex?\theta_0,%20\theta_1) are **model parameters**

---

### 1️⃣ Compute Partial Derivatives
The gradients for the cost function are:

<div align="center"> 
    <img src="https://latex.codecogs.com/svg.latex?\frac{\partial%20J}{\partial%20\theta_0}%20=%20-\frac{1}{m}%20\sum_{i=1}^{m}%20(y_i%20-%20\hat{y}_i)" alt="Gradient theta_0"> 
</div> 

<div align="center"> 
    <img src="https://latex.codecogs.com/svg.latex?\frac{\partial%20J}{\partial%20\theta_1}%20=%20-\frac{1}{m}%20\sum_{i=1}^{m}%20(y_i%20-%20\hat{y}_i)%20x_i" alt="Gradient theta_1"> 
</div>

where ![\hat{y}_i](https://latex.codecogs.com/svg.latex?\hat{y}_i) is the predicted CreditScore.

---

### 2️⃣ Update Parameters
Using **gradient descent**, the parameters are updated as follows:

<div align="center"> 
    <img src="https://latex.codecogs.com/svg.latex?\theta_0^{(new)}%20=%20\theta_0%20-%20\alpha%20\frac{\partial%20J}{\partial%20\theta_0}" alt="Theta_0 update"> 
</div> 

<div align="center"> 
    <img src="https://latex.codecogs.com/svg.latex?\theta_1^{(new)}%20=%20\theta_1%20-%20\alpha%20\frac{\partial%20J}{\partial%20\theta_1}" alt="Theta_1 update"> 
</div>

where ![\alpha = 0.01](https://latex.codecogs.com/svg.latex?\alpha%20=%200.01) is the **learning rate**.

---

### 3️⃣ Interpret the Updates
- If the gradient is **positive**, the parameter is **decreased**.
- If the gradient is **negative**, the parameter is **increased**.
- This ensures the model moves toward a **better fit**.
