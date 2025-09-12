# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import the required libraries.


### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.
## Program:
```
 Developed By   :Farhana H
 Register Number:212223230057
```

### 1. Smoothing Filters

## i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Imgage2.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()



```
## ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
## iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()




```
## iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
## i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()





```
## ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters


## i) Using Averaging Filter
<img width="903" height="305" alt="Screenshot 2025-09-12 211255" src="https://github.com/user-attachments/assets/d855f4d5-9467-4f9f-b7c1-41f5d2603424" />


## ii)Using Weighted Averaging Filter
<img width="664" height="231" alt="Screenshot 2025-09-12 211301" src="https://github.com/user-attachments/assets/23ce52b7-c1ea-46c4-b594-0f7bc5a0091e" />


## iii)Using Gaussian Filter

<img width="671" height="226" alt="Screenshot 2025-09-12 211306" src="https://github.com/user-attachments/assets/114731a4-9d03-45ca-8fb5-4b679dde10c4" />

## iv) Using Median Filter

<img width="908" height="307" alt="Screenshot 2025-09-12 211314" src="https://github.com/user-attachments/assets/7e1da133-d31d-42b2-8115-7717458d76eb" />

### 2. Sharpening Filters


## i) Using Laplacian Kernal

<img width="667" height="226" alt="Screenshot 2025-09-12 211319" src="https://github.com/user-attachments/assets/91bd2c7c-2ff2-4c1f-8784-ccb3c30d2194" />

## ii) Using Laplacian Operator
<img width="662" height="227" alt="Screenshot 2025-09-12 211326" src="https://github.com/user-attachments/assets/348345dd-45b1-47e9-a516-bb66c994d9d4" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
