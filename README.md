# 🩺 Logistic Regression on Cancer Dataset

## 📌 Project Overview
This project applies **Logistic Regression** to the [Breast Cancer Dataset](https://www.kaggle.com/datasets/erdemtaha/cancer-data).  
The main purpose is to classify cancer cases as **Malignant (1)** or **Benign (0)** and analyze how **feature selection** improves the model's performance.

---

## 🛠️ Tools & Libraries
- 🐍 Python  
- 📊 Numpy, Pandas, Matplotlib, Seaborn  
- 📂 Kagglehub, OS  
- 🤖 Scikit-learn (Logistic Regression, Train-Test Split, Confusion Matrix, Classification Report, SelectKBest)  

---

## 📂 Dataset
- **Link:** [Cancer Dataset](https://www.kaggle.com/datasets/erdemtaha/cancer-data)  
- **Shape:** `(569, 33)`  
- **Target Column:** Diagnosis (mapped to `1 = Malignant`, `0 = Benign`)  
- **Cleaning Steps:**  
  - Dropped unrelated columns (`id`, `Unnamed`)  
  - Checked for **null values → None found**  
  - Checked for **duplicates → None found**  

---

## 🔍 Steps Performed

### 1️⃣ Data Preparation
- Loaded dataset, cleaned unnecessary columns  
- Mapped target labels to binary (`1`, `0`)  
- Split data into **X (features)** and **y (target)**  

---

### 2️⃣ Train-Test Split
- **80:20 split**  
- Logistic Regression model trained on training data  

---

### 3️⃣ Model Performance
- ✅ **Accuracy:** `0.91`  
- 📊 **Confusion Matrix:**  
  *<img width="640" height="547" alt="p17-1" src="https://github.com/user-attachments/assets/5105e07b-63fe-42ba-82bd-4c196c52c660" />
*  
- 📝 **Classification Report:**  
- Precision: `0.93`  
- Recall: `0.93`  

---

### 4️⃣ Feature Selection
- Created a copy of dataset  
- Used **SelectKBest** to remove least important features  
- Dropped low-score columns  

---

### 5️⃣ Retraining with Selected Features
- Re-split into training and testing sets  
- Fitted Logistic Regression again  
- ✅ **Accuracy Improved:** `0.92`  
- 📊 **Confusion Matrix:** (Shows **1 less False Negative**)  
  <img width="640" height="547" alt="p17-2" src="https://github.com/user-attachments/assets/610ebd5a-e89a-45e8-80b4-035a78a06911" />


---

## 📈 Results & Insights
- Initial model performed **well (91% accuracy)**  
- After **feature selection**, accuracy improved slightly to **92%**  
- More importantly, the confusion matrix showed a **reduction in False Negatives**, which is critical in medical diagnosis  

---

## 🎯 Conclusion
- Logistic Regression is effective for binary classification in cancer diagnosis  
- **Feature selection enhances performance** by removing irrelevant attributes  
- Key takeaway: Even small improvements in **recall** or reducing **false negatives** can be **life-saving in medical applications**  

---

## 📸 Visuals
- 🔹 Confusion Matrix (Before Feature Selection)  
- 🔹 Confusion Matrix (After Feature Selection)  

---

✨ *This project demonstrates the importance of feature selection in improving machine learning models, especially for healthcare datasets.*  
