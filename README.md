
# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.

 
## Program:

```
# Developed By: Swaminathan.V
# Register No: 212223110057

import cv2
import numpy as np
import matplotlib.pyplot as plt


image = np.zeros((500, 500, 3), dtype=np.uint8)


font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Swaminathan. V', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)


plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')


kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)

plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')

dilated_image = cv2.dilate(image, kernel, iterations=1)


plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')





```
## Output:

### Display the input Image:


![image](https://github.com/user-attachments/assets/e79cd36a-b515-4d1d-9b7d-d2c6cb70101b)




### Display the Eroded Image:

![image](https://github.com/user-attachments/assets/4a48d66f-29a7-447a-89da-5ed80ddc346a)




### Display the Dilated Image:

![image](https://github.com/user-attachments/assets/dfe8a326-44e1-453d-9a79-a04bae8c9c0c)







## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
