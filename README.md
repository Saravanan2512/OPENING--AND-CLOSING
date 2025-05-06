# OPENING--AND-CLOSING

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Load the input image using cv2.imread().

### Step2:

Define a structuring element (e.g., 5x5 rectangular) using cv2.getStructuringElement().


### Step3:

Perform erosion followed by dilation using cv2.morphologyEx() with the cv2.MORPH_OPEN operation.


### Step4:

Perform dilation followed by erosion using cv2.morphologyEx() with the cv2.MORPH_CLOSE operation.


### Step5:

Use plt.subplot() to show the original, opening, and closing images side by side.


 
## Program:

``` 
import cv2
import numpy as np
import matplotlib.pyplot as plt
#i) Create the Text using cv2.putText
img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"SARAVANAN",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()
#ii) Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
#iii) Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()
#iv) Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image

![Screenshot 2025-05-06 094857](https://github.com/user-attachments/assets/21037f49-02b5-4a9c-b438-87a68a211fb9)



### Display the result of Opening
![Screenshot 2025-05-06 094906](https://github.com/user-attachments/assets/603f44a3-2907-420f-8291-8b6a87a36e45)


### Display the result of Closing
![Screenshot 2025-05-06 093207](https://github.com/user-attachments/assets/4dd68c51-4114-409e-9976-412e81031d50)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
