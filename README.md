# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary packages

### Step2:
Create an empty window and add text to it
### Step3:
create a structuring element

### Step4:
Do the operation

### Step5:
Show the output image

 
## Program:
```
NAME:KATHIRVEL.A
REG NO:212221230047
```

``` Python
# Import the necessary packages
import cv2
import numpy as np


# Create the Text using cv2.putText

img= np.zeros((350,1400),dtype ='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'THALAPATHY',(15,200),font,5,(255),10,cv2.LINE_AA)
cv2.imshow('created_text',img)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element



# Erode the image

erode1= np.ones((5,5),np.uint8)
erode2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

image_erode1 = cv2.erode(img,erode1)
cv2.imshow('Eroded_image_1',image_erode1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_erode2 = cv2.erode(img,erode2)
cv2.imshow('Eroded_image_2',image_erode2)
cv2.waitKey(0)
cv2.destroyAllWindows()


# Dilate the image


dilate1= np.ones((5,5),np.uint8)
dilate2 = cv2.getStructuringElement(cv2.MORPH_CROSS,(12,12))

image_dilate1 = cv2.dilate(img,dilate1)
cv2.imshow('Dilated_image_1',image_dilate1)
cv2.waitKey(0)
cv2.destroyAllWindows()
image_dilated2 = cv2.dilate(img,dilate2)
cv2.imshow('Dilated_image_2',image_dilated2)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:

### Display the input Image
![Screenshot_20231107_132842](https://github.com/KathirvelAIDS/EROSION-AND-DILATION/assets/94911373/54ad6b91-85ac-4154-8b0d-ca3510671c49)




### Display the Eroded Image
![Screenshot_20231107_132852](https://github.com/KathirvelAIDS/EROSION-AND-DILATION/assets/94911373/c65f7e15-9c30-4dc6-bce3-4b84a30dbbf7)



### Display the Dilated Image
![Screenshot_20231107_132906](https://github.com/KathirvelAIDS/EROSION-AND-DILATION/assets/94911373/0c1bcfb5-016c-4e44-a744-f51dfb349507)



## Result
Thus the generated text image is eroded and dilated using Python and OpenCV.
