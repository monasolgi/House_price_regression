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

## Final Observations

Different regression models behaved differently on the House Prices dataset.

### Linear Regression

Linear Regression achieved the weakest performance.
Possible reasons:

* the dataset contains many correlated features
* many one-hot encoded categorical variables
* the model is too simple for some nonlinear relationships in the data

### Ridge Regression

Ridge Regression improved performance noticeably compared to standard Linear Regression.

Possible reason:

* Ridge regularization penalizes large coefficients
* this helps reduce overfitting and stabilizes the model when many correlated features exist

### Random Forest Regressor

Random Forest improved over Linear Regression but did not outperform Ridge Regression.

Possible reason:

* the dataset contains many sparse one-hot encoded features
* Random Forest may not capture smooth numerical relationships as effectively in this setup

### Gradient Boosting Regressor

Gradient Boosting achieved the best Kaggle score.

Possible reason:

* Gradient Boosting learns sequentially from previous errors
* it often performs very well on structured/tabular datasets such as house-price prediction tasks

---

<img width="1464" height="902" alt="image" src="https://github.com/user-attachments/assets/56aa3580-3d7f-42ef-a392-f62047e30e54" />

---

## Future Improvements

* Hyperparameter tuning
* Feature engineering
* XGBoost / LightGBM
* Better handling of skewed numerical features
  
