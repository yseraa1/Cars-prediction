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

This process is done in **Pre_Processing.ipynb** where all the steps explained in detail.

# 2. Training and validation of model
I have used Fastai implementation on ResNet152 model which very fast in terms of learning time and also giving very good accuracy with 30 minutes of training time.Here are the steps involved in training and validation:
* Creating data augmentation and batches to feed into model
* Using pre-trained model as initial step towards model building
* Unfreezing the model, geting optimal learning rate and epochs and train the model for all weights
* Checking accuracy on validation data and testing dataset

All of the above steps are done in **Training&Validation.ipynb** notebook. All steps are explained in detail inside the notebook. I have got 70% accuracy on validation dataset using pre-trained model whereas got 88% using unfreezing and training model again. Accuracy on test dataset images is coming as 88%, which is quite good. This can also be improved by creating hybrid modesl, experimenting with mixing different types of hidden layers.

# 3. Prediction on new images
If you have to predict the car's year,make,model then, you don't have to go through Step 1 & 2. You can directly jump into Step 3. For predicting new images(cropped using bounding box or no-cropped), you need to download this repository where **Predicting.ipynb** and **models/resnet152.pth** is useful for you. The steps involved are:
* Download this git repository
* Download trained resnet152 weights from this [link](https://drive.google.com/file/d/1kh-xsHcyjdNg-F9FxDbUZtOAHz2h2qpn/view?usp=sharing) into your **models/** folder
* Open **Predicting.ipynb** and change **path** variable to your local directory where all these notebooks, models folder is there
* Create a folder **cars_predict/** and store all the images in this folder for which you have to do prediction
* Create a metadata file( with .mat extension) containing bounding boxes for these prediction images. This file should be similar to **devkit/cars_test_annos.mat** file and the name should be **devkit/cars_predict_annos.mat**. If the images are already cropped using bounding boxes, then there is no need to create metadata file.
* Open **Predicting.ipynb** and change **IsCropRequired** variable. Put **False** if images are already cropped else put **True**. In case of True, you need to store metadata file(**devkit/cars_predict_annos.mat**) as described in above pointer.
* Run the **Predicting.ipynb** which will store a CSV file of predicted classes and their probabilities.


