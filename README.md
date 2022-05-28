# Pneumonia_Detection_Xray_Image_Processing
Identifying Medical Diagnoses and Treatable Diseases by Image-Based Deep Learning

## Introduction
Because of a number of other conditions in the lungs, such as fluid overload, bleeding, volume loss, and lung cancer, diagnosing pneumonia on chest X-ray images is difficult. In addition, every shift, clinicians read a large number of images. When clinicians are tired or distracted, they may miss some details in the image. Deep learning-based pneumonia detection can assist clinicians in diagnosing the disease.

## Data
Kaggle's Chest X-Ray Images (Pneumonia) dataset was used. https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia is the link. The data set is divided into three folders: test, train, and val. Additionally, each folder contains two subfolders: 'normal' and 'pneumonia.'

## Model
I created a CNN model (convolutional neural network).
With convolutional layers and max-pooling, I used five convolutional blocks.
I started with a flatten layer and then added fully connected layers on top of it.
I've also used dropout to avoid overfitting.
Because this is a binary classification problem, the activation function was Relu throughout except for the last layer, where it was Sigmoid.
RMSprob was used as the optimizer, and cross-entropy was used as the loss. ModelCheckpoint and EarlyStopping are two callbacks I define before training the model.

## Transfer Learning
I used transfer learning with two models, VGG16, VGG19, InceptionV3, and ResNet50, and the model ResNet50 produced the best results.

## Results of the Best Model
The model's accuracy is 0.93.
The model's recall is 0.98.
The model's precision is 0.91, and its f1 score is 0.94.
The accuracy refers to the percentage of total data that was correctly predicted.
"What percent of the positive cases did you catch?" says the recall.
"What percentage of your predictions were correct?" is what precision means.
The harmonic mean of precision and recall is the f1-score. "What percentage of positive predictions were correct?" it asks.

## Conclusion
I built a CNN model from scratch and used VGG16, VGG19, InceptionV3, and ResNet50 transfer learning models. The best model was ResNet50, which has a 93 percent accuracy rate in detecting pneumonia disease.
