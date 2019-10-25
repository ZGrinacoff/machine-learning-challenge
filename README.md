# Machine Learning: Exoplanet Exploration

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I created machine learning models capable of classifying candidate exoplanets from the raw dataset. The steps taken to do so are outlined below:

## Repository Navigation:

* machine-learning-challenge (Repo Home):
  * README.md
  * exoplanet_data.csv
  * **exoplanet_exploration_randomForest.ipynb**
  * exoplanet_exploration_svm.ipynb
  * Images (Folder):
    * featureimportance.png
    * randomforest_classificationreport.png
  * Models (Folder):
    * **zGrinacoff_randomForest.sav**
    * zGrinacoff_svm.sav
   
**PLEASE USE RANDOM FOREST MODEL**

## Preprocess the Data:

  * Preprocess the dataset prior to fitting the model.
  * Perform feature selection and remove unnecessary features.
  * Use MinMaxScaler to scale the numerical data.
  * Separate the data into training and testing data.
  
## Tune Model Parameters:

  * Use GridSearch to tune model parameters.
  * Tune and compare two different classifiers (Support Vector Machine & Random Forest Classifier).
  
## Report and Final Model Outcome:

  * Even without controlling GridSearchCV params, the Random Forest Model was much more effective and capable in classifying candidate exoplanets.
  
  *  Random forests are much simpler to train for a practitioner; it’s easier to find a good, robust model. The complexity of a random forest grows with the number of trees in the forest, and the number of training samples we have. In SVMs, we typically need to do a fair amount of parameter tuning, and in addition to that, the computational cost grows linearly with the number of classes as well.

## Random Forest:

  |               | BeforeCV      | AfterCV       |
  |:-------------:|:-------------:|:-------------:|
  |Training Score | 0.995         | 1.0           |
  |Testing Score  | 0.883         | 0.899         |
  
Random Forest Classification Report:
![alt text](https://github.com/ZGrinacoff/machine-learning-challenge/blob/master/Images/randomforest_classificationreport.png "Random Forest Classification")


Random Forest Feature Importance:
![alt text](https://github.com/ZGrinacoff/machine-learning-challenge/blob/master/Images/featureimportance.png "Random Forest Feature Importance")
  
## Support Vector Machine:

  |               | BeforeCV      | AfterCV       |
  |:-------------:|:-------------:|:-------------:|
  |Training Score | 0.846         | 0.887         |
  |Testing Score  | 0.842         | 0.879         |
  
  * Although the Random Forest model was quite successful, it would be important to train and test additional models for accuracy and reliability. However, for a first time Machine Learning project, I am quite happy with the results. I look forward to further exploration in Machine Learning and beyond our planet's solar system!
