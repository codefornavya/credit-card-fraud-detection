# credit-card-fraud-detection
This machine learning project aims to detect fraudulent credit card transactions using a classification model trained on real transaction data.  🎯 Objective: To accurately classify whether a given credit card transaction is fraudulent or genuine, despite the heavy class imbalance (frauds are rare)
Here’s a **complete `README.md`** file for your Credit Card Fraud Detection project, suitable for GitHub or project documentation:

---

````markdown
# 💳 Credit Card Fraud Detection using Machine Learning

This project applies machine learning techniques to detect fraudulent credit card transactions. Using real-world anonymized data, the model is trained to distinguish between genuine and fraudulent transactions, despite significant class imbalance.

## 📁 Dataset

- Source: [Kaggle – Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- Transactions: 284,807
- Fraudulent: 492 (~0.17%)
- Features:
  - `Time`, `Amount`: Original features
  - `V1` to `V28`: PCA-transformed features to preserve confidentiality
  - `Class`: Target variable (0 = Genuine, 1 = Fraudulent)

---

## 📊 Project Workflow

### 1. Data Preprocessing
- Normalized `Amount` and `Time` features using `StandardScaler`.
- Split data into training and testing sets using **stratified sampling** to maintain class distribution.

### 2. Handling Class Imbalance
- Used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the training dataset.
- Ensured oversampling was applied only to training data to avoid data leakage.

### 3. Model Training
Two models were trained and compared:
- ✅ **Logistic Regression**
- 🌲 **Random Forest Classifier**

### 4. Model Evaluation
- Metrics used:
  - **Precision**
  - **Recall**
  - **F1-Score**
  - **Confusion Matrix**
  - **ROC-AUC Curve**
- Plotted confusion matrices and ROC curves for both classifiers.

---

## 📦 Installation & Usage

### Requirements

Install required libraries via pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
````

### Run the Notebook

```bash
jupyter notebook credit_card_fraud_detection.ipynb
```

Make sure the `creditcard.csv` file is in the same directory or adjust the path accordingly.

---

## 📈 Results Summary

| Model               | Precision | Recall | F1-Score | ROC-AUC |
| ------------------- | --------- | ------ | -------- | ------- |
| Logistic Regression | High      | High   | Good     | \~0.97  |
| Random Forest       | Higher    | Higher | Better   | \~0.99  |

> 📌 Random Forest outperformed Logistic Regression in all key metrics, particularly in detecting rare fraud cases.

---

## 🔐 Why This Matters

Detecting fraud in credit card transactions is a crucial challenge in the financial sector. The rarity of fraud cases makes this a classic imbalanced classification problem, requiring careful preprocessing and evaluation.

This project showcases:

* The use of **imbalanced-learn** techniques
* Practical model training and evaluation
* Visualization of model performance

---

## 📌 Future Work

* Implement other models: XGBoost, LightGBM
* Deploy the model via Flask or FastAPI
* Automate model tuning with GridSearchCV
* Real-time prediction dashboard with Streamlit

---

## 🧑‍💻 Author

**Your Name**
GitHub: [@codefornavya](https://github.com/codefornavya)

---

## 📄 License

This project is licensed under the MIT License.

```

---


