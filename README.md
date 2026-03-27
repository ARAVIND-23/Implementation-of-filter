# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Using Averaging Filter
</br> 

### Step2
</br>
Using Weighted Averaging Filter
</br> 

### Step3
</br>
Using Gaussian Filter
</br> 

### Step4
</br>
Using Median Filter
</br> 

### Step5
</br>
Using Laplacian Kernal
</br>

### Step6
</br>
Using Laplacian Operator
</br> 

## Program:
### Developed By   :  ARAVIND G
### Register Number: 212223240011
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("rose.png")
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
ii) Using Weighted Averaging Filter
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
iii) Using Gaussian Filter
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
iv)Using Median Filter
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
i) Using Laplacian Linear Kernal
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
ii) Using Laplacian Operator
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
</br>

i) Using Averaging Filter
</br>
</br>
<img width="830" height="245" alt="image" src="https://github.com/user-attachments/assets/2b7070aa-99ac-4168-be35-164124046be0" />
</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br>
<img width="627" height="197" alt="image" src="https://github.com/user-attachments/assets/e6eee03d-33a7-4808-a570-cb1b278ccf31" />

</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
<img width="577" height="187" alt="image" src="https://github.com/user-attachments/assets/9ac20215-6695-48ba-b0ba-636cbf0959d5" />

</br>
</br>

iv) Using Median Filter
</br>
</br>
<img width="801" height="247" alt="image" src="https://github.com/user-attachments/assets/af1575a2-4aa0-42ac-9a93-33e332a6ef61" />


</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
<img width="588" height="187" alt="image" src="https://github.com/user-attachments/assets/c9201ee0-3d75-4e9b-ab13-7d709d2da760" />


</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
<img width="562" height="186" alt="image" src="https://github.com/user-attachments/assets/72cfed29-ad42-4c60-a136-bebaa01df625" />


</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
