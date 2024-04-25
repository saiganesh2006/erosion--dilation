# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText


### Step3:
Create the structuring element


### Step4:
Erode the image

### Step5:
Dilate the Image


 
## Program:
### DEVELOPED BY : D.B.V. SAI GANESH
### REGISTER NO: 212223240025
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'SAI GANESH',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')


# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')






```
## Output:

### Display the input Image
![image](https://github.com/saiganesh2006/erosion--dilation/assets/145742342/efb72025-0488-4bae-9c26-410658e4a861)


### Display the Eroded Image
![image](https://github.com/saiganesh2006/erosion--dilation/assets/145742342/2f187065-3b7f-47d2-8322-2f1f1896e688)


### Display the Dilated Image
![image](https://github.com/saiganesh2006/erosion--dilation/assets/145742342/dd5f421a-3744-45fe-a893-8f87cb36333f)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
