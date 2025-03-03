# Email Spam Support Vector Machine Project

## Dataset

Dataset containing 83,446 emails labelled either spam or not spam. Dataset obtained from Kaggle at https://www.kaggle.com/datasets/purusinghvi/email-spam-classification-dataset/data.

Dataset contains the columns:

- label: If the email was spam or not (1 for spam, 0 for not spam)
- text: The contents of the email.

## Preprocessing

No preprocessing was performed on the dataset.

##  Tools and Tech Used

This project is written in Python in a Jupyter Notebook.

## Findings

From performing operations on this dataset, I have found that the Support Vector Machine model was overfit to the data. This can be seen by the results in the classification report, with every accuracy measurement being above 0.98. 

This issue was marginally improved by lowering the regularisation parameter, but not be enough to solve the overfitting issue.

A model with a regularisation parameter of 0.01 led to much better results. Their may still be some overfitting as seen in the negative prediction precision score and the positive prediction recall score but the other metric show that the model is in a much better state.