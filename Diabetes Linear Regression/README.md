# Linear Regression on Diabetes Data

## Introduction

This project involved developing a machine learning model using linear regression to analyse and predict various pieces of human data such as BMI, blood pressure, and diabetes pedigree function.

## Data Sources

The dataset used for this project was obtained from Kaggle, available here: https://www.kaggle.com/datasets/mathchi/diabetes-data-set. This dataset was originally taken from larger datasbase from the National Institute of Diabetes and Digestive and Kidney Diseases.

The columns in the dataset included:

- Pregnancies: Number of times pregnant
- Glucose: Plasma glucose concentration, 2 hours in an oral glucose tolerance test
- BloodPressure: Diastolic blood pressure (mm Hg)
- SkinThickness: Triceps skin fold thickness (mm)
- Insulin: 2-hour serum insulin (mu U/ml)
- BMI: Body mass index (weight in kg / (height in m)^2)
- DiabetesPedigreeFunction: Probability of diabetes based on family history
- Age: Age in years
- Outcome: Presence of diabetes (0 or 1)

## Pre-Processing

No pre-processing was performed on the dataset.

## Tools and Tech Used

This project is written in Python in a Jupyter Notebook.

## Findings

From performing operations on this data I have found that many of these fields have no correlation between them. For example, there seems to be no accurate link between blood pressure and skin thickness.
However, there are some fields here where a noticable correlation is present. For example, BMi and skin thickness. There is a noticable trend of increased skin thickness as BMI rises.

Findings like this could have clinical relevance. For example, the correlation found between BMI and skin thickness could suggest that monitoring BMI could be important for assessing skin-related health issues.

I think the data here shows the limitations of linear regression as many of the pieces of data have no linear correlation between them. Perhaps a different machine learning model could find a more consistent pattern that could be used for accurate predictions.

There could potentially be many other variables that could affect these data values that haven't been considered in this dataset, such as height.