# COVID-19 Patient Outcome Prediction Using Machine Learning

This project applies machine learning models to predict the outcome (alive or deceased) of COVID-19 patients based on their clinical history, symptoms, and comorbidities. The aim is to assist healthcare resource allocation and early intervention planning using interpretable and accurate models.

## 🚀 Project Overview

- **Problem**: Predict whether a COVID-19 patient will survive based on medical records.
- **Objective**: Improve predictive accuracy through the use of ensemble learning and class balancing techniques.
- **Dataset**: An anonymized, publicly available dataset from the [Mexican Government's COVID-19 Open Data Platform](https://www.gob.mx/salud/documentos/datos-abiertos-152127) with over 1 million patient records.
- **Models**:
  - Logistic Regression
  - Random Forest
  - XGBoost
  - Stacking Ensemble (LR + RF as base models, XGB as meta-classifier)

## 📁 Repository Structure

```
.
├── Data preprocessing.ipynb   # Full preprocessing, modeling and evaluation pipeline
├── Covid Data.csv             # Source dataset (not included in GitHub repo due to size)
├── requirements.txt           # (Optional) Python dependencies list
```

## ⚙️ How to Run This Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/covid-prediction-ml.git
cd covid-prediction-ml
```

### 2. Install Required Libraries

```bash
pip install -r requirements.txt
```

Or manually install the required packages:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost imbalanced-learn
```

### 3. Download the Dataset

The dataset used is **not uploaded** here to avoid storage bloat. You can download it from the Mexican government portal:

- 📥 [Download CSV (~100MB)](https://www.gob.mx/salud/documentos/datos-abiertos-152127)

Save the CSV as `Covid Data.csv` in the root folder.

### 4. Open the Notebook

```bash
jupyter notebook Data\ preprocessing.ipynb
```

And run each cell step by step to reproduce the results.

## 📊 Features and Techniques Used

- PCA for dimensionality reduction
- SMOTE and RandomUnderSampler for class balancing
- Ensemble learning using stacking
- GridSearchCV for hyperparameter optimization
- Performance evaluation using:
  - Accuracy, F1-score, ROC-AUC
  - Confusion Matrix
  - ROC Curves

## 📌 Acknowledgements

This project was supervised by **Dr. Isaac Osei Agyemang**, who provided essential guidance in structuring the workflow, model selection, and writing the dissertation. The visual flowchart of the model pipeline was also created under his direction.

## 🧠 Third-party Code and Tools

The project uses open-source libraries including:

- [scikit-learn](https://scikit-learn.org/)
- [XGBoost](https://xgboost.readthedocs.io/)
- [imbalanced-learn](https://imbalanced-learn.org/)
- [matplotlib](https://matplotlib.org/)
- [seaborn](https://seaborn.pydata.org/)

All code written in this project is original unless otherwise stated in comments or documentation.

## 📌 License

This repository is for academic purposes only. Please cite appropriately if reusing any part of the codebase.
