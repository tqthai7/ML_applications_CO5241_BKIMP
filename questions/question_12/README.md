# 📌 Question 12: Identifying and Reducing Bias in Loan Risk Data

## 🔍 Problem Overview
In this task, we analyze potential sources of **bias** in the training dataset and propose methods to mitigate them. Bias in data can lead to unfair or inaccurate loan risk predictions, affecting decision-making processes.

## 🏗️ Methodology
### 1️⃣ Identifying Bias in the Dataset
We analyze the feature distributions and class imbalances:
- **Feature Distribution Analysis**: Check if certain values (e.g., `CreditScore`, `Age`) are disproportionately associated with `RiskLevel`.
- **Missing Data Bias**: Identify if missing values are biased toward a particular class.
- **Class Imbalance**: If `Low Risk` or `High Risk` cases dominate, it may skew predictions.

#### **Bias Detection Methods**
- **Statistical Tests**: Use chi-square or t-tests to check feature-class correlations.
- **Visualization**: Histograms, box plots to detect skewed distributions.

### 2️⃣ Methods to Reduce Bias
#### **1. Data Rebalancing**
- **Oversampling** minority class (e.g., `SMOTE`)
- **Undersampling** majority class

#### **2. Feature Engineering**
- Normalize numerical features to remove scale bias.
- Introduce domain knowledge-based synthetic features.

#### **3. Handling Missing Data**
- Use **imputation techniques** (mean/mode imputation or predictive modeling).
- Apply a **dedicated missingness indicator** feature.

#### **4. Regularization in Models**
- Penalize models that rely too much on biased features.
- Use **fairness-aware algorithms** to balance predictions.

## 📊 Expected Outcome
- Detect and quantify biases in the dataset.
- Propose and implement strategies to mitigate bias.
- Improve model fairness and reliability.