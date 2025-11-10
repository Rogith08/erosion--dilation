# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages

### Step2:
create the text using cv2.put Text

### Step3:
create the structuting element

### Step4:
Erodde the image

### Step5:
Dilate the image

## Program:

## DEVELOPED BY:ROGITH. K
## REG NO:212223110042
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'ROGITH. K', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)

# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image
<img width="468" height="502" alt="Screenshot 2025-11-10 103229" src="https://github.com/user-attachments/assets/35b730be-1972-448d-a1f4-498bac18db02" />



### Display the Eroded Image
<img width="464" height="496" alt="Screenshot 2025-11-10 103237" src="https://github.com/user-attachments/assets/1826d9d8-4d10-4835-9afd-1ee9e395b4ba" />



### Display the Dilated Image
<img width="460" height="499" alt="Screenshot 2025-11-10 103247" src="https://github.com/user-attachments/assets/3f5a8672-2999-4ed8-a005-801ba8ec741f" />




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
