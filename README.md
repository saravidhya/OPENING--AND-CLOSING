# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1 :

Import the necessary packages

### Step 2 :

Create the Text using cv2.putText

### Step 3 :

Create the structuring element

### Step 4 :

Use Opening operation

### Step 5 :

Use Closing Operation

 
## Program:

```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Kavinraja D",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))

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

### Display the input Image :

![image](https://github.com/user-attachments/assets/d9b60430-ec54-4fa5-8e93-5bd89c129a13)




### Display the result of Opening :


![image](https://github.com/user-attachments/assets/7996f7f3-3d37-4b36-b4d1-eb393bc40484)


### Display the result of Closing :


![image](https://github.com/user-attachments/assets/4f34ca2c-2834-4f7c-9d5b-1f98aef0038a)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
