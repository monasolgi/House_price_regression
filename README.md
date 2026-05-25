# House Prices Prediction

## Project Overview

This project predicts house sale prices using regression models and automated preprocessing pipelines.

The project focused on learning regression workflows, handling mixed feature types, and building reusable preprocessing pipelines using scikit-learn.

---

## Dataset

Kaggle House Prices dataset:

* train.csv
* test.csv

Target variable:

* `SalePrice`

---

## Main preprocessing steps

* Removed identifier column:

  * Id

* Separated:

  * numerical features
  * categorical features

* Numerical preprocessing:

  * missing-value imputation
  * scaling

* Categorical preprocessing:

  * missing-value handling
  * one-hot encoding

* Combined preprocessing using:

  * ColumnTransformer
  * Pipeline

---

## Models Used

* Linear Regression
* Ridge Regression
* Random Forest Regressor
* Gradient Boosting Regressor

---

## Evaluation Method

Cross-validation using:

* RMSE (Root Mean Squared Error)

Log-transformed target:

* `np.log1p(SalePrice)`

Inverse transformation for predictions:

* `np.expm1(predictions)`

---

## Kaggle Results

| Model                       | Public Score |
| --------------------------- | ------------ |
| Linear Regression           | 0.15377      |
| Random Forest Regressor     | 0.14582      |
| Ridge Regression            | 0.13269      |
| Gradient Boosting Regressor | 0.13246      |

Gradient Boosting achieved the best score.

---

## Key Concepts Learned

* Regression workflow
* RMSE evaluation
* Ridge regularization
* Pipelines
* ColumnTransformer
* Imputers
* OneHotEncoder
* Log transformation of skewed targets
* Automated preprocessing

---

## Future Improvements

* Hyperparameter tuning
* Feature engineering
* XGBoost / LightGBM
* Better handling of skewed numerical features

<img width="1464" height="902" alt="image" src="https://github.com/user-attachments/assets/56aa3580-3d7f-42ef-a392-f62047e30e54" />
