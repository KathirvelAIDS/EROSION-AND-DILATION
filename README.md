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
![image](https://github.com/PERARASU10/EROSION-AND-DILATION/assets/118348589/e5703e5a-27dd-458c-aadf-f50f71808a19)



### Display the Eroded Image
![image](https://github.com/PERARASU10/EROSION-AND-DILATION/assets/118348589/3dd5ded5-2105-416f-bbbc-9dd54f0af116)

![image](https://github.com/PERARASU10/EROSION-AND-DILATION/assets/118348589/794c1709-12ca-45bd-b651-bfda53d4a6e2)


### Display the Dilated Image

![image](https://github.com/PERARASU10/EROSION-AND-DILATION/assets/118348589/10dd4283-9943-4b71-b5d2-5e61e8ca11ae)

![image](https://github.com/PERARASU10/EROSION-AND-DILATION/assets/118348589/b97d3589-9eb1-4d5e-8ca7-e446c7cbf7db)


## Result
Thus the generated text image is eroded and dilated using Python and OpenCV.
