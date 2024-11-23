# Decision Tree on Heart Disease Data

## Introduction

This project involves developing a machine learning model using a decision tree to predict the presence of heart disease based on information about a person.

## Data Sources

The dataset used for this project was obtained from Kaggle at https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease, the original data obtained by the Center for Disease Control and Prevention.

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

The PhysicalHealth and MentalHealth columns were removed before model training as the majority of the data was empty and no information was provided on how the result was arrived at. 

## Tools and Tech Used

This project is written in Python in a Jupyter Notebook.
Excel was used for the pre-processing of the dataset.

## Findings

From performing operations on this data set, I have found that the decision tree model is very good at predicting the absence of heart disease. The overall accuracy of the model was quite high at 0.86 and a specificity of 0.92. However, the model is not good at correctly predicting the presence of heart disease. This is clearly shown through the precision and recall scores of 0.23 and 0.24 respectively. I think these findings show the risk of relying on machine learning models in medicine. As we are dealing with people's health and wellbeing, we must try to be as accurate as possible with diagnosis. Due to this, despite being accurate as a whole, this model would serve no real world benefit.