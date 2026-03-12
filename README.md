# Exp-9-Implementation-of-Erosion-and-Dilation
## Name : Kishore S M
## Reg No : 212224230131
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

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
# Create a blank image
image = np.zeros((500, 600, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'kishore', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Erode the image


# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

# Dilate the image
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')




```
## Output:

### Display the input Image
<br>
<br>
<br><img width="1111" height="553" alt="image" src="https://github.com/user-attachments/assets/90dc2996-79f9-45da-add5-15b8623e6575" />

<br>
<br>
<br>

### Display the Eroded Image
<br>
<br><img width="892" height="658" alt="image" src="https://github.com/user-attachments/assets/edb38e5a-f17a-4d85-af42-a11504fed99e" />

<br>
<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<br>
<br><img width="1015" height="610" alt="image" src="https://github.com/user-attachments/assets/c606415a-6c41-4635-80cb-38e6788babc7" />

<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
