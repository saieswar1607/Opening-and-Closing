# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the required packages.


### Step2:

Create the input image.

### Step3:

Create the structuring element.

### Step4:

Apply opening operation.

### Step5:

Apply closing operation. 

 
## Program:

``` Python
# Import necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
im=cv2.putText(img1,' ESWAR ',(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Input Image",im)

# Create the structuring element

Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
cv2.imshow("Opening Image",image1)

# Use Closing Operation

image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
cv2.imshow("Closing Image",image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image

<img width="502" alt="1" src="https://user-images.githubusercontent.com/93427011/175801161-ba5ba062-bd9b-4e2c-9843-d881d9ab2e35.png">


### Display the result of Opening

<img width="502" alt="2" src="https://user-images.githubusercontent.com/93427011/175801170-b501d6e1-4c18-4e0e-ab7f-0f6f674e46a2.png">


### Display the result of Closing

<img width="502" alt="3" src="https://user-images.githubusercontent.com/93427011/175801176-03de36dd-2d46-4822-9951-610e6e7b0312.png">


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
