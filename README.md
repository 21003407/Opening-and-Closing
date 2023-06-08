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
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening and Closing Operations

### Step5:
End Program.

## Program:
~~~
Developed by: Anusha R
register number: 212221230006
~~~
``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Anusha",(5,70),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element

kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation

img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation

img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

### Display the input Image

![11a](https://github.com/Anusha-Rajarajan/Opening-and-Closing/assets/93427472/0689f2fb-797a-44d5-b0a4-d0684406c66f)


### Display the result of Opening

![11b](https://github.com/Anusha-Rajarajan/Opening-and-Closing/assets/93427472/6c351287-2e1e-4de3-8f98-6e68e7625c0c)

### Display the result of Closing

![11c](https://github.com/Anusha-Rajarajan/Opening-and-Closing/assets/93427472/ce25dcdd-9fad-4a5b-927a-b6c72818b314)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
