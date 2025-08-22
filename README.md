# MSCS_634_ProjectDeliverable_4

## Project Overview
This project focuses on predicting the presence of heart disease using the **Heart Disease UCI dataset**. The project explores multiple stages of the data mining process, including data preprocessing, exploratory data analysis (EDA), feature engineering, regression, classification, clustering, and association rule mining. The goal is to provide actionable insights for early detection and preventive healthcare strategies.

## Dataset Summary

- **Dataset Name:** Heart Disease UCI  
- **Source:** [Kaggle](https://www.kaggle.com/datasets/ineubytes/heart-disease-dataset)  
- **Records:** 1026  
- **Attributes:** 14 (including target)  
- **Objective:** Predict the presence (1) or absence (0) of heart disease based on patient health metrics.  

**Features:**  
Age, Sex, Chest Pain Type (`cp`), Resting Blood Pressure (`trestbps`), Cholesterol (`chol`), Fasting Blood Sugar (`fbs`), Resting ECG (`restecg`), Maximum Heart Rate (`thalach`), Exercise-Induced Angina (`exang`), ST Depression (`oldpeak`), Slope of ST Segment (`slope`), Number of Major Vessels (`ca`), Thalassemia (`thal`)  

**Target Variable:**  
`target` — 1 = presence of heart disease, 0 = absence of heart disease

## Project Steps

### 1. Data Preprocessing
- Checked for missing values and duplicates; cleaned dataset accordingly.  
- Verified feature ranges and identified potential outliers.  
- Encoded categorical variables for modeling.  
- Scaled numeric features for algorithms sensitive to feature magnitude (e.g., KNN, SVM, K-Means).

### 2. Exploratory Data Analysis (EDA)
- Analyzed class balance (~54% positive cases).  
- Identified strongly correlated features such as `cp`, `thalach`, and `oldpeak`.  
- Visualizations: Count plots, correlation heatmaps, pairplots.

### 3. Feature Engineering
- Derived new features such as `chol_high` and `bp_high` for association rule mining.  
- Converted categorical features to numeric for modeling.  

### 4. Regression Analysis
- **Models:** Linear Regression, Ridge Regression (α=1.0), Lasso Regression (α=0.1)  
- **Evaluation:** RMSE, R², predicted vs actual plots  
- Ridge Regression performed best, balancing bias and variance.

### 5. Classification Analysis
- **Models:** Logistic Regression, KNN, Decision Tree, Random Forest, SVM, Naive Bayes  
- **Evaluation Metrics:** Accuracy, F1-Score, ROC-AUC, Confusion Matrix  
- Random Forest and Decision Tree showed high accuracy and reliable predictions.  

### 6. Clustering Analysis
- **Algorithm:** K-Means (`n_clusters=2`)  
- **Evaluation Metric:** Silhouette Score  
- Patient clusters aligned partially with disease presence, useful for segmentation.  

### 7. Association Rule Mining
- **Algorithm:** Apriori  
- Discretized features such as high cholesterol and high blood pressure.  
- Strong rules found linking these risk factors with heart disease presence.  


## Practical Recommendations
- Use Random Forest or Decision Tree classifiers for early detection in clinical settings.  
- Monitor key features (`cp`, `thalach`, `oldpeak`, `chol`) for risk assessment.  
- Apply clustering to segment patients for personalized interventions.  
- Leverage association rules for preventive healthcare strategies.  
- Retrain models periodically with new patient data for improved performance.

## Ethical Considerations
- Ensured **data privacy** by using publicly available anonymized dataset.  
- Addressed **fairness and bias** by evaluating class balance and feature selection.  
- Recommendations are **clinical-supportive**, not diagnostic; human oversight is required.  


## Visualizations
- **Confusion Matrices** for all classifiers  
- **Cluster Scatter Plots** (`age` vs `thalach`)  
- **Top Association Rules** table  

## Author
Pawan Pandey  
Advanced Big Data and Data Mining (MSCS-634-B01)  
University of the Cumberlands 