# 📌 Question 17: k-NN Classification Based on Euclidean Distance

## 🔍 Problem Overview
In this task, we classify **test sample T1** using the **k-Nearest Neighbors (k-NN) algorithm** with normalized `Age` and `CreditScore` features. We calculate Euclidean distances to all training samples and determine T1's classification for **k = 3**.

## 🏗️ Methodology
### 1️⃣ Euclidean Distance Calculation
The Euclidean distance formula between two feature vectors \( x_i \) and \( x_j \) is:
\[
 d(x_i, x_j) = \sqrt{\sum_{k=1}^{n} (x_{ik} - x_{jk})^2}
\]

Steps:
1. **Normalize** the `Age` and `CreditScore` features.
2. Compute the **Euclidean distance** between T1 and all training samples.
3. Select the **3 nearest neighbors** (smallest distances).

### 2️⃣ k-NN Classification Rule
- Assign T1 to the majority class among its 3 nearest neighbors.
- If a tie occurs, use distance-weighted voting (optional for robustness).

### 3️⃣ Effect of Different k Values
- **Small k (e.g., 1, 3)** → More sensitive to noise, risk of overfitting.
- **Large k (e.g., 10, 15)** → Smoother decision boundary, but may underfit.
- **Odd k** helps avoid ties.

## 📊 Expected Outcome
- Compute **Euclidean distances** between T1 and training samples.
- Classify T1 using **k = 3** nearest neighbors.
- Analyze how k influences classification.