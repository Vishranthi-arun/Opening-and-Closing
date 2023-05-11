# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

<br>


### Step2:
Create the Text using cv2.putText.

<br>

### Step3:
Create the structuring element.

<br>

### Step4:
Use Opening and Closing operation.

<br>

### Step5:
Print the output and end the program.

<br>

 
## Program:
```
Develped by : Vishranthi A
Reg no.: 212221230124
```
``` Python
# Import the necessary packages
import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Vishranthi A",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("ORIGINAL IMAGE")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
open_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("OPENING")
plt.imshow(open_image)
plt.axis('off')

# Use Closing Operation
close_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("CLOSING")
plt.imshow(close_image)
plt.axis('off')
```
## Output:

### Display the input Image
<br>
<br>
<br>

![image](https://github.com/Vishranthi-arun/Opening-and-Closing/assets/93427278/031039e6-0db1-4db7-8e6d-b157ba333efb)


<br>
<br>
<br>

### Display the result of Opening
<br>
<br>
<br>

![image](https://github.com/Vishranthi-arun/Opening-and-Closing/assets/93427278/9dd9fd22-4874-4c21-8ac2-331677d5763b)

<br>
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>

![image](https://github.com/Vishranthi-arun/Opening-and-Closing/assets/93427278/8b55205b-a10d-4040-bbe8-969bda9eeea5)

<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
