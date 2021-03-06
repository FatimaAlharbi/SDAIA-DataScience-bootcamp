 # Tomato Disease Classifier with Convolutional Neural Network
Fatima Alharbi

## Abstract
The goal of this project was to use classification model to clasify and identify the leaf status if infected by any disease or healthy . In order to help improve agriculture and make a good impact in sustainablity . I worked with data provided by [Kaggle](https://www.kaggle.com/emmarex/plantdisease/)  that contains many crops but to be more accurate I selected all related toTomato leafs , training along with a Convolutional Neural Network model to achieve promising results for this multiclass problem. After refining a model, I deploy the model to an API.      

## Design
This project originates to Classifying statuses accurately via deel learning learning model would enable the socity to improve operations and maintenance planning of agriculture units, allocate resources more quickly to needed to prevent spread of diseases , and ensure water is not wasate .

## Data
 The dataset collected from Kaggle contains 27000 pictures includes 8 diseases and healthy leaf for different crops. In this project, I used Tomato leafs and it has 9 diseases and healthy leaf dataset as follows:
- 'Tomato_Bacterial_spot'.
- Tomato_Early_blight'.
- Tomato_Late_blight'.
- Tomato_Leaf_Mold'.
- Tomato_Septoria_leaf_spot'.
- Tomato_Spider_mites_Two_spotted_spider_mite'.
- Tomato__Target_Spot'.
- Tomato__Tomato_YellowLeaf__Curl_Virus'.
- Tomato__Tomato_mosaic_virus'.
- Tomato_healthy.

## Deep learning Model

*Convolutional Neural Network*
  
.


**CNN** 
   - Accuracy: 0.9571 

## Tools
- TensorFlow for modeling
- Keras for modeling, layers
- Matplotlib for plotting
- FastAPI for deploy model as api

## Communication
 The presentation [slides here](https://github.com/FatimaAlharbi/SDAIA-DataScience-bootcamp/blob/58d5957efb536e30ab0d5100390c9aca0e802f95/SDAIA%20project.pptx)
 
 
 # How to run code
 ## Training the Model
- Download the data from [Kaggle](https://www.kaggle.com/emmarex/plantdisease/).
- Only keep folders related to Tomatos.
- Run Jupyter Notebook in Browser.
```sh
Jupyter Notebook
```
- Open [training/training_CNN.ipynb](https://github.com/FatimaAlharbi/SDAIA-DataScience-bootcamp/blob/dee473df629380aa8ca765871c3f974ba9d24381/training/training_CNN.ipynb) in Jupyter Notebook.
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


