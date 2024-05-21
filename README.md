Simulation Study for Estimating Treatment Effects


Overview

This project compares the effectiveness of Propensity Score Matching (PSM) and Double Machine Learning (DML) in estimating treatment effects using the Infant Health and Development Program (IHDP) dataset. The study employs various machine learning models within the DML framework, including Random Forest, XGBoost, and Neural Network. The simulation aims to provide insights into the precision and stability of these methods in a realistic observational study setting.

Dataset
The IHDP dataset includes data on 747 subjects with 25 variables, encompassing treatment assignment and various covariates. To simulate an observational study, selection bias is introduced by removing a non-random subset of treated individuals.

Methods

Propensity Score Matching (PSM)
PSM involves:

Estimating propensity scores using logistic regression.
Matching treated and untreated subjects based on their propensity scores.
Estimating the treatment effect by comparing outcomes of matched pairs.

Double Machine Learning (DML)

DML leverages machine learning models to flexibly model the relationships between covariates and outcomes, orthogonalizing the estimation process to mitigate biases. The models used in this study are:
Random Forest
XGBoost
Neural Network
Simulation Steps
Data Preparation
Load the IHDP dataset.
Introduce selection bias by removing a subset of treated individuals.
Split the dataset into training and test sets.
Define covariates, treatment, and outcome variables.
PSM Implementation
Estimate propensity scores using logistic regression.
Perform matching based on propensity scores.
Estimate the treatment effect for matched pairs.
DML Implementation
Create DoubleMLData objects for the dataset.
Define DML models using different machine learning algorithms.
Fit the models and estimate treatment effects.
Performance Evaluation
Use bootstrapping to estimate the variability of treatment effect estimates.
Calculate mean, variance, and confidence intervals for the estimates.
Results
The results are summarized in a table, highlighting the mean estimate, ATT, variance estimate, and 95% confidence intervals for each method.

Dependencies

Python 3.6+
pandas
numpy
scikit-learn
xgboost
doubleml
tabulate
Running the Simulation
Clone the repository and navigate to the project directory.
Ensure all dependencies are installed.

Conclusion

The study concludes that DML methods, particularly with Random Forest, offer more precise and stable estimates of treatment effects compared to PSM. The theoretical advantages of DML in handling high-dimensional data and reducing bias through orthogonalization contribute to its superior performance. However, the results are based on the IHDP dataset, and further validation is necessary to generalize the findings.

Limitations

The results are specific to the IHDP dataset and may not generalize to other datasets.
The dataset size and covariate structures influence the performance of the methods.
Further research is needed to validate the findings in different contexts.
