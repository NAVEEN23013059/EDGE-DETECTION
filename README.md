# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## DEVOLOPED BY : S.NAVEEN
## REGISTER NUMBER: 212223240106
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
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('court.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)

laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

canny_edges = cv2.Canny(gray_image, 50, 150)

plt.figure(figsize=(12, 12))

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

plt.figure(figsize=(10, 10))
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Combined Edges')
plt.axis('off')

plt.figure(figsize=(10, 10))
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edges')
plt.axis('off')

plt.figure(figsize=(10, 10))
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edges')
plt.axis('off')



plt.tight_layout()
plt.show()

```
## Output:
## ORIGINAL IMAGE:
![image](https://github.com/user-attachments/assets/58e96298-af19-4978-915f-f039ac352d37)


### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/c5033945-2c5b-4f62-a4f4-e90f88bf0dac)



### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/7221f36f-6d60-4287-aa5e-412d56247ac7)


### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/4f6ca649-39ee-4aa2-89aa-bf0f802d4c0f)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
