# Image Classification
This was the first homework of the Artificial Neural Network and Deep Learning course 2020/2021.

Developed by Diego Savoia and Francesco Emanuele Stradi.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/savoiadiego/Image-Classification/blob/main/Image%20Classification.ipynb)

The goal was to classify images depicting groups of people based on the number of masked people. More specifically, the solution discriminates between images depending on the following cases:
* All the people in the image are wearing a mask
* No person in the image is wearing a mask
* Someone in the image is not wearing a mask

Thus, the classification is performed on 3 different classes. Being a classification problem, given an image, the goal is to predict the correct class label. The output is a csv file containing the predictions associated to each test image.

### Dataset Details
* Image size: variable
* Color space: RGB
* File Format: JPG
* Number of classes: 3
* Classes:
  * 0: "NO PERSON in the image is wearing a mask"
  * 1: "ALL THE PEOPLE in the image are wearing a mask"
  * 2: "SOMEONE in the image is not wearing a mask"

### Dataset Structure
* Two folders:
  * training: 5614 images
  * test: 450 images
* Training images per class:
  * 0 : 1900 
  * 1 : 1897
  * 2 : 1817
* Ground Truth:
  * Labels for images are provided in the *train_gt.json" file.
  
### Implementation
The notebook is meant to be used in Google Colaboratory, loading the dataset from Drive as explained inside the notebook.
After the data preparation part, there are five different models to train and use for predictions:
* Custom model
* Custom model variation
* Transfer Learning using VGG-16
* Transfer Learning using InceptionV3
* Transfer Learning using ResNet

Every model can be trained on the given dataset, using 20% of the samples for validation. Then, the prediction can be computed on the samples in the test folder. After that, the csv file containing the predictions is exported inside the Drive directory.
