# Heart Disease Prediction using Machine Learning
This project aims to predict the presence of heart disease using a Logistic Regression model. The task is formulated as a binary classification problem where the model predicts whether a patient has heart disease based on clinical and demographic features.

DATASET:
The dataset used in this project is the Heart Disease dataset from the UCI Machine Learning Repository.
The dataset contains 918 patient records with 11 original clinical features. After one-hot encoding categorical variables, the dataset expanded to 21 features.

Target variable:

0 → No heart disease

1 → Heart disease

Class distribution:

508 patients with heart disease

410 patients without heart disease

The dataset is relatively balanced.

Data Preprocessing:
The following preprocessing steps were applied:

1-Verified absence of missing values
2-Removed duplicate records (none found)
3-Detected outliers in Age using the IQR method
4-Applied one-hot encoding to categorical variables
5-Standardized numerical features (Age, RestingBP, Cholesterol, MaxHR, Oldpeak) using StandardScaler
6-Split data into 80% training and 20% testing sets (random_state = 42)

Model
Logistic Regression
Logistic Regression was used for binary classification. It models the probability of heart disease using the sigmoid function:
P(y=1|x) = 1 / (1 + e^(-z))
Regularization was applied to prevent overfitting.

Hyperparameter Tuning
GridSearchCV with 5-fold cross-validation was used to tune:
C (regularization strength)
Penalty type
Solver
Best parameters found:
C = 1
penalty = l1
solver = saga
Best cross-validation accuracy: 0.864
