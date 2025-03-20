# 📌 Question 20: Forward Algorithm for Credit Risk Prediction Using HMM

## 🔍 Problem Overview
In this task, we extend the **Hidden Markov Model (HMM)** from **Question 19** to compute the probability of observing the sequence `[705, 645]` using the **Forward Algorithm**. This method helps in predicting **future credit behavior** based on historical data.

## 🏗️ Methodology
### 1️⃣ Defining the HMM (Revisited)
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
- **Emission Probabilities:** Assumed to follow a Gaussian distribution for each state.

### 2️⃣ Forward Algorithm for Observation Probability
The **Forward Algorithm** computes the probability of observing the sequence `[705, 645]` by iteratively summing over all possible paths:

1. **Initialization:** Compute initial probabilities for state distribution given the first observation.
2. **Recursion:** Update probabilities for each step using:
   \[
   \alpha_t(s) = \sum_{s'} \alpha_{t-1}(s') P(s' \to s) P(O_t | s)
   \]
3. **Termination:** Sum probabilities across all states at the final time step.

### 3️⃣ Interpretation
- **Output:** Probability of the sequence `[705, 645]` occurring given the model.
- **Business Insight:** Helps financial institutions in assessing creditworthiness trends over time.

## 📊 Expected Outcome
- Compute **observation probability** using the Forward Algorithm.
- Compare results with **Viterbi Algorithm** (from Question 19).
- Explain how HMM can be used for **long-term credit risk forecasting**.