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
import numpy as np
import matplotlib.pyplot as plt
import cv2
~~~
~~~
text_image = np.zeros((100,850),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"joans",(130,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')
~~~
~~~
kernel = cv2.getStructuringElement(cv2.MORPH_ELLIPSE,(5,11))
~~~
~~~
opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')
~~~
~~~
closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')
~~~
## Output:

### Display the input Image
![](a1.png)

### Display the result of Opening
![](a2.png)

### Display the result of Closing
![](a3.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
