# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION
### Name : VIJAY K
### Reg No : 212224240182
# Aim
To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

1.Image Erosion
2.Image Dilation
# Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
# Algorithm
# Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

# Step 2:
Create a blank image using NumPy.

# Step 3:
Insert text onto the image using OpenCV's text drawing function.

# Step 4:
Display the original image.

# Step 5:
Create a structuring element (kernel) of suitable size.

# Step 6: Image Erosion
Apply the erosion operation using the created kernel.
Remove pixels from the boundaries of foreground objects.
Display the eroded image.
# Step 7: Image Dilation
Apply the dilation operation using the same kernel.
Add pixels to the boundaries of foreground objects.
Display the dilated image.
# Step 8:
Compare the original, eroded, and dilated images.


# PROGRAM:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'THALAPATHY', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
```
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```

# OUTPUT:
<img width="389" height="410" alt="download" src="https://github.com/user-attachments/assets/8911cd9f-3861-48b4-b42f-21dc0e66996d" />

<img width="389" height="410" alt="download" src="https://github.com/user-attachments/assets/e342711b-44e5-4913-90b5-54d9d972f75c" />


<img width="389" height="410" alt="download" src="https://github.com/user-attachments/assets/d5a6a06a-806e-4dc8-9704-37d554f756b2" />


# RESULT:
Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV.
