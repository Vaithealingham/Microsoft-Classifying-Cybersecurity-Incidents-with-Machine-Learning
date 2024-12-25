# **Microsoft Cybersecurity Incident Classification**

This project focuses on building a machine learning model to classify cybersecurity incidents into three categories:
  - ***True Positive (TP):*** Verified security threats.
  - ***False Positive (FP):*** False alarms or benign events.
  - ***Benign Positive (BP):*** Non-threatening but notable activities.

The primary goal is to improve the enterprise security posture by reducing false positives and ensuring true threats are addressed promptly.

**Datasets**
---

The project leverages a large dataset of cybersecurity logs with the following key characteristics:
  - ***Training Data Set:*** Contains feature columns and the target variable for training the model.
  - ***Test Data Set:*** Contains feature columns and the target variable for testing the model.

**Key features include:**
  - ***Categorical:*** MitreTechniques, ActionGrouped, ThreatFamily, SuspicionLevel, etc.
  - ***Numerical:*** AlertCount, Severity, etc.

***Target Variable:***
  - True Positive
  - False Positive
  - Benign Positive

**Libraries Used**
---

Core libraries for data processing, visualization, and modeling:
  - ***Data Manipulation:*** pandas, numpy
  - ***Visualization:*** matplotlib, seaborn, plotly
  - ***Modeling and Evaluation:*** scikit-learn, xgboost
  - ***Imbalanced Data Handling:*** imbalanced-learn (SMOTE, RUS)


**Data Cleaning**
---

***Null Handling:***
  - Columns with >90% null values (e.g., ActionGrouped, ActionGranular) were dropped.
  - Imputed missing values in remaining columns using mode or median strategies.

***Data Type Conversions:*** Ensured proper data types for numerical and categorical columns.

***Outlier Treatment:*** Outliers in numerical columns like AlertCount and Severity were capped.

**Data Visualization**
---

***Target Distribution:***
  - Bar chart showing the imbalanced distribution of TP, FP, and BP.

***Feature Analysis:***
  - Heatmap showing correlations between AlertCount, Severity, and other features.
  - Pie chart of MitreTechniques usage percentages.

**Modeling Building**
---

The prediction model was built following these steps:

***Data Balancing:***
Applied SMOTE and SMOTETomek to handle the class imbalance in True Positive.

***Train-Test Split:***
Used an 80/20 split for training and testing.

***Algorithms Tested:***
  - Logistic Regression
  - Random Forest
  - XGBoost (best performance)
***Threshold Tuning:***
Adjusted decision boundaries to reduce false positives further.

**Model Evaluation**
---

***Accuracy:*** Overall classification performance.

***Precision, Recall, and F1-Score:*** Trade-off between false positives and false negatives.

***Confusion Matrix:*** Visualized TP, FP, and BP counts.

***ROC-AUC Curve:*** Assessed the model's ability to separate the three classes.
