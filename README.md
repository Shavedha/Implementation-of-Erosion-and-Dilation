# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages

### Step 2:
Create the text image using cv2.putText.

### Step 3:
Then create the structuring image for dilation/erosion.

### Step 4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step 5:
Plot the images using plt.imshow.

 ## Program:

``` 
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,560),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Shavedha Y ",(5,70),font,2,(255),5,cv2.LINE_AA)
# cv2.imshow("nameimg",text_image)
# cv2.waitKey(0)
# cv2.destroyAllWindows()
plt.title("Original Image")
plt.imshow(text_image,'RdGy_r')
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'RdGy_r')
plt.axis('off')

# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'RdGy_r')
plt.axis('off')

```
## Output:

### Display the input Image
<img width="395" alt="image" src="https://user-images.githubusercontent.com/93427376/235285260-9279a4e0-8238-46c0-8eca-6f687652fedb.png">

### Display the Eroded Image
<img width="412" alt="image" src="https://user-images.githubusercontent.com/93427376/235285274-9395c98c-3bc6-44f3-b3d5-730077860fce.png">

### Display the Dilated Image
<img width="406" alt="image" src="https://user-images.githubusercontent.com/93427376/235285281-14b3f211-c3dc-42c0-8a62-802c829d050a.png">

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
