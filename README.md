 EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using plt.erode and plt.dilate.

### Step5:
Plot the images using plt.imshow.

## Program:
```
Developed by : JAYASRI DODDA
Register no: 212222240028
```
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
image = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"Jayasri D",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Create the structuring element
```python
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Erode the image
```python
image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Dilate the image
```python
image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:

### Display the input Image
![Screenshot from 2023-10-11 11-26-28](https://github.com/jayasridodda/EROSION-AND-DILATION/assets/123259278/2d5e735a-1f95-41cc-8186-e21f0007e73d)

### Display the Eroded Image
![Screenshot from 2023-10-11 11-26-48](https://github.com/jayasridodda/EROSION-AND-DILATION/assets/123259278/51d9c1c2-5a97-4107-99b1-8b24b7fac152)

### Display the Dilated Image
![Screenshot from 2023-10-11 11-26-59](https://github.com/jayasridodda/EROSION-AND-DILATION/assets/123259278/92a228c7-431b-44e1-b746-a77b45a60d2b)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
