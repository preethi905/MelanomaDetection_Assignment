# Melanoma Detection - Convolution neural network assignment

## Table of Contents
* [General Information](#General Information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)


## General Information

To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:
- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion


Data can be downloaded from [here](https://drive.google.com/file/d/1xLfSQUGDl8ezNNbUkpuHOYvSpTyxVhCs/view).

## Technologies Used
- Tensorflow
- Keras
- Augumentor
- numpy, Matplotlib, panda, seaborn

## Conclusions
- Training accuracy of the model seems to increase linearly whereas validation accuracy remained stagnant around 55%
High training accuracy means the model has learnt the noise in the data as well, however its poor performance on validation data shows lack of generalizability of the model.
The above observations confirm the case of overfitting. To mitigate overfitting augmentation technique will be used. Since the training data available is less, we will generate new samples by slightly modifying the existing training data (for eg. flipping the image horizontally/vertically, slightly rotating the image etc) and use them for training the model as well.

- Model Performance is not imporved, so the imbalanced data needs to be balanced using augumentations, increasing each class count to 500

- After balancing the data, From training accuracy and validation accuracy we can conclude that the model is stable val accuracy is 83.74 futher increasing the number of epochs will improve the accuracy.



## Contact
Created by [@preethi905] - feel free to contact me!

