# Abalones Age

In this notebook we will be looking at abalones data set from UCI
The dataset and description can be found [here](https://archive.ics.uci.edu/ml/datasets/Abalone)

The goal is to predict which age category an observation belongs to based on the information given. 
There are 4177 observations with 7 given variables. The age can be determined by the number of Rings. 
We can roughly classify the age into young (1-9 Rings), medium (9, 10 Rings) and old (10+ Rings).

## Exploratory Data Analysis 

We conduct some exploratory data analysis with visualizations. We can examine several of the variables by the age segments we defined earier. The main visual aide for continous variables is are KDE plots. We see that the young population is more different than the medium and old. The medium and old independent variables are very similar in most cases. This might suggest that differentiating between medium and old will be more difficult than determining if an observation is part of the young class. 

We examine the sex categorical variable using simple bar plots. The data confirms that the scientist have trouble identifying the younger abalone's gender. 

## Analysis 
 
In the PCA Analysis, we find that most of the variance (90%) can be explained by one transformed variable. 
 
Next we use logistic regression pre applied to understand the data. We use cross validation to ensure we have accurate results. 
 
Next we use K Nearest Neighbors and 1 v all logistic regression to predict the age group. 
We conduct a cross validated K Nearest Neighbors with 3 to 20 neighbors. For the K Nearest Neighbors we see that the number of neighbors becomes less important after 14 neighbors and the cross validation score (R2) is around 56%. 

We also try scaling the data and find that the KNN CV performance increases to about 64% with 17 neighbors. 

The jupyter notebook can be found [here](https://github.com/malctaylor15/Abalones_Age/blob/master/Abalones%20Final.ipynb)
