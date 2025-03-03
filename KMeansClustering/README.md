# Wine Quality K-Means Clustering

## Dataset

Dataset containing information about the red variants of the Portuguese "Vinho Verde" wine. Dataset contains 1,599 rows of data. Dataset obtained from Kaggle at https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009. 

Dataset contains the columns:

- fixed acidity: Referring to acids that do not evaporate easily
- volatile acidity: Referring to acids that can evaporate at room temperature
- citric acid: The level of citric acid in the wine
- residual sugar: The level of residual sugar in the wine
- chlorides: The level of chlorides in the wine
- free sulfur dioxide: Portion of sulfur dioxide not bount to other molecules
- total sulfur dioxide: Sum of free and bound sulfur dioxide in the wine
- density: The density of the wine
- pH: The pH of the wine
- suphates: The level of sulphates in the wine
- alcohol: The alcohol percentage of the wine
- quality: Quality score between 0 and 10


## Preprocessing

No preprocessing was performed on the dataset.

##  Tools and Tech Used

This project is written in Python in a Jupyter Notebook.

## Findings

From performing operations on this dataset, I have found that the K-Means Clustering model was not very accurate. As seen in the graph the clusters are somewhat distinct, but the silhouette score shows that there is some degree overlap.

The K-Means algorithm was then ran using an n_init parameter of 20, meaning that the algorithm was run 20 times to find the best centroid initialisation. This resulted in a very minor increase in model performance but not enough to make the model useful.