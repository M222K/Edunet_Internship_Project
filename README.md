# 🛡️ Network Intrusion Detection System using Machine Learning

This project implements a Machine Learning-based Network Intrusion Detection System (NIDS) capable of detecting and classifying various types of cyberattacks including DoS, Probe, R2L, and U2R using the KDD Cup 1999 dataset.

---

## 📁 Dataset

**Source:** [Kaggle - Network Intrusion Detection Dataset (KDD'99)](https://www.kaggle.com/datasets/sampadab17/network-intrusion-detection)  
**Classes:** Normal, DoS, Probe, R2L, U2R  
**Features:** 41 network connection attributes

---

## ⚙️ System Requirements

- Python 3.8+
- Jupyter Notebook / VSCode / Any Python IDE
- 8GB RAM (minimum)

---

## 📦 Libraries Used

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `xgboost`
- `joblib`

Install all libraries using:

```bash
pip install -r requirements.txt


## ⚙️ Algorithm Used

- **Model**: XGBoost Classifier  
- **Why**: High accuracy, handles class imbalance well, fast training, and interpretable  
- **Input Features**: Encoded and normalized network connection features  
- **Output**: Attack type classification — `Normal`, `DoS`, `Probe`, `R2L`, `U2R`

---

## 🧠 Model Training & Testing

### 🔄 Preprocessing
- Encode categorical features (`protocol_type`, `service`, `flag`)
- Normalize numerical values
- Handle class imbalance using class weighting or SMOTE

### 🏋️‍♀️ Model Training
- 80% data used for training  
- 20% data used for testing  
- Cross-validation used for reliability

---

## 📊 Evaluation

- **Metrics**: Accuracy, Precision, Recall, F1-Score
- **Tools**: Confusion Matrix for visualizing class-wise performance

### ✅ Results
- **Accuracy**: ~98%  
- **Strengths**: Fast detection and generalization across attack types  
- **Limitation**: Lower recall on rare classes like U2R

---

## ⚠️ Challenges Faced

- Highly imbalanced dataset
- Complex categorical feature encoding
- Long training time on full dataset

---
