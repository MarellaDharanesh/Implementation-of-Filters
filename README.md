# Implementation-of-Filters
## AIM:
To implement filters for smoothing and sharpening the images in the spatial domain.
## SOFTWARE REQUIRED:
Anaconda - Python 3.7
## ALGORITHM:
### Step 1:
Import the necessary modules. 
### Step 2:
For performing smoothing operation on a image. 
- Average filter
```python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
```
- Weighted average filter
```python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
```
- Gaussian Blur 
```python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
```
- Median filter
```python
median=cv2.medianBlur(image2,13)
```
### Step 3:
For performing sharpening on a image.
- Laplacian Kernel
```python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
```
- Laplacian Operator
```python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
```
### Step 4:
Display all the images with their respective filters.
## PROGRAM:
```python
# Developed By   : Marella Dharanesh
# Register Number: 212222240062

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("bts.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
### 1. Smoothing Filters
i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
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
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
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
iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```
### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
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
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
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

i) Using Averaging Filter


![exppic1](https://user-images.githubusercontent.com/118707669/230024421-57318d25-7c84-44d6-a482-9093f98a90b0.png)



ii) Using Weighted Averaging Filter


![exppic2](https://user-images.githubusercontent.com/118707669/230024388-9430dd8b-9d7f-43d2-ac77-484f635ba9be.png)



iii) Using Gaussian Filter

![exppic3](https://user-images.githubusercontent.com/118707669/230024360-b7d6c2fe-aa58-4b75-a450-ade5b9a311b6.png)



iv) Using Median Filter


![exppic4](https://user-images.githubusercontent.com/118707669/230024331-1ed92c15-0ad9-4d2f-98e0-46a2e2238fc8.png)



### 2. Sharpening Filters

i) Using Laplacian Kernal



![exppic5](https://user-images.githubusercontent.com/118707669/230024216-16505f86-c8dc-44a4-b8a0-59b52d696dd5.png)


ii) Using Laplacian Operator
![exppic6](https://user-images.githubusercontent.com/118707669/230024254-2947a1d9-d3f8-4f72-8a12-8b78b5746320.png)





## RESULT:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
