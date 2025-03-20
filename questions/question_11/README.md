# 📌 Question 11: Naïve Bayes vs. Non-Naïve Bayesian Classification for Loan Risk

## 🔍 Problem Overview
In this task, we apply **Naïve Bayes classification** to determine the risk level for **T1** and compare it with a **non-naïve Bayesian approach**. The key objectives are:
- Compute **posterior probabilities** for `RiskLevel`
- Compare Naïve Bayes (independent features) vs. non-naïve Bayes (accounting for feature dependencies)

## 🏗️ Methodology
### 1️⃣ Naïve Bayes Classification
Using Bayes' theorem:
\[
P(Y | X) = \frac{P(X | Y) P(Y)}{P(X)}
\]
Where:
- \( Y \) is `RiskLevel`
- \( X \) is (`Age`, `CreditScore`)
- **Assumption**: Features are conditionally independent

#### **Compute Priors**
\[
P(\text{Low Risk}) = \frac{\#(\text{Low Risk})}{\text{Total Samples}}
\]
\[
P(\text{High Risk}) = \frac{\#(\text{High Risk})}{\text{Total Samples}}
\]

#### **Compute Likelihoods**
Using Gaussian distribution for numerical features:
\[
P(X_i | Y) = \frac{1}{\sqrt{2\pi \sigma^2}} e^{- \frac{(X_i - \mu)^2}{2 \sigma^2}}
\]
Where \( \mu \) and \( \sigma \) are the mean and standard deviation of each feature per class.

#### **Final Classification**
The predicted class is the one with the highest posterior probability:
\[
\hat{Y} = \arg\max_Y P(Y | X)
\]

### 2️⃣ Non-Naïve Bayesian Approach
- Considers dependencies between `Age` and `CreditScore`
- Uses **joint probability distribution**
- Computes **conditional dependencies** via covariance

## 📊 Expected Outcome
- Compute posterior probabilities using **Naïve Bayes**
- Compare with a **non-naïve Bayesian approach**
- Discuss differences in performance and accuracy