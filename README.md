# Predicting Medical Costs Using Machine Learning 

**Project Overview Group ( 240202448, 240149659, 240213444, 240228482 )**

This project focuses on predicting medical charges for individuals based on their personal attributes such as age, BMI, smoking status, and other factors. The analysis aims to support healthcare providers and insurance companies in budgeting, resource allocation, and setting fair premiums.
We explore data exploration, preprocessing, model development, evaluation, and ethical implications in this end-to-end machine learning pipeline.

Dataset

    Name: Insurance.csv.
    Features:
        Numerical: Age, BMI, Number of Children, Charges.
        Categorical: Sex, Smoking Status, Region.
    Target Variable: charges (medical costs).
    Size: 1338 samples.

Project Workflow
1. Data Exploration

    Explored the dataset to understand distributions and patterns.
    Key statistics:
        Average age: 39 years (range: 18–63).
        Average BMI: 30 (range: 17–42).
        Average charges: $13,270 (range: $1,137–$51,194).
    Visualizations:
        Pair plots and box plots to identify trends and outliers.

2. Data Preprocessing

    Handling Categorical Variables:
        Label-encoded sex, smoker, region, and created age_group.
    Feature Scaling:
        Standardized numerical features using StandardScaler.
    Feature Engineering:
        Created an age_group variable to categorize age into bins.

3. Correlation Analysis

    Used a heatmap to examine correlations between features.
    Observations:
        smoker and charges showed the strongest correlation.

4. Model Development

    Algorithms Used:
        Linear Regression
        Support Vector Regression (SVR)
        Random Forest Regressor
    Training and Evaluation:
        Split dataset into 80% training and 20% testing.
        Used cross-validation (5-fold) for robust evaluation.

5. Recursive Feature Elimination (RFE)

    Selected top features contributing to predictions:
        smoker, bmi, and age_group.

6. Hyperparameter Tuning

    Performed GridSearchCV for Random Forest:
        Tuned parameters: n_estimators, max_depth, min_samples_split, and min_samples_leaf.

7. Ethical Implications

    Privacy: Data anonymization and secure storage.
    Fairness: Avoid biased predictions disadvantaging vulnerable groups.
    Transparency: Clear communication about predictive processes.

Results
Model Performance Metrics
Model	RMSE	MAE	R²	CV R²
Linear Regression	0.54	0.38	0.72	0.68
Support Vector Regression	0.49	0.35	0.78	0.75
Random Forest Regressor	0.42	0.31	0.84	0.82

    Best Model: Random Forest Regressor.

Feature Importance

    Key predictors:
        smoker: Strong influence on charges.
        bmi: Moderate influence.
        age_group: Adds contextual relevance.

Limitations and Future Work
Limitations

    Limited diversity in regional data.
    Basic preprocessing and feature engineering.

Future Work

    Increase dataset size for better generalization.
    Test advanced algorithms like Gradient Boosting.
    Incorporate socioeconomic and lifestyle features.

How to Run
Prerequisites

    Python 3.7 or higher.
    Required libraries: pandas, numpy, matplotlib, seaborn, scikit-learn.

Steps

    Clone the repository and navigate to the Notebook.
    Install dependencies using:

pip install -r requirements.txt


Run the Notebook:

    Assessment componet 2 Group.ipynb

Files in Repository

    Assessment componet 2 Group.ipynb: Main script for data processing, model training, and evaluation.
    requirements.txt: List of dependencies.
    README.txt: Project documentation.
    Dataset: insurance.csv 

Acknowledgments

    Dataset Source: University internal
    Libraries Used: scikit-learn, pandas, numpy, seaborn, matplotlib.


