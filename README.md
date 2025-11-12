
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:

Create the structuring element.
### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:
### DEVELOPED BY: SHYAM KUMAR E
### REGISTER NO: 212223230207

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'SHYAM KUMAR', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```
## Output:

### Display the input Image
<img width="676" height="145" alt="Screenshot 2025-11-12 134859" src="https://github.com/user-attachments/assets/66d89bce-f797-4763-b188-dbd8b4adbe12" />




### Display the result of Opening
<img width="668" height="150" alt="Screenshot 2025-11-12 134906" src="https://github.com/user-attachments/assets/4dee6820-a7d9-48b1-bdd2-fe6b3bb3d6dc" />




### Display the result of Closing
<img width="646" height="154" alt="Screenshot 2025-11-12 134913" src="https://github.com/user-attachments/assets/5c89f547-f8e8-41a3-8149-922a613a13a7" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
