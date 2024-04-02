# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## PROGRAM:
```
DEVELOPED BY:HARINI V
REGISTER NO.:212222230044
```
```python
Convert image to grayscale and remove noise:
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("bridge.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
#### SOBEL X AXIS :
```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
#### SOBEL Y AXIS :
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
#### SOBEL XY AXIS :
```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR:
```py
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

### CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```


## Output:
### SOBEL EDGE DETECTOR:
#### SOBEL X AXIS:
![image](https://github.com/harini1006/EDGE-DETECTION/assets/113497405/d35e60bc-fac4-440b-ab1f-324dbde81aaf)
#### SOBEL Y AXIS:
![image](https://github.com/harini1006/EDGE-DETECTION/assets/113497405/7e626092-b87a-4011-b594-3ff054c6c76a)
#### SOBEL XY AXIS:
![image](https://github.com/harini1006/EDGE-DETECTION/assets/113497405/9439a3ab-6c64-4908-be83-a440e3d0e7f6)

### LAPLACIAN EDGE DETECTOR:
![image](https://github.com/harini1006/EDGE-DETECTION/assets/113497405/ff0b937a-a018-43f1-915d-6b2dbfbe5e35)

### CANNY EDGE DETECTOR:
![image](https://github.com/harini1006/EDGE-DETECTION/assets/113497405/65b777da-56af-4923-8e7d-368f132bdfe6)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
