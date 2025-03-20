# 📌 Question 14: Variance and Entropy Analysis of CreditScore by Risk Level

## 🔍 Problem Overview
In this task, we analyze the **variance** and **entropy** of the `CreditScore` feature for both `Low Risk` and `High Risk` classes. These statistical measures help us understand data distribution and how different machine learning models handle them.

## 🏗️ Methodology
### 1️⃣ Calculating Variance
Variance measures the spread of `CreditScore` values within each risk class:
\[
\sigma^2 = \frac{\sum (x_i - \mu)^2}{N}
\]
Where:
- \( x_i \) is an individual `CreditScore`
- \( \mu \) is the mean of `CreditScore` for the class
- \( N \) is the number of samples in that class

Higher variance suggests that the `CreditScore` feature is more dispersed within a given risk level.

### 2️⃣ Calculating Entropy
Entropy quantifies the uncertainty (disorder) within the class distribution:
\[
H(X) = - \sum P(x) \log_2 P(x)
\]
Where:
- \( P(x) \) is the probability of `CreditScore` belonging to a particular risk class.

Higher entropy means greater uncertainty, making classification more challenging.

### 3️⃣ Interpreting the Results for ML Models
- **Decision Trees**: Prefer features with **low entropy** (high information gain) to make confident splits.
- **Logistic Regression**: Works better with **low variance** features since high variance might indicate multicollinearity.
- **SVM and k-NN**: Can handle high variance if data is well-separated in feature space.
- **Naïve Bayes**: Assumes feature independence, so variance affects conditional probabilities.

## 📊 Expected Outcome
- Compute **variance and entropy** for `CreditScore` by risk level.
- Explain how different ML models utilize this information.
- Provide insights on whether `CreditScore` is a reliable feature for classification.