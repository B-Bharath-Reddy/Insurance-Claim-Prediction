
# Insurance Claim Prediction

This project aims to develop a predictive model to assess the claim probability for car insurance policies. The primary goal is to understand the factors influencing claim frequency and severity, helping insurance companies better assess risk and determine premiums.

## Project Overview

### Objectives
- Develop a predictive model for car insurance claim probability.
- Understand the key factors that influence insurance claims.
- Improve claims processing accuracy and reduce fraudulent claims.

### Dataset
- **Source:** Provided by Learnbay
- **Size:** 58,592 rows and 44 columns
- **Key Features:** 
  - `policy_id`: Unique identifier
  - `policy_tenure`: Duration of the policy
  - `age_of_car`: Age of the car
  - `age_of_policyholder`: Age of the policyholder
  - `area_cluster`: Area category
  - `population_density`: Population density of the area
  - `make`: Car manufacturer
  - `model`: Car model
  - `segment`: Car segment
  - `fuel_type`: Type of fuel used

## Data Preprocessing
- **Missing Values:** No missing values were found.
- **Encoding:** One-hot encoding was used for categorical variables.
- **Scaling:** StandardScaler was applied to numerical features.
- **Outlier Treatment:** Z-score method was used to identify and treat outliers.

## Exploratory Data Analysis (EDA)
- **Target Variable Distribution:** Imbalanced dataset (94% no-claim, 6% claim).
- **Univariate Analysis:** Histograms and box plots for numerical features; count plots for categorical features.
- **Bivariate Analysis:** Histograms, box plots, and count plots to analyze relationships between pairs of features.

## Statistical Tests and Feature Selection
- **ANOVA:** Used to identify significant differences between groups for numerical features.
- **Chi-Square Test:** Identified significant associations between categorical features and the target variable.
- **Feature Importance:** Random Forest and Gradient Boosting were used to identify important features.
- **Principal Component Analysis (PCA):** Reduced 67 features to 26 components.

## Model Training and Evaluation
### Algorithms Considered
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- XGBoost Classifier
- Gradient Boosting Classifier
- AdaBoost Classifier

### Chosen Models
- **AdaBoost Classifier**
- **Gradient Boosting Classifier**

### Process
- **Train-Test Split:** 70:30 ratio
- **Handling Imbalanced Data:** Oversampling techniques applied to training data.
- **Hyperparameter Tuning:** RandomizedSearchCV used for efficient hyperparameter tuning.
- **Evaluation Metrics:** F1 Score, Precision, Recall, and ROC-AUC on both training and test sets.

### Model Performance on Test Set
| Model                    | Test F1 Score | Test Precision | Test Recall | Test ROC-AUC |
|--------------------------|---------------|----------------|-------------|--------------|
| Logistic Regression      | 0.144         | 0.083          | 0.554       | 0.594        |
| Decision Tree Classifier | 0.085         | 0.073          | 0.100       | 0.517        |
| XGBoost Classifier       | 0.059         | 0.105          | 0.041       | 0.593        |
| AdaBoost Classifier      | 0.148         | 0.096          | 0.326       | 0.619        |
| Random Forest Classifier | 0.113         | 0.093          | 0.142       | 0.593        |
| Gradient Boosting        | 0.071         | 0.128          | 0.049       | 0.635        |

### Key Observations
- **AdaBoost Classifier:** Highest Test F1 Score (0.148) and Test ROC-AUC Score (0.619).
- **Gradient Boosting Classifier:** Highest Precision (0.128) and highest ROC-AUC Score (0.635).

## Challenges and Solutions
- **Imbalanced Dataset:** Applied oversampling techniques and appropriate evaluation metrics.
- **High Computational Time:** Reduced hyperparameter grid and used efficient search techniques like RandomizedSearchCV.
- **Model Selection:** Evaluated multiple models to determine the best-performing one based on training and test performance.

## Business Impact
- **Improved Claims Processing Accuracy:** Enhanced accuracy in predicting insurance claims, leading to more reliable and fair assessments.
- **Cost Savings:** Efficient resource allocation and reduced manual review workload.
- **Return on Investment (ROI):** Quantifiable benefits such as reduction in fraudulent claims and improved operational efficiency.

## Conclusion
The AdaBoost and Gradient Boosting classifiers demonstrated strong performance, with AdaBoost providing a good balance and Gradient Boosting offering slightly better precision and ROC-AUC. The choice between these models can depend on specific application needs.



---

