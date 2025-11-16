# EXP NO - 8: THRESHOLDING
### NAME : LOKESHWARAN.R
### REG NO : 212224220053


## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:

Load the necessary packages.
### Step2:
Read the Image and convert to grayscale

### Step3:
Read the Image and convert to grayscale

### Step4:
Use Adaptive thresholding to segment the image

### Step5:

Use Adaptive thresholding to segment the image
## Program

```python

EXP NO - 4 : THRESHOLDING
 NAME : LOKESHWARAN.R
 REG NO : 242224220053
# Load the necessary packages


import numpy as np
import matplotlib.pyplot as plt
import cv2


# Read the Image and convert to grayscale

image = cv2.imread("disney.jpg",1)
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
image_gray = cv2.imread("disney.jpg",0)


# Use Global thresholding to segment the image


ret,thresh_img1=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(image_gray,100,255,cv2.THRESH_TRUNC)

# Use Adaptive thresholding to segment the image


thresh_img7=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img8=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)

# Use Otsu's method to segment the image 

ret,thresh_img6=cv2.threshold(image_gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)


# Display the results





```
## Output

### Original Image
```


plt.axis("off")
plt.title("Original Image")
plt.imshow(image)


```

<img width="833" height="367" alt="image" src="https://github.com/user-attachments/assets/25fa8eb3-f5ef-4cd9-86a9-476060e1efd2" />


### Global Thresholding

<img width="827" height="405" alt="image" src="https://github.com/user-attachments/assets/0d8d5bc6-3bfa-49d1-a172-dcd0f213c3ad" />

<img width="822" height="382" alt="image" src="https://github.com/user-attachments/assets/49f479f2-55fb-4ffd-8a0d-fe7fcb998d8a" />

<img width="848" height="387" alt="image" src="https://github.com/user-attachments/assets/819bddad-78cc-4314-bbce-3ebde0dc38ba" />

<img width="851" height="350" alt="image" src="https://github.com/user-attachments/assets/7d883825-6054-47e8-999f-2136ac751cac" />



### Adaptive Thresholding


<img width="587" height="516" alt="image" src="https://github.com/user-attachments/assets/cd874203-633a-4347-a1bb-42fd95fa247e" />


<img width="600" height="545" alt="image" src="https://github.com/user-attachments/assets/b45d8db0-f5f5-4f4a-82e3-32c940b64708" />

### Optimum Global Thesholding using Otsu's Method

<img width="565" height="546" alt="image" src="https://github.com/user-attachments/assets/55ac9665-24ee-4df3-b7fd-c5e81527e007" />


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
