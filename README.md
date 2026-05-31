# Lung Cancer Risk Prediction

**Data Science Capstone — Merrimack College, 2024**

Binary classification project predicting lung cancer presence from 16 patient-reported 
risk factors and symptoms. Built end-to-end in both Python and R.

## The problem

Lung cancer has low early-detection rates, and many diagnostic markers overlap with 
common conditions. This project explores whether a set of 16 behavioral, symptomatic, 
and demographic features can reliably predict lung cancer status — and which features 
carry the most predictive weight.

## Dataset

309 patient records with 16 features:

| Feature | Description |
|---|---|
| GENDER | Patient gender (M/F) |
| AGE | Patient age |
| SMOKING | Current smoker |
| YELLOW_FINGERS | Yellowing of fingers |
| ANXIETY | Anxiety diagnosis |
| PEER_PRESSURE | Peer influence on smoking behavior |
| CHRONIC_DISEASE | Any chronic disease diagnosis |
| FATIGUE | Fatigue as a reported symptom |
| ALLERGY | Allergy history |
| WHEEZING | Wheezing symptom |
| ALCOHOL_CONSUMING | Regular alcohol consumption |
| COUGHING | Persistent cough |
| SHORTNESS_OF_BREATH | Shortness of breath |
| SWALLOWING_DIFFICULTY | Difficulty swallowing |
| CHEST_PAIN | Chest pain |
| LUNG_CANCER | Target variable (YES/NO) |

Binary features are encoded as 1/0. Target class distribution is imbalanced toward 
positive cases.

## Methods

**Feature engineering**
- Age binning into clinically meaningful ranges (`Age_Binning.ipynb`)
- Binary encoding of categorical variables

**Dimensionality reduction**
- PCA in Python (`CapstonePCA.ipynb`) to identify correlated feature groups
- PCA in R (`LungCancer_RFile.Rmd`) with scree plot, eigenvalue analysis, 
  and correlation heatmap via `factoextra` and `corrplot`

**Modeling**
- Logistic Regression, Decision Tree, Random Forest, K-Nearest Neighbors, 
  and Naive Bayes classifiers
- Train/test split with stratification
- Accuracy, precision, recall, F1, and ROC-AUC evaluation
- Feature importance analysis to identify top predictors

(`Lung Cancer Analysis and Prediction Final Code Complete.ipynb`)

## Key findings

- Wheezing, coughing, and shortness of breath were the strongest individual predictors
- PCA revealed high correlation between symptom clusters (respiratory, behavioral)
- Random Forest achieved the highest overall accuracy and F1 on the test set
- Age alone was a weak predictor; age combined with smoking behavior was stronger

## Stack

- Python: `pandas`, `scikit-learn`, `matplotlib`, `seaborn`
- R: `factoextra`, `corrplot`, R Markdown

## Author

**Zach Laher**  
B.S. Data Science, Merrimack College, 2025  
[linkedin.com/in/zachlaher](https://linkedin.com/in/zachlaher) · [zachlaher](https://github.com/zachlaher)
