# Random Forest on Real Estate Dara

## Introduction

This project involves developing a machine learning model using a random forest to predict the price of a house based off of other information about the house.

## Data Sources

The dataset used for this project was obtained from Kaggle at https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset, original data obtained from https://www.realtor.com/.

Dataset contains the columns:

- HeartDisease: If the person has heart disease
- BMI: Body mass index (weight in kg / (height in m)^2)
- Smoking: If the person smokes
- AlcoholDrinking: If the person drinks alcohol
- Stroke: If the person has suffered from a stroke
- PhysicalHealth: Person's physical health
- MentalHealth: Person's mental health
- DiffWalking: Does the person have difficulty walking
- Sex: Male or female
- Age Category: 18-24, 25-29, 30-34, 35-39, 40-44, 45-49, 50-54, 55-59, 60-64, 65-69, 70-74, 80 or older
- Race: American Indian/Alaskan Native, Black, Hispanic, Other, White
- Diabetic: If the person is diabetic
- Physical Activity: Does the person participate in physical activity
- GenHealth: Quality of person's general health. Poor, Fair, Good, Very Good, Excellent
- SleepTime: Amount of sleep in hours
- Asthma: If the person has asthma
- KidneyDisease: If the person has kidney disease
- SkinCancer: If the person has skin cancer

## Pre-Processing

prev_sold_date column was removed to make dataset smaller due to memory restrictions. For the same reason, the data was sorted by brokered_by in ascending order and only the first 300,000 rows were used for this project.

Any row containing a null value for a column was also removed.

## Tools and Tech Used

This project is written in Python in a Jupyter Notebook.
Excel was used for the pre-processing of the dataset.

## Findings

From performing operations on this dataset, I have found that the random forest model used is very innacurate, with an accuracy score of 0.0003. This model is essentially useless for predicting house prices based on the information in the dataset. This could potentially be improved if all of the dataset could be used but that was not possible in my case. Due to the format of the results, I was unable to display the confusion matrix or provide values for precision, recall, specificity or f1.