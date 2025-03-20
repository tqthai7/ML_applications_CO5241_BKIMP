# 📌 Question 18: Distance-Weighted k-NN vs. Standard k-NN for Loan Risk Classification

## 🔍 Problem Overview
In this task, we compare **distance-weighted k-Nearest Neighbors (k-NN)** with **standard k-NN** for classifying loan risk. The goal is to analyze how each method determines the probability of test case `T1` belonging to the `High Risk` or `Low Risk` class when using `k=3`.

## 🏗️ Methodology
### 1️⃣ Standard k-NN Classification
- Identify the **k=3 nearest neighbors** based on **Euclidean distance**.
- Perform **majority voting**:
  - If the majority of neighbors belong to `High Risk`, classify `T1` as `High Risk`.
  - Otherwise, classify it as `Low Risk`.
- **Limitations**:
  - Treats all neighbors equally, regardless of distance.
  - May misclassify if closer points have less influence.

### 2️⃣ Distance-Weighted k-NN
- Instead of simple majority voting, we assign weights to neighbors:
  \[
  w_i = \frac{1}{d_i + \epsilon}
  \]
  where:
  - \( d_i \) is the Euclidean distance of neighbor \( i \) from `T1`.
  - Small constant \( \epsilon \) prevents division by zero.
- Compute **weighted probability** for each class:
  \[
  P(\text{High Risk} | T1) = \frac{\sum w_i \cdot I(y_i = \text{High Risk})}{\sum w_i}
  \]
  \[
  P(\text{Low Risk} | T1) = \frac{\sum w_i \cdot I(y_i = \text{Low Risk})}{\sum w_i}
  \]
  where \( I(y_i) \) is an indicator function.
- **Advantages**:
  - Closer points have more influence on classification.
  - Reduces errors from distant but misrepresentative neighbors.

### 3️⃣ Impact on Classification
- Compare classifications using **standard k-NN** vs. **distance-weighted k-NN**.
- Analyze which method provides **more stable and robust predictions**.

## 📊 Expected Outcome
- Compute and compare `T1`’s **risk classification probabilities** using both methods.
- Explain why **distance-weighted k-NN** is often more reliable.
- Visualize the **decision boundary** for both approaches.