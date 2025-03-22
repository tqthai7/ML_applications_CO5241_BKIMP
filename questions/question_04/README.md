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

![\frac{\partial J}{\partial \theta_0} = -\frac{1}{m} \sum_{i=1}^{m} (y_i - \hat{y}_i)](https://latex.codecogs.com/svg.latex?\frac{\partial%20J}{\partial%20\theta_0}%20=%20-\frac{1}{m}%20\sum_{i=1}^{m}%20(y_i%20-%20\hat{y}_i))

![\frac{\partial J}{\partial \theta_1} = -\frac{1}{m} \sum_{i=1}^{m} (y_i - \hat{y}_i) x_i](https://latex.codecogs.com/svg.latex?\frac{\partial%20J}{\partial%20\theta_1}%20=%20-\frac{1}{m}%20\sum_{i=1}^{m}%20(y_i%20-%20\hat{y}_i)%20x_i)

where ![\hat{y}_i](https://latex.codecogs.com/svg.latex?\hat{y}_i) is the predicted CreditScore.

---

### 2️⃣ Update Parameters
Using **gradient descent**, the parameters are updated as follows:

![\theta_0^{(new)} = \theta_0 - \alpha \frac{\partial J}{\partial \theta_0}](https://latex.codecogs.com/svg.latex?\theta_0^{(new)}%20=%20\theta_0%20-%20\alpha%20\frac{\partial%20J}{\partial%20\theta_0})

![\theta_1^{(new)} = \theta_1 - \alpha \frac{\partial J}{\partial \theta_1}](https://latex.codecogs.com/svg.latex?\theta_1^{(new)}%20=%20\theta_1%20-%20\alpha%20\frac{\partial%20J}{\partial%20\theta_1})

where ![\alpha = 0.01](https://latex.codecogs.com/svg.latex?\alpha%20=%200.01) is the **learning rate**.

---

### 3️⃣ Interpret the Updates
- If the gradient is **positive**, the parameter is **decreased**.
- If the gradient is **negative**, the parameter is **increased**.
- This ensures the model moves toward a **better fit**.

---

## 📊 Expected Outcome
By performing **one iteration** of gradient descent, we update ![\theta_0](https://latex.codecogs.com/svg.latex?\theta_0) and ![\theta_1](https://latex.codecogs.com/svg.latex?\theta_1), improving the model's ability to **predict CreditScore** based on Age.
