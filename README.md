# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:

``` Python
Developed by :YASHASWI.M 
Register Number: 212220230062
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'YASHASWI.M',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()



# Create the structuring element

kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation

image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation

image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()



```
## Output:

### Display the input Image
![DIP 11-1](https://github.com/yashaswimitta/Opening-and-Closing/assets/94619247/253ae05d-cf03-4415-8dd4-d43f194b7af6)

### Display the result of Opening
![DIP 11-2](https://github.com/yashaswimitta/Opening-and-Closing/assets/94619247/3eb9f468-2d6f-44c4-aab5-a0ab53a06169)


### Display the result of Closing
![DIP 11-3](https://github.com/yashaswimitta/Opening-and-Closing/assets/94619247/60f45fd0-c8d4-456a-be20-389638a273bf)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
