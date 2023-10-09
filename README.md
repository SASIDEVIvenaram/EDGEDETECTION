# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.

### Step2:
Read the image and convert the bgr image to gray scale image.
### Step3:
Use any filters for smoothing the image to reduse the noise.

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow

 
## Program:
```
DEVELOPED BY: SASIDEVI V
REG NO : 212222230136
```
# Load the image, Convert to grayscale and remove noise
```
# Import the packages
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("EX78.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR
# SOBEL X AXIS :
```
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
# SOBEL Y AXIS :
```
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
# SOBEL XY AXIS :
```
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
# LAPLACIAN EDGE DETECTOR
```
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
# CANNY EDGE DETECTOR
```
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
### SOBEL EDGE DETECTOR
### SOBEL X AXIS :
![image](https://github.com/SASIDEVIvenaram/EDGEDETECTION/assets/118707332/6db12955-6fdc-407b-b459-67452918ac90)
### SOBEL Y AXIS :
![image](https://github.com/SASIDEVIvenaram/EDGEDETECTION/assets/118707332/009ef61c-bf76-4a6c-9009-3d779a3f1b7b)
### SOBEL XY AXIS :
![image](https://github.com/SASIDEVIvenaram/EDGEDETECTION/assets/118707332/2429c482-8807-4604-8248-a98ff98b0d2b)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/SASIDEVIvenaram/EDGEDETECTION/assets/118707332/3913ad45-0358-4c2f-ab91-91239caaf7f9)

### CANNY EDGE DETECTOR
![image](https://github.com/SASIDEVIvenaram/EDGEDETECTION/assets/118707332/49a017b2-e2bd-42d2-a618-fcc350697bb2)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
