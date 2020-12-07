# Problem Statement
The debate of mask wearing in America has crippled our ability to slow the spread of Covid-19. Tools such as this help businesses operate safely and mitigate spread in their buildings.

In this project, I aim to take an existing mask classification project from [Samuel Mohebban](https://github.com/HeeebsInc/FaceMaskEmotionDetection), and enhance the model to better predict when the person is wearing glasses. This technique is commonly referred to as transfer learning.

# Data

## Base Model
<pre>
File Name      : Mobilenet_Masks.h5
URL            : https://github.com/HeeebsInc/FaceMaskEmotionDetection/blob/master/ModelWeights/Mobilenet_Masks.h5
Limitations    : 5000 images of individuals with or without glasses
</pre>

## Mask Detection
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

## Glasses or No Glasses
<pre>
URL            : https://www.kaggle.com/jeffheaton/glasses-or-no-glasses
Limitations    : 5000 images of individuals with or without glasses
Concerns       : N/A
Total Images   : 5000
No Mask Images : 5000
Mask Images    : 0
</pre>
