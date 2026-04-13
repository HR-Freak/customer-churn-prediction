# 📡 Telco Customer Churn Prediction  
### Predictive Modelling for Customer Retention

**Author:** Marisa Oliveira  
**Project Type:** Group Data Analytics / Machine Learning Project  
**Year:** 2026  

---

## 🚀 Interactive App  
👉 [Launch the Streamlit App](https://customer-churn-prediction-isaoli.streamlit.app/)

---

## 📌 Project Overview  
A telecom provider was experiencing a churn rate of **26–27%**, with the highest attrition among **high-value fibre-optic customers**.  

This project builds an **end-to-end churn prediction system** to identify at-risk customers early and enable **proactive retention strategies**.

---

## 🎯 Key Results  

- 📉 Identified **~69% of churn-risk customers** (Recall ≈ 0.69)  
- 🎯 Improved precision from **0.49 → 0.61** (~24% increase)  
- 🔻 Reduced false alerts from **315 → 168** (**−47%**)  
- 📊 Achieved **PR-AUC ≈ 0.652** and **MCC ≈ 0.51**  
- 🌳 Tree-based models slightly outperformed on ranking metrics but lacked interpretability  

---

## 💼 Business Impact  

The model enables a shift from **reactive churn handling → proactive retention strategy**.

**Operational benefits:**
- 🎯 Focus retention efforts on genuinely at-risk customers  
- 💰 Reduce wasted outreach and improve campaign ROI  
- 🔍 Provide interpretable insights for decision-makers  

---

## 🧠 Technical Approach  

### 📊 Data Preparation  

- Cleaned missing values in `TotalCharges` using tenure consistency  
- Handled zero-tenure customers appropriately  
- Removed identifiers to prevent leakage  
- Applied **one-hot encoding** to categorical variables  
- Standardised numerical features  

### ⚖️ Handling Imbalance  

- Dataset: ~73% non-churn vs ~27% churn  
- Applied **SMOTE** on training data only  
- Maintained realistic distribution in test set  

---

## 📈 Modelling Strategy  

### Metrics Used  

- **PR-AUC** → ranking churners correctly  
- **MCC** → balanced performance metric  
- **Precision / Recall / F1** → operational trade-offs  
- **ROC-AUC** → overall ranking ability  

---

## 🤖 Model Comparison  

| Model | Precision | Recall | F1 | MCC | ROC-AUC | PR-AUC |
|------|----------|--------|----|-----|--------|--------|
| Logistic Regression | 0.49 | 0.82 | 0.61 | ~0.40 | ~0.79 | ~0.57 |
| Logistic + SMOTE | 0.61 | 0.69 | 0.65 | 0.51 | 0.80 | 0.652 |
| Random Forest | 0.68 | 0.51 | 0.58 | 0.47 | 0.845 | 0.660 |
| XGBoost | 0.51 | 0.79 | 0.62 | 0.46 | 0.846 | 0.665 |

---

## 🏆 Final Model Selection  

**Logistic Regression with SMOTE**

Chosen because it offers:

- ⚖️ Balanced performance  
- 🔍 Interpretability for business stakeholders  
- 🧩 Simplicity and ease of deployment  

Tree-based models remain strong candidates for future iterations.

---

## 📊 Key Insights  

### 📉 Contract Risk  
Month-to-month customers show significantly higher churn risk.

**Recommendation:**  
Encourage migration to longer contracts via incentives.

---

### 💸 Price Sensitivity  
Churners tend to pay ~£15 more monthly.

**Recommendation:**  
Optimise pricing strategy for high-cost segments.

---

### ⏳ Critical Risk Window  
Highest churn risk occurs within the **first 12 months**.

**Recommendation:**  
Strengthen onboarding and early engagement.

---

## ⚙️ Operational Impact  

| Metric | Baseline | Final Model |
|--------|--------|-------------|
| False Positives | 315 | 168 |
| Precision | 0.49 | 0.61 |
| Recall | 0.82 | 0.69 |
| MCC | ~0.40 | 0.51 |

✔ Reduced **147 false alerts per cycle**  
✔ Maintained strong churn detection  

---

## 📂 Project Structure  

- 📓 Exploratory Data Analysis Notebook  
- 🤖 Modelling & Evaluation Notebook  
- 📊 Dataset (Telco Churn)  
- 📄 Documentation (README)  
- 🌐 Streamlit App  

---

## 🛠️ Tools & Technologies  

- Python  
- Pandas, NumPy  
- Scikit-learn  
- imbalanced-learn (SMOTE)  
- XGBoost  
- Matplotlib, Seaborn  
- Streamlit  
- Jupyter Notebook  
