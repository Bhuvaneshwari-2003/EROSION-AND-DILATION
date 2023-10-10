# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
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
Erode and Dilate the image.

### Step5:
End the Program.
 
## Program:
```
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Load the Image
img1=np.zeros((100,450),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
# Create the Text using cv2.putText
cv2.putText(img1,' PRISON BREAK ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()
# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()


```

## Output:

### Display the input Image
![image](https://github.com/Bhuvaneshwari-2003/EROSION-AND-DILATION/assets/94828604/0f38308c-39bf-468b-ad0d-545d7660b025)



### Display the Eroded Image
![image](https://github.com/Bhuvaneshwari-2003/EROSION-AND-DILATION/assets/94828604/37f1c1c4-11c3-4fee-96b3-00fbe2485212)


### Display the Dilated Image
![image](https://github.com/Bhuvaneshwari-2003/EROSION-AND-DILATION/assets/94828604/a2f17c80-55a2-447e-b436-42efb8b4176e)



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
