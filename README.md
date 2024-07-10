# Melanoma Detection
> This project is to build a model who can detect Melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths.
> It helps doctors by reducing lot of manual effort required in diagnosis of skin cancer.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)


<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Provide general information about your project here.
  - This project focusses on building a custom CNN model to do Image classification and identify if a particular image has features of Melanoma.
- What is the business problem that your project is trying to solve?
  - Ability to help the dermatologists by reducing the manual effort required in diagnosing of Skin cancer. This will help in reducing the number of deaths caused due to Skin Cancer.
- What is the dataset that is being used?
  - The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). 

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
-Considered Adam and SGD optimizer
  - SGD optimizer doesn't seem to perform well, it has very less train and validation accuracy
  - ADAM optimizer is considered for the following  
    - Basic model seems to overfit with in 9-10 epochs with almost 72% training accuracy and 51% validation accuracy, but with only 27% of test accuracy.
    - Adding a dropout of 0.2 improved the balance a bit between train and validation accuracy. It also improved test accuracy by 8%.
    - Data augmentation balanced the train and validation accuracy, however there is no major improvement in test accuracy compared to previous one.
    - Rebalancing the classes increased the test accuracy by 3-4%. It is still not able to predict unseen patterns. Validation accuracy is higher than training accuracy.
    - Adding one more Convolution layer has increased test accuracy by additional 3-4%, but adding more feature maps hasn't shown any improvement in the test accuracy.
    - More types of image augmentation techniques needs to be added using say imgaug library, so that it might uncover patterns of test data.
    - More dense layers and convolution layers may help, but since Colab GPU limit has exhausted, training each model variation on local machine is taking couple of hours, couldn't test it further. Also, can test reducing the learning rate might improve on test accuracy.
    - Tried using keras-tuner for Hyperparameter tuning(dropout, learningrate, number of dense layers), however since each trial was taking almost couple of hours, couldn't proceed further on local machine.



<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- numpy, pandas
- matplotlib, seaborn-0.13.2
- keras, Adam optimizer, Dropout, BatchNormalization, L2 Regulizer
- Augmentor
- EarlyStopping
- datetime





<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
