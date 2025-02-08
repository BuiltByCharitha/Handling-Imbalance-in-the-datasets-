# Handling-Imbalance-in-the-datasets-
Credit Card Fraud Detection and Human Activity Recognition


## 📌 Project Overview
This project consists of two major tasks:
1. **💳 Credit Card Fraud Detection** - Detect fraudulent transactions using machine learning.
2. **🏃 Human Activity Recognition** - Classify human activities based on sensor data using ML models.

---

## 🏦 Task 1: Credit Card Fraud Detection

### 🔍 Methodology
- **📊 Data Preprocessing:**
  - Scaled features using `StandardScaler`.
  - Split dataset into training & testing sets.
- **🛠️ Feature Engineering:**
  - **Geographical Features:** Flagged transactions outside the US.
  - **Transaction Category:** Marked suspicious categories.
  - **Time-Based Features:** Extracted date & time components.
  - **Profile & Merchant Encoding:** Encoded transactions & computed merchant frequencies.
  - **Feature Selection:** Removed irrelevant features.
- **🧠 Model Selection & Training:**
  - Used **Random Forest** classifier.
  - Hyperparameters tuned via **Grid Search** (F1-score optimization).
- **📈 Evaluation & Testing:**
  - Used **Accuracy, F1-score, and classification reports**.
  - Cross-validation ensured robustness.
  - Feature importance analysis performed.

### 🏆 Results
✅ **Accuracy:** 90%+  
✅ **Fraud Class Recall:** 89%  
✅ **Precision:** 99.99%  

### 🔎 Observations
- Class weight balancing **worsened** precision & recall.
- Fraud detection needs **high recall** to catch fraud cases.

---

## 🚶 Task 2: Human Activity Recognition

### 🔍 Methodology
- **📊 Data Preprocessing:**
  - Handled missing values.
  - Label-encoded target column.
  - Normalized features using `StandardScaler`.
- **🧠 Model Selection & Training:**
  - Trained **SVM** and **XGBoost** models.
  - Used **Soft Voting Classifier** to combine models.
  - Applied **class weighting** for handling imbalance.
- **📈 Evaluation & Testing:**
  - Used **Accuracy, Precision, Recall, and F1-score**.
  - Analyzed confusion matrices.
  - Saved best-performing model as a **pipeline**.

### 🏆 Results
✅ **Macro F1-score:** 0.74  
✅ **Test Accuracy:** 83.52%  

### 🔎 Observations
- **SMOTE (oversampling) worsened performance**, so it was removed.
- **Class weights improved accuracy** significantly.
- **Soft Voting improved F1-score** from **0.7019 → 0.7455**.

---

## ⚠️ Challenges Faced
### 🏦 Task 1: Fraud Detection
- Some engineered features (e.g., **customer-merchant distance**) had **low impact**.
- Ensuring **consistent preprocessing** for training & test data.

### 🚶 Task 2: Activity Recognition
- **Class imbalance:**
  - **SMOTE did not work**; class weights were a better alternative.
- **Model Deployment Issues:**
  - Initially, **encoders & scalers weren’t saved**, causing errors.
  - The final pipeline includes **scaler + voting classifier**.

---

## 🏁 Conclusion
✅ **Feature Engineering Matters**: New features improved fraud detection.
✅ **Model Experimentation is Key**: Tried multiple models before selecting the best.
✅ **Handling Class Imbalance**: **Class weighting** was better than oversampling.
✅ **Deployment Ready**: Final models are **saved using `joblib`** for easy testing.

---

