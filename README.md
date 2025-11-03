# THRESHOLDING

### DEVELOPED BY : PRAVESH N
### REG NO: 212223230154

## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:

Load the necessary packages.

### Step2:

Read the Image and convert to grayscale.


### Step3:

Use Global thresholding to segment the image.

### Step4:

Use Adaptive thresholding to segment the image.

### Step5:

Use Otsu's method to segment the image and display the results.

## Program



# Load the necessary packages
```py
# DEVELOPED BY : PRAVESH N
# REG NO : 212223230154

import cv2
import matplotlib.pyplot as plt
```




# Read the Image and convert to grayscale
```py
image=cv2.imread('beaut.jpg')
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
# Original image
```py
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

# Use Global thresholding to segment the image
```py
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)
```



# Use Adaptive thresholding to segment the image
```py
adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```



# Use Otsu's method to segment the image 
```py
_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```



# Global Thresholding

```py
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
# Adaptive Thresholding
```py
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
# Otsu's Method
```py
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
# Show the plot
```py
plt.tight_layout()
plt.show()
```
## Output

### Original Image

<img width="299" height="170" alt="Screenshot 2025-10-23 203918" src="https://github.com/user-attachments/assets/2a0b26b0-42b0-4350-bc9e-702909ac80a4" />



### Global Thresholding

<img width="297" height="172" alt="Screenshot 2025-10-23 204105" src="https://github.com/user-attachments/assets/a67017f0-bbb5-43d1-bd82-db3b55f53a57" />


### Adaptive Thresholding


<img width="299" height="175" alt="Screenshot 2025-10-23 204122" src="https://github.com/user-attachments/assets/a54de0d4-ba6c-47a2-81ec-78984e15b67f" />



### Optimum Global Thesholding using Otsu's Method

<img width="280" height="167" alt="Screenshot 2025-10-23 204152" src="https://github.com/user-attachments/assets/d09e7691-f16a-4b3c-991f-4a3b4d4cabb3" />


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
