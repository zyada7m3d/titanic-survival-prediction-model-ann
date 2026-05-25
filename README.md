# Titanic Survival Prediction – Data Analysis & Machine Learning Report

## Project Overview

### Objective
The project aims to predict passenger survival outcomes on the Titanic dataset using data analysis and an Artificial Neural Network (ANN) classification model.

### Business / Problem Context
The Titanic dataset is a classical binary classification problem used to evaluate predictive analytics workflows. The objective is to identify passenger characteristics that influenced survival probability and build a predictive model.

### Expected Outcomes
- Identify survival patterns and key drivers.
- Develop a predictive model with optimized features.
- Generate actionable insights suitable for portfolio and academic presentation use.

---

## Dataset Description

### Dataset Source
- Source: Kaggle Titanic Survival Prediction Dataset
- Files Used:
  - `train.csv`
  - `test.csv`
  - `gender_submission.csv`

### Dataset Size
- Training records: **891 passengers**
- Features: **12 columns**
- Target Variable: **Survived**

### Main Features
| Feature | Type | Description |
|----------|------|-------------|
| Pclass | Categorical | Passenger class |
| Sex | Categorical | Gender |
| Age | Numerical | Passenger age |
| Fare | Numerical | Ticket fare |
| Embarked | Categorical | Port of embarkation |
| SibSp / Parch | Numerical | Family relations onboard |

### Data Cleaning & Preprocessing
Performed preprocessing steps included:

- Missing values handling:
  - `Age` → Median imputation
  - `Embarked` → Mode imputation
- Removed low-value features:
  - `Ticket`
  - `Cabin`
- Duplicate validation performed
- Feature engineering:
  - Extracted passenger **Title**
  - Created `Family_Count`
  - Generated `IsAlone`
- Applied one-hot encoding for categorical variables.

---

## Key Insights and Findings

### Survival Patterns
- Female passengers had significantly higher survival rates.
- First-class passengers showed better survival probability.
- Younger passengers demonstrated improved survival likelihood.
- Family composition influenced outcomes.

### Correlations & Trends
Key positive indicators:
- Female gender
- Higher ticket class
- Family presence

Negative indicators:
- Traveling alone
- Lower passenger class

### Business Implications
- Feature engineering substantially improves prediction quality.
- Demographic variables strongly affect classification performance.
- Behavioral segmentation provides better predictive insights.

**Suggested Visualizations**
- Survival by gender (bar chart)
- Survival by passenger class
- Correlation heatmap
- Age distribution histogram

---

## Modeling Approach and Results

### Model Used
**Artificial Neural Network (ANN)**

### Workflow
1. Data preprocessing
2. Feature engineering
3. Train-test split (80/20)
4. Model training
5. Performance evaluation

### Feature Selection
Final features included:
- Passenger class
- Gender
- Age
- Fare
- Embarkation port
- Title category
- Family-based engineered variables

### Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score

### Results Summary
The ANN model demonstrated strong classification capability and effectively captured nonlinear relationships between passenger attributes and survival outcomes.

Model strengths:
- Handles feature interactions
- Learns complex patterns
- Improved predictive performance through engineered features

---

## Final Conclusions

### Overall Findings
The analysis confirmed that demographic and socioeconomic variables strongly influenced survival outcomes.

Key drivers:
- Gender
- Passenger class
- Family structure
- Age

### Recommendations
- Expand feature engineering techniques.
- Compare ANN with Random Forest, XGBoost, and Logistic Regression.
- Perform hyperparameter optimization.

### Limitations
- Small dataset size
- Missing historical context
- Limited external variables

### Future Improvements
- Ensemble learning
- Cross-validation optimization
- Explainability techniques (SHAP / feature importance)

---

**Project Type:** Data Analysis + Machine Learning Portfolio Project  
**Domain:** Predictive Analytics / Classification  
**Tools:** Python, Pandas, Scikit-learn, Matplotlib, Seaborn, ANN
