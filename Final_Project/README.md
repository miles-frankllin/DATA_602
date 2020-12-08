![Title](https://github.com/miles-frankllin/DATA_602/blob/master/Final_Project/Notebook_Images/Banner.png)

## Overview
The debate of mask wearing in America has crippled our ability to slow the spread of Covid-19. Tools such as this help businesses operate safely and mitigate spread in their buildings.

## Goals
In this project, I aim to take an existing mask classification project from [Samuel Mohebban](https://github.com/HeeebsInc/FaceMaskEmotionDetection), and enhance the model. In particular, I aim to accomplish one of the future directions in from his project and try improving the prediction accuracy when the person is wearing glasses and a mask. This technique is commonly referred to as transfer learning. It was expected to be a difficult task to find a dataset of this specific class of images, so I opted for a different approach instead. The goal is to continue to train the model on images that have an individual wearing glasses and not a mask, with the hope that it will teach the model that glasses are not an important feature in the classification process. 

## Navigation (Need to link notebooks)

[Technical Notebok](https://github.com/miles-frankllin/DATA_602/blob/master/Final_Project/Notebooks/Technical_Notebook.ipynb) -
[Additional NoteBook](https://github.com/miles-frankllin/DATA_602/blob/master/Final_Project/Notebooks/Data_602_FinalProject_TransferLearning.ipynb) -
[Data (Base Project)](https://github.com/HeeebsInc/FaceMaskEmotionDetection) - 
[Data (Kaggle)](https://www.kaggle.com/aneerbanchakraborty/face-mask-detection-data) - 
[Data - (Kaggle)](https://www.kaggle.com/harry418/dataset-for-mask-detection)

## Requirements
<pre>
Languages    : Python 3.8.3
Tools/IDE    : Google Colab
Libraries    : zipfile, os, pandas, numpy, random, sklearn.model_selection.train_test_split,
               sklearn.metrics.classification_report, sklearn.metrics.confusion_matrix,
               seaborn, shutil, errno tensorflow,  keras_preprocessing.image.ImageDataGenerator
</pre>

## Data
Base Model
<pre>
File Name      : Mobilenet_Masks.h5
URL            : https://github.com/HeeebsInc/FaceMaskEmotionDetection/blob/master/ModelWeights/Mobilenet_Masks.h5
</pre>

Mask Detection
<pre>
URL            : https://www.kaggle.com/milesfranklin/mask-detection
Limitations    : I had previously attempted this project from scratch and scraped the 
                 Shutter Stock Photo [website](https://www.shutterstock.com). Unfortunately,
                 a large portion of the images were unable to be uploaded to be Kaggle,
                 although I have hand labeled all this images from this set and I am 
                 comfortable using these images as a testing set.
Concerns       : N/A
Total Images   : 677
No Mask Images : 175
Mask Images    : 502
</pre>

Glasses or No Glasses
<pre>
URL            : https://www.kaggle.com/jeffheaton/glasses-or-no-glasses
Limitations    : Only contains images of individuals without a mask.
Concerns       : N/A
Total Images   : 5000
No Mask Images : 5000
Mask Images    : 0
</pre>

Face Mask Detection Data
<pre>
URL            : https://www.kaggle.com/aneerbanchakraborty/face-mask-detection-data
Limitations    : N/A
Concerns       : N/A
Total Images   : 3833
No Mask Images : 1918
Mask Images    : 1915
</pre>

Dataset for Mask Detection
<pre>
URL            : https://www.kaggle.com/harry418/dataset-for-mask-detection
Limitations    : N/A
Concerns       : N/A
Total Images   : 1237
No Mask Images : 543
Mask Images    : 694
</pre>



## References

<pre>
URL            : https://github.com/HeeebsInc/FaceMaskEmotionDetection
Author         : Samuel Mohebban
Purpose        : This repository holds the base model used in the transfer learning process.
</pre>
<pre>
URL            : https://github.com/miles-frankllin/Data_603/blob/main/Mask_Classification_CNN.ipynb
Author         : Miles Franklin
Purpose        : This is a previous attempt I made for mask classification before learning about transfer learning. I used this for refernce code and syntax.
</pre>
<pre>
URL            : https://machinelearningmastery.com/how-to-use-transfer-learning-when-developing-convolutional-neural-network-models/
Author         : Jason Brownlee
Purpose        : This was a helpful introduction to transfer learning and understanding how network types of different layers work.
</pre>
<pre>
URL            : https://towardsdatascience.com/transfer-learning-using-mobilenet-and-keras-c75daf7ff299
Author         : Ferhat Culfaz
Purpose        : This was a helpful guide and introduction to transfer learning.
</pre>
