# 📌 Question 16: Nonlinear Decision Boundary with Kernel SVM

## 🔍 Problem Overview
In this task, we use a **Support Vector Machine (SVM) with a Radial Basis Function (RBF) kernel** to classify loan risk based on `Age` and `CreditScore`. The goal is to determine the **nonlinear decision boundary** and compute the kernel matrix for the first three training samples.

## 🏗️ Methodology
### 1️⃣ Why Use an RBF Kernel?
- **Linear SVM** may struggle when data is not linearly separable.
- **Kernel trick** allows us to map input data into a higher-dimensional space without explicitly computing feature transformations.
- **RBF Kernel Formula**:
  \[
  K(x_i, x_j) = \exp\left(-\gamma ||x_i - x_j||^2\right)
  \]
  where \( \gamma \) controls the influence of training samples:
  - **Higher \( \gamma \)** → More complex decision boundary (risk of overfitting).
  - **Lower \( \gamma \)** → Smoother boundary (risk of underfitting).

### 2️⃣ Computing the Kernel Matrix
For three training samples \( x_1, x_2, x_3 \):
\[
K = \begin{bmatrix} K(x_1, x_1) & K(x_1, x_2) & K(x_1, x_3) \\ K(x_2, x_1) & K(x_2, x_2) & K(x_2, x_3) \\ K(x_3, x_1) & K(x_3, x_2) & K(x_3, x_3) \end{bmatrix}
\]
- Compute pairwise Euclidean distances.
- Apply the **RBF kernel function** with \( \gamma = 0.1 \).

### 3️⃣ Interpreting the Kernel Transformation
- **Higher kernel values** indicate strong similarity between points.
- **Transformed feature space** enables SVM to find a nonlinear boundary.
- **Decision boundary** becomes curved rather than linear, adapting to complex data structures.

## 📊 Expected Outcome
- Compute the **kernel matrix** for the first three training samples.
- Train an **RBF kernel SVM** to classify loan risk.
- Visualize the **nonlinear decision boundary**.