# Stroke Prediction & Market Basket Analysis

This project presents a comprehensive Data Mining solution that combines healthcare stroke prediction and market basket analysis within a single interactive Streamlit application. The system applies machine learning techniques to predict stroke risk using patient clinical data and association rule mining to discover purchasing patterns from transactional grocery data.

## Project Overview

The application consists of two major components:

1. **Stroke Prediction System**
   - Predicts the likelihood of stroke occurrence based on patient health indicators.
   - Compares multiple machine learning algorithms to identify the most effective model for healthcare decision support.

2. **Market Basket Analysis**
   - Identifies frequently purchased product combinations.
   - Generates association rules using Apriori and FP-Growth algorithms.

---

## 🧠 Machine Learning Models

The stroke prediction module performs comparative analysis of the following classifiers:

### Decision Tree
- High interpretability and strong recall performance.
- Selected as the recommended model due to its transparency and effectiveness.

### Support Vector Machine (SVM)
- Uses an RBF kernel to capture non-linear relationships.
- Achieved recall performance comparable to the Decision Tree.

### RIPPER Rule-Based Classifier
- Generates human-readable IF-THEN rules.
- Included for interpretability comparison.

### Gaussian Naive Bayes
- Probabilistic baseline model for classification.
- Provides fast training and prediction.

---

## 🛒 Market Basket Analysis Algorithms

### Apriori
- Generates frequent itemsets and association rules through candidate generation.

### FP-Growth
- Uses FP-Tree structures for efficient frequent pattern mining.

Both algorithms are compared based on:
- Runtime performance
- Frequent itemset generation
- Association rule quality

---

## Key Features

### Healthcare Stroke Prediction
- Missing value imputation
- Label encoding of categorical features
- Feature binning and normalization
- Class imbalance handling using balanced class weights
- Real-time stroke risk prediction
- Model comparison dashboard

### Market Basket Analysis
- Frequent itemset mining
- Association rule generation
- Support, confidence, and lift analysis
- Interactive threshold adjustment
- Apriori vs FP-Growth comparison

### Interactive Streamlit Dashboard
- User-friendly interface
- Real-time predictions
- Dynamic visualizations
- Downloadable analysis outputs

---

## Technical Stack

### Programming Language
- Python

### Machine Learning
- Scikit-learn
- Wittgenstein (RIPPER)

### Association Rule Mining
- Mlxtend

### Data Processing
- Pandas
- NumPy

### Visualization
- Matplotlib
- Seaborn
- Plotly

### Frontend
- Streamlit

---

## How to Run

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Launch Application

```bash
streamlit run app.py
```

---

## Project Structure

```text
├── app.py
├── Stroke_Prediction_MID_PROJECT.ipynb
├── healthcare-dataset-stroke-data.csv
├── groceries.csv
├── requirements.txt
├── Stroke_MBA_Final_Report.docx
└── README.md
```

---

## Dataset Information

### Healthcare Stroke Dataset
- Source: Kaggle
- 5,110 patient records
- Healthcare indicators including age, BMI, glucose level, hypertension, heart disease, smoking status, and more.

### Groceries Dataset
- 9,835 customer transactions
- 169 unique products
- Used for association rule mining and market basket analysis.

---

## Results

### Stroke Prediction
- Decision Tree and SVM achieved the highest recall (0.76)
- Decision Tree selected as the recommended model due to interpretability and strong predictive performance.

### Market Basket Analysis
- Apriori and FP-Growth generated identical frequent itemsets and association rules.
- Strongest rule discovered:

```text
{root vegetables, whole milk} → {other vegetables}
Lift = 2.45
```

---

## Future Improvements

- Implement SMOTE and ADASYN for advanced class imbalance handling.
- Add XGBoost and LightGBM models.
- Integrate ECLAT algorithm for association rule mining.
- Deploy the application online using Streamlit Cloud.
- Incorporate additional healthcare risk factors for improved stroke prediction.

---

