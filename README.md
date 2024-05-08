# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Step1:
Import the necessary packages.
<br>
## Step2:
Create the text image using cv2.putText.
<br>
## Step3:
Then create the structuring image for dilation/erosion.
<br>
## Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.
<br>
## Step5:
Plot the images using plt.imshow.
<br>
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," K.M.Swetha",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')


```
## Output:

### Display the input Image
![image](https://github.com/swethamohanraj/erosion--dilation/assets/94228215/ffd4e1f4-ffa3-465a-94a1-d3d167cf3c44)



### Display the Eroded Image
![image](https://github.com/swethamohanraj/erosion--dilation/assets/94228215/05f473b3-b9d6-48b0-a76e-75b2d916a540)



### Display the Dilated Image
![image](https://github.com/swethamohanraj/erosion--dilation/assets/94228215/d605d0ab-71cd-487e-add4-de5b63767665)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
