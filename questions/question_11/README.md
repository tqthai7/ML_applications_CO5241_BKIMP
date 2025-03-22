# 📌 Question 11: Naïve Bayes vs. Non-Naïve Bayesian Classification for Loan Risk

## 🔍 Problem Overview
In this task, we apply **Naïve Bayes classification** to determine the risk level for **T1** and compare it with a **non-naïve Bayesian approach**. The key objectives are:
- Compute **posterior probabilities** for `RiskLevel`
- Compare Naïve Bayes (independent features) vs. non-naïve Bayes (accounting for feature dependencies)

## 🏗️ Methodology
### 1️⃣ Naïve Bayes Classification
Using Bayes' theorem:
<div align="center"> 
  <img src="https://latex.codecogs.com/svg.latex?P(Y%20|%20X)%20=%20\frac{P(X%20|%20Y)%20P(Y)}{P(X)}" alt="Bayes' Theorem">
</div>

Where:
- \( Y \) is `RiskLevel`
- \( X \) is (`Age`, `CreditScore`)
- **Assumption**: Features are conditionally independent

#### **Compute Priors**

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?P(\mathrm{Low\ Risk})%20=%20\frac{\mathrm{Count(Low\ Risk)}}{\mathrm{Total\ Samples}}" alt="Prior Probability Low Risk">
</div>


<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?P(\mathrm{High\ Risk})%20=%20\frac{\mathrm{Count(High\ Risk)}}{\mathrm{Total\ Samples}}" alt="Prior Probability High Risk">
</div>

#### **Compute Likelihoods**
Using Gaussian distribution for numerical features:
<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?P(X_i%20|%20Y)%20=%20\frac{1}{\sqrt{2\pi%20\sigma^2}}%20e^{-\frac{(X_i-\mu)^2}{2\sigma^2}}" alt="Gaussian Likelihood">
</div>

Where \( \mu \) and \( \sigma \) are the mean and standard deviation of each feature per class.

#### **Final Classification**
The predicted class is the one with the highest posterior probability:
<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?\hat{Y}%20=%20\arg\max_Y%20P(Y%20|%20X)" alt="Classification Decision">
</div>

### 2️⃣ Non-Naïve Bayesian Approach
- Considers dependencies between `Age` and `CreditScore`
- Uses **joint probability distribution**
- Computes **conditional dependencies** via covariance

**Multivariate Gaussian Distribution**

Instead of assuming independence, we model XX using a multivariate normal distribution:
<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?P(X%20|%20Y)%20=%20\frac{1}{(2\pi)^{n/2}|\Sigma_Y|^{1/2}}e^{-\frac{1}{2}(X-\mu_Y)^T\Sigma_Y^{-1}(X-\mu_Y)}" alt="Multivariate Gaussian">
</div>

Where:

ΣYΣY​ is the covariance matrix for features given class YY.

The dependency structure is captured in ΣYΣY​.

**Final Classification**

Similar to Naïve Bayes, we choose the class with the highest posterior probability.

## 📊 Expected Outcome
- Compute posterior probabilities using **Naïve Bayes**
- Compare with a **non-naïve Bayesian approach**
- Discuss differences in performance and accuracy
