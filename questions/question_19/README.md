# 📌 Question 19: Hidden Markov Model (HMM) for Credit Risk Progression

## 🔍 Problem Overview
In this task, we construct a **Hidden Markov Model (HMM)** to model the evolution of **credit risk levels** over time. We apply the **Viterbi algorithm** to determine the most likely sequence of hidden states given observed credit scores `[710, 650, 680]` and predefined transition probabilities.

## 🏗️ Methodology
### 1️⃣ Defining the HMM
- **Hidden States:** `{Low, Medium, High}` representing risk levels.
- **Observations:** Credit scores (continuous values, discretized if necessary).
- **Transition Probabilities:**
  \[
  \begin{aligned}
  P(Low \to Low) &= 0.7, \quad P(Low \to Medium) = 0.3 \\
  P(Medium \to Medium) &= 0.6, \quad P(Medium \to High) = 0.4 \\
  P(High \to High) &= 0.8, \quad P(High \to Medium) = 0.2
  \end{aligned}
  \]
- **Emission Probabilities:** Determined by a Gaussian distribution model for credit scores.

### 2️⃣ Applying the Viterbi Algorithm
- The **Viterbi algorithm** finds the most probable sequence of hidden states.
- **Dynamic programming approach**:
  1. **Initialization**: Compute probabilities for the first observation.
  2. **Recursion**: Update probabilities for each step based on previous states and transition probabilities.
  3. **Backtracking**: Trace back the most probable sequence.

### 3️⃣ Interpretation
- **Output**: The sequence of risk levels corresponding to `[710, 650, 680]`.
- **Business Insight**: Helps in predicting future credit risk levels based on historical credit scores.

## 📊 Expected Outcome
- Compute the **most likely sequence of credit risk levels**.
- Visualize the **state transitions over time**.
- Explain how HMM can improve **credit risk assessment** in financial decision-making.