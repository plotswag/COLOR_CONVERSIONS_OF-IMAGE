# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
	Draw a line from the top-left to the bottom-right of the image.
	Draw a circle at the center of the image.
	Draw a rectangle around a specific region of interest in the image.
	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
	Convert the image from RGB to HSV and display it.
	Convert the image from RGB to GRAY and display it.
	Convert the image from RGB to YCrCb and display it.
	Convert the HSV image back to RGB and display it.

### Step4:
	Access and print the value of the pixel at coordinates (100, 100).
	Modify the color of the pixel at (200, 200) to white.

### Step5:
	Resize the original image to half its size and display it.
### Step6:
	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
	Flip the original image horizontally and display it.
	Flip the original image vertically and display it.
### Step8:
	Save the final modified image to your local directory.
```
Developed By: Jeevanesh S
Register Number: 212222243002
```
# Program:

### 1)Read and Display an Image

```Python
import cv2
image=cv2.imread('lokesh.jpeg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
 

### OUTPUT:

![Screenshot 2024-09-10 115034](https://github.com/user-attachments/assets/33f69471-5b33-48cb-a628-064e33974e71)


 

### 2.) Draw Shapes and Add Text:
i)Draw a line from the top-left to the bottom-right of the image.

```Python
import cv2
img = cv2.imread("lokesh.JPEG")
img=cv2.resize(img,(600,800))
res = cv2.line(img, (0, 0), (599, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>


### OUTPUT:

![Screenshot 2024-09-10 115108](https://github.com/user-attachments/assets/5e3b57e8-b677-4bdf-b2c7-706f157d2b0f)



 
### ii)Draw Shapes and Add Text
```Python
import cv2

# Load the image
img = cv2.imread("lokesh.JPEG")
img1=cv2.resize(img,(600,800))


# Get the dimensions of the image
height, width, _ = img1.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img1, center_coordinates, 150, (255, 0, 0), 10)

# Display the image with the circle
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>


### OUTPUT:
![Screenshot 2024-09-10 115130](https://github.com/user-attachments/assets/161a5b68-8db9-4de9-92c0-8bbe813f6ea8)



      
### iii)Draw a rectangle around a specific region of interest in the image.
```Python

import cv2

img = cv2.imread("lokesh.JPEG")
img1=cv2.resize(img,(600,800))
start=(0,0)
stop=(409,529)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img1,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
 <br>
 <br>

### OUTPUT:

![Screenshot 2024-09-10 115231](https://github.com/user-attachments/assets/d5b7cca5-5c21-4921-b467-4643f8f0441a)



      
### iv)Add the text "OpenCV Drawing" at the top-left corner of the image.

 ```Python
import cv2

# Load the image
img = cv2.imread("lokesh.JPEG")
img1=cv2.resize(img,(600,800))


# Define the text to be added and its position
text = "OPENCV DRAWING"
position = (50, 50)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img1, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>

    
### OUTPUT:

![Screenshot 2024-09-10 115251](https://github.com/user-attachments/assets/e411fa99-abb4-4d1b-8659-d42ef043f9a3)



### 3)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpg',1)

img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### OUTPUT:
![Screenshot 2024-09-10 115318](https://github.com/user-attachments/assets/7dc574b7-812c-4ab5-aea9-2d58d45e6bf4)

#### ii.)Convert the image from RGB to GRAY and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpeg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output:
![Screenshot 2024-09-10 115342](https://github.com/user-attachments/assets/6f3dd83f-95e2-43c7-9613-21d91ac95228)


#### iii.)Convert the image from RGB to YCrCb and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpeg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:
![Screenshot 2024-09-10 115342](https://github.com/user-attachments/assets/882cb5bb-4694-49fe-9b5e-78c74ab0a4d1)

#### iv.)Convert the HSV image back to RGB and display it.
```Python
import cv2
img = cv2.imread('lokesh.jpeg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115430](https://github.com/user-attachments/assets/849ca599-dd6a-45df-8592-a81061ec4b7d)

## 4. Access and Manipulate Image Pixels:
```Python
import cv2

# Load and resize the image
img = cv2.imread('jesko.jpg', 1)
img = cv2.resize(img, (300, 200))

# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115453](https://github.com/user-attachments/assets/96b809bd-bd11-4a13-8af8-735a61f3ec01)


![image](https://github.com/user-attachments/assets/b8046e59-11d5-4177-ad23-4dff09579f18)


## 5. Image Resizing:
```Python
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115537](https://github.com/user-attachments/assets/8120bd6c-5c5f-4739-8317-1012fa3273c0)

## 6.Image Cropping:
```Python
import cv2

# Load the image
image1=cv2.imread('lokesh.jpeg',1)
img1=cv2.resize(image1,(600,800))

# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 100, 100

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115604](https://github.com/user-attachments/assets/610a8242-1d4b-4356-948f-eb3108d24644)



## 7.Image Flipping:
i.)Flip the original image horizontally and display it.
```Python


import cv2

img = cv2.imread("lokesh.JPEG")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115621](https://github.com/user-attachments/assets/6927c61d-9613-4285-aa07-5f26c712516c)



#### ii.)Flip the original image vertically and display it.

```Python
import cv2

img = cv2.imread("lokesh.JPEG")
img1=cv2.resize(img,(600,800))
img = cv2.resize(img1,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115655](https://github.com/user-attachments/assets/fc93c97b-2c71-44bc-a53a-bb5ff37550e2)


## 8. Write and Save the Modified Image:
```Python
import cv2
img = cv2.imread("lokesh.JPEG")
img = cv2.resize(img,(300,200))
cv2.imwrite('lokesh1.jpg',img)
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/a3cfb30f-a732-425e-8cee-01c431bcaeb5)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.


