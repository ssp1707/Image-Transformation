# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:

## Developed By: S. Sanjna Priya
## Register Number:212220230043

## i)Image Translation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('simp.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show
rows,cols,dim=input_image.shape
input_image.shape
M=np.float32([[1,0,25],
             [0,1,100],
             [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show
```

## ii) Image Scaling
```
M=np.float32([[1.5,0,0],
             [0,1.8,0],
             [0,0,1]])
scaled_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show
```

## iii)Image shearing
```

```


iv)Image Reflection




v)Image Rotation




vi)Image Cropping






## Output:
### i)Image Translation
<br>
<br>
<br>
<br>

### ii) Image Scaling
<br>
<br>
<br>
<br>


### iii)Image shearing
<br>
<br>
<br>
<br>


### iv)Image Reflection
<br>
<br>
<br>
<br>



### v)Image Rotation
<br>
<br>
<br>
<br>



### vi)Image Cropping
<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
