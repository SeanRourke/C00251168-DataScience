# Cats and Dogs Classification Convolutional Neural Network Project

## Dataset

Dataset containing 10,000 images of cats and dogs. Dataset obtained from Kaggle at https://www.kaggle.com/datasets/tongpython/cat-and-dog. 

Dataset contained following (class / number of images):

- cat / 5,000
- dog / 5,000

## Preprocessing

All images are resized to 244 x 244 in this notebook. The original dataset was separated into training and test folders of images, these folders were combined and the data was split in this notebook instead.

##  Tools and Tech Used

This project is written in Python in a Jupyter Notebook.

## Findings

From performing operations on this dataset, I have found that this convolutional neural network created to classify the cats and dogs was not accurate. As seen by the accuracy score of around 0.75, the model is correct in its classification more often than not, but is not consistent enough to be relied upon.