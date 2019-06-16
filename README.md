# Cars' year, make and model prediction on Stanford Cars dataset using ResNet152
This solution is for traning a Deep Neural Network for prediction of car year, make, model based on car images provided by Stanford. This is classic use case of CNN models for developing a classification model. I have used a ResNet152 model which is very widely used in computer vision field and also working very good in most of the cases.

This activity has been divided into three major part which are:
1. **Pre-processing the image dataset**
2. **Training and validation of model**
3. **Prediction on new images**

Lets go one by one on all the three steps.
# 1. Pre-processing the image dataset
The steps involved in preparing image dataset are below:
* Download the dataset and unzip it into google colab workspace
* Create training, validation sets from initial training set and organize according to class label
* Store test dataset in test folder

This process is done in **Pre-Processing.ipynb** where all the steps explained in detail.

# 2. Training and validation of model
I have used Fastai implementation on ResNet152 model which very fast in terms of learning time and also giving very good accuracy with 30 minutes of training time.Here are the steps involved in training and validation:
* Creating data augmentation and batches to feed into model
* Using pre-trained model as initial step towards model building
* Unfreezing the model and train the model for all weights
* Checking accuracy on validation data and testing dataset

All of the above steps are done in **Training&Validation.ipynb** notebook. All steps are explained in detail inside the notebook.



https://drive.google.com/file/d/1kh-xsHcyjdNg-F9FxDbUZtOAHz2h2qpn/view?usp=sharing
