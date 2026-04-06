## 🔬 Thesis Trial Work: Explainable Machine Learning for TB Drug Resistance Prediction

This project represents the initial trial implementation of my undergraduate thesis, which focuses on applying explainable machine learning techniques to predict drug resistance in *Mycobacterium tuberculosis* (MTB) and identify potential genetic markers associated with resistance.

### 📊 Objective

The primary goal of this trial was to validate the feasibility of building a machine learning pipeline capable of:

* Predicting drug resistance from genomic mutation data
* Handling real-world biological datasets
* Providing interpretable insights using Explainable AI (XAI)

---

### 🧬 Dataset Used

The trial utilized genomic feature data (`gene_data_19.csv`) and corresponding drug resistance labels (`AllLabels.csv`).

* Each sample represents an MTB isolate
* Features correspond to gene mutations / SNPs
* Labels indicate resistance (0/1) for multiple drugs (e.g., amikacin)

---

### ⚙️ Methodology

#### 1. Data Preprocessing

* Loaded and aligned feature and label datasets using sample IDs
* Removed inconsistent and missing values
* Selected a target drug (`amikacin`) for binary classification
* Handled class imbalance using `scale_pos_weight`

---

#### 2. Machine Learning Models

Multiple models were implemented to evaluate predictive performance:

* Logistic Regression
* Random Forest
* XGBoost (primary model)

To improve performance and generalization:

* **Voting Ensemble** (soft voting)
* **Stacking Ensemble** (meta-learning approach)

---

#### 3. Model Evaluation

Models were evaluated using:

* Accuracy
* Precision, Recall, F1-score
* ROC-AUC Score

These metrics helped assess performance under imbalanced data conditions.

---

### 🧠 Explainable AI (SHAP)

To address the “black-box” nature of machine learning models, SHAP (SHapley Additive exPlanations) was applied:

* Identified key genetic features contributing to resistance
* Visualized feature importance using summary plots
* Compared explanations across models (XGBoost, Random Forest)
* Approximated explanations for ensemble models using Kernel SHAP

This step aligns directly with the thesis goal of discovering **interpretable and biologically meaningful resistance markers**.

---

### 🚀 Key Outcomes

* Successfully built an end-to-end ML pipeline for TB resistance prediction
* Demonstrated that ensemble models improve predictive performance
* Verified that SHAP can highlight important mutations influencing resistance
* Established a strong foundation for scaling to larger datasets (e.g., CRyPTIC)

---

### 🔍 Future Work

* Extend to multi-drug resistance prediction
* Use full-scale WGS datasets (CRyPTIC, GenTB)
* Perform advanced feature engineering for rare mutations
* Integrate clustering for subgroup analysis
* Validate discovered markers with biological evidence

---

### ✅ Conclusion

This trial work confirms the feasibility of combining machine learning and explainable AI to predict drug resistance in tuberculosis. It serves as a foundational step toward developing a robust, interpretable framework for discovering novel resistance-associated mutations.

---
