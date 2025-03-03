# Thyroid Cancer Risk k-Nearest Neighbours Project

## Dataset

Dataset containing demographic facts, clinical history, lifestyle factors and key thyroid hormone degrees of patients. The dataset contains information for 212,691 patients. Dataset obtained from Kaggle at https://www.kaggle.com/datasets/mzohaibzeeshan/thyroid-cancer-risk-dataset.

Dataset contains the columns:

- Patient_ID: Unique identifier for each patient.
- Age: The age of the patient.
- Gender: Gender of the patient (Male / Female).
- Country: Patient's country of residence.
- Ethnicity: Patient's ethnic background.
- Family_History: Whether the patient has a family history of thyroid cancer (Yes / No).
- Radiation Exposure: History of radiation exposure (Yes / No).
- Iodine_Deficiency: Presence of iodine deficiency (Yes / No).
- Smoking: Whether the patient smokes (Yes / No).
- Obesity: Whether the patient is obese (Yes / No).
- Diabetes: Whether the patient has diabetes (Yes / No).
- TSH_Level: Thyroid-Stimulating Hormone level (µg/dL).
- T3_Level: Triiodothyronine level (ng/dL).
- T4_Level: Thyroxine level (µg/dL).
- Nodule_Size (float): Size of thyroid nodules (cm).
- Thyroid_Cancer_Risk (object): Estimated risk of thyroid cancer (Low/Medium/High).
- Diagnosis (object): Final diagnosis (Benign/Malignant).

## Preprocessing

The Patient_ID column was removed before training as it should have no relation to the presence of thyroid cancer.

## Tools and Tech Used

This project is written in Python in a Jupyter Notebook.
Excel was used for the pre-processing of the dataset.

## Findings

From performing operations on this dataset, I have found that using k-Nearest Neighbours with a value of 3 neighbours is somewhat accurate but not enough to be considered useful in the medical field. An accuracy value of 0.77 is not terrible but when the prediction involves people's health it is not accurate enough. Using more detailed accuracy measurements, we can see that the model is quite accurate at predicting the absence of thyroid cancer, with precision, recall and f1 score values of 0.82, 0.90 and 0.86 respectively. It struggled with accurately predicting the presence of thyroid cancer, using the same measures we get values of 0.51, 0.35 and 0.41. This could be due to many things such as needing more malignant data or using a different value for k in our prediction.

When using 5 neighbours instead of 3, we see an increase in every accuracy measurement except for malignant diagnosis recall, which saw a decrease of 0.01. These improvements are not enough to make a signifcant difference but they do show that there could be potential for further improvement with a different amount of neighbours once again.

Operations were performed with classifier models instead of regression models to see if that would lead to more accurate results but no change was found.

Using GridSearchCV, it was determined that 13 was the best value for k between 1 and 50. Creating a model using this value led to a further increase in total accuracy, but notably, malignant diagnosis recall and f1 score saw further decreases in score.

Using GridSearchCV, I found the best method for weighting neighbours. Using this and the best k value, I created a bagging classifier model, that uses bootstrap sampling, where multiple subsets of the training data are created by random sampling with replacement. This model did not result in any improvement in the accuracy measurements. The only change was a reduction in malignant diagnosis recall by 0.01.

The most accurate model was the classifier model using a k value of 13.