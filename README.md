 # Tomato Disease Classifier with Convolutional Neural Network
Fatima Alharbi

## Abstract
The goal of this project was to use classification models to predict the operating condition of waterpoints in Tanzania in order to help improve operations and maintenance planning of these units. I worked with data provided by [Taarifa](http://taarifa.org/) and the Tanzanian Ministry of Water, leveraging geographic and categorical feature engineering along with a random forest model to achieve promising results for this multiclass problem. After refining a model, I built an interactive dashboard to visualize and communicate my results using Tableau.      

## Design
This project originates from the [DrivenData competition](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/) "Pump it Up: Data Mining the Water Table". The data is provided by [Taarifa](http://taarifa.org/) and the Tanzanian Ministry of Water, and presents a three-class operational status of **functional**, **functional needs repair**, and **non-functional** for waterpoints across the country. Classifying statuses accurately via machine learning models would enable the Tanzanian Ministry of Water to take action to improve operations and maintenance planning of these units, allocate resources more quickly to needed areas, and ensure potable water is accessible to as many people as possible.

## Data
 The dataset collected from Kaggle contains 27000 pictures includes 8 diseases and healthy leaf.

## Algorithms

*Feature Engineering*
1. Mapping latitude and longitude to 3-dimensional coordinates so nearby continuous values would also be close in reality
2. Converting categorical features to binary dummy variables
3. Combining particular dummies and ranges of numeric features to highlight strong signals and illogical values for waterpoint status identified during EDA
4. Selecting subsets of the total unique values for categorical features that were converted to dummies, according to the number of samples they were associated with and their contribution to certain statuses

*Convolutional Neural Network*
  
Logistic regression, k-nearest neighbors, and random forest classifiers were used before settling on random forest as the model with strongest cross-validation performance. Random forest feature importance ranking was used directly to guide the choice and order of variables to be included as the model underwent refinement.

*Model Evaluation and Selection*
  
The entire training dataset of 59,400 records was split into 80/20 train vs. holdout, and all scores reported below were calculated with 5-fold cross validation on the training portion only. Predictions on the 20% holdout were limited to the very end, so this split was only used and scores seen just once.

The official metric for DrivenData was classification rate (accuracy); however, class weights were included to improve performance against F1 score and provide a more useful real-world application where classification of the minority class (functional needs repair) would be essential.


**CNN** 
   - Accuracy: 0.9571 

## Tools
- TensorFlow for modeling
- Keras for modeling, layers
- Matplotlib for plotting
- FastAPI for deploy model as api

## Communication
 The presentation slides here
 
 
 # How to run code
 ## Training the Model
- Download the data from kaggle. [Kaggle](https://www.kaggle.com/emmarex/plantdisease/)
- Only keep folders related to Tomatos.
- Run Jupyter Notebook in Browser.
```sh
Jupyter Notebook
```
- Open training/training_CNN.ipynb in Jupyter Notebook.
- In cell #2, update the path to dataset.
- Run all the Cells one by one.
- Copy the model generated and save it with the version number in the models folder.


## Running the API
Using FastAPI

1- Get inside api folder

```sh
cd api
```

2- Run the FastAPI Server using uvicorn
```sh
uvicorn main:app --reload --host 0.0.0.0
```

3- Your API is now running at 0.0.0.0:8000

use function predict to start predicting 


