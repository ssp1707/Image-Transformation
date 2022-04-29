# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using
M=np.float32([[1,0,20],[0,1,50],[0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step3:
Scale the image using
M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
Shear the image using
M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step5:
Reflection of image can be achieved through the code
M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step 6:
Rotate the image using<br>
angle=np.radians(45)<br>
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])<br>
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step 7:
Crop the image using <br>
cropped_img=input_img[20:150,60:230]

### Step 8:
Display all the Transformed images.


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
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```

## iv)Image Reflection
```
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```

## v)Image Rotation
```
angle=np.radians(25)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```

## vi)Image Cropping
```
cropped_img=input_image[20:100,10:200]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```

## Output:
### i)Image Translation

![EXPT 5 1](https://user-images.githubusercontent.com/75234965/165884776-37258744-7e64-4390-ac11-8703394ba1c1.PNG)

### ii) Image Scaling

![EXPT 5 2](https://user-images.githubusercontent.com/75234965/165884786-8abb73df-c694-4856-8c05-fef0930b5a41.PNG)

### iii)Image shearing

![EXPT 5 3](https://user-images.githubusercontent.com/75234965/165884793-00fb2552-b6a1-423c-8110-d89ff5d4b207.PNG)

### iv)Image Reflection

![EXPT 5 4](https://user-images.githubusercontent.com/75234965/165884798-8832686c-244d-43a3-b2f9-233b521277e8.PNG)

### v)Image Rotation

![EXPT 5 5](https://user-images.githubusercontent.com/75234965/165884801-8aaecc90-4514-4773-9fe4-5f43302703f2.PNG)

### vi)Image Cropping
![EXPT 5 6](https://user-images.githubusercontent.com/75234965/165884804-14875fe8-fc90-4c3a-9b94-f5a2c32a0b9b.PNG)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
