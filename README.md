# Machine Learning - Exoplanet Exploration

![exoplanets.jpg](Images/exoplanets.jpg)

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I created machine learning models capable of classifying candidate exoplanets from the raw dataset.

Stages:

1. [Preprocess the raw data](#Preprocessing) 
2. [Tune the models](#Tune-Model-Parameters)
3. [Compare several models](#Evaluate-Model-Performance)

### Preprocess the Data

* Preprocessed the dataset prior to fitting the model.
* Performed feature selection and remove unnecessary features.
* Used `MinMaxScaler` to scale the numerical data.
* Separated the data into **training** and **testing** data.

### Tune Model Parameters

* Used `GridSearch` to tune model parameters.
* Compared at least two different classifiers.

### Reporting

* I applied 3 different models: 
1. `Sequential` from Keras.models is **the best** ( model_loss=0.2712, model_accuracy=0.8802)
2. `Support Vector Machine (SVM)` - SVC from sklearn.svm (modelSVC.score=0.84, modelSVC_accuracy=0.84), then I tune SVM model by `GridSearch` (model.score=0.8859,grid_accuracy=0.88), and this model becomes **the second best**.
3. I tried the `K-Nearest Neighbor Model (KNN)` KNeighborsClassifier from sklearn.neighbors, but found it the worst in this list (modelKNN.score=0.8369, modelKNN_accuracy=0.82)


## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)

