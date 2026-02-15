# Stroke Classifier

## Introduction

This project is a classification task aiming to differentiate patients belonging to the stroke or no stroke classes.

To do so, this project utilized the [Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) from Kaggle.

## Method

The dataset in question is composed of 11 clinical features and 5110 observations only 5% of which belong to the positive class. This makes the dataset extremly imbalanced. To deal with this problem the data was augmented using the synthetic minority oversampling technique (SMOTE) combined with undersampling of the majority class.

The data is processed in a pipeline to streamline the code. The pipeline applies mean imputation and standard scaling before applying the oversampling and undersampling methods. The pipeline also accomodates cross-validation while maintaining proper separation between training and validation data.

Cross validation was used in order to finetune logistic regression parameters to improve precision. However, in this case, it did not lead to a significant difference.

The jupyter notebooks present confusion matrices for the logistic regression and random forest models, as well as their ROC curve.

The final performance of the model resulted in a recall score of 0.82 for the minority class, and a precision score of 0.11.
