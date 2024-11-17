# EXP 9 Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image

#### Step5: <br>
Dilate the Image

 ### Program:
##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'HEALTH',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
### Output:

#### Display the input Image
![WhatsApp Image 2024-11-17 at 18 50 29_abde420e](https://github.com/user-attachments/assets/ba0a5212-515d-4682-a04a-4d3d849fb5d2)



#### Display the Eroded Image
![WhatsApp Image 2024-11-17 at 18 50 29_c1656bc7](https://github.com/user-attachments/assets/18bb04dc-2b27-4525-b6dc-59f392cfa9f3)



#### Display the Dilated Image
![WhatsApp Image 2024-11-17 at 18 50 29_f8420cb6](https://github.com/user-attachments/assets/72456000-0afa-4f4d-852c-1020f29087fc)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
