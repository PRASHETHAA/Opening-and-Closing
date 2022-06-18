# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

<br><br><br><br><br>

## PROGRAM:
```
/*
Developed by   : PRASHETHAA R
Register Number: 212220230036
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Prashe',(5,70),font,2,(255),5,cv2.LINE_AA)
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
## OUTPUT:

### Display the input Image

![p1](https://user-images.githubusercontent.com/75234942/171095333-314671dd-43be-4fbf-8836-f28f1bbc3cf9.png)


### Display the result of Opening

![p2](https://user-images.githubusercontent.com/75234942/171095365-208168da-5810-4979-8479-40c83842cd66.png)

### Display the result of Closing

![p3](https://user-images.githubusercontent.com/75234942/171095390-7e367523-8db9-4270-a475-4dae4934abce.png)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
