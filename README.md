# AdaBoost (Adaptive Boosting)

**AdaBoost** is an **ensemble learning algorithm** that combines multiple **weak learners** (often shallow decision trees) to form a **strong classifier**. It works by **focusing on the mistakes** of previous models and adapting accordingly.

---

## 🔍 Key Intuition Behind AdaBoost

1. **Initialize Weights**  
   - All training samples start with **equal weights**.

2. **Train a Weak Learner**  
   - Fit a weak classifier (e.g., a decision stump) to the weighted data.

3. **Evaluate the Learner**
   - **Misclassified samples**: their weights are **increased**.
   - **Correctly classified samples**: their weights are **decreased**.

4. **Adapt and Repeat**
   - A new classifier is trained, giving more focus to **previously misclassified** samples.
   - Repeat this process for **T iterations** or until a stopping condition is met.

5. **Combine Weak Learners**
   - Each weak learner is given a **weight (alpha)** based on its accuracy.
   - The final prediction is made using **weighted voting** (classification) or **weighted sum** (regression).

---

## 🧠 Why It Works

- Weak learners on their own are only slightly better than random guessing.
- AdaBoost emphasizes harder examples, forcing subsequent learners to correct mistakes.
- The final model is robust and often performs well without overfitting (especially with simple learners).

---

## ✅ Advantages

- Often improves accuracy significantly.
- Simple and interpretable with decision stumps.
- Effective in practice with minimal parameter tuning.

---

## ⚠️ Considerations

- Sensitive to noisy data and outliers.
- Works best with weak but stable learners.
