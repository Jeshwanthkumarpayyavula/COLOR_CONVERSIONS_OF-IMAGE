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
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.
### Step8:
o	Save the final modified image to your local directory.
```
Developed By: JESHWANTH KUMAR P
Register Number: 212223240114
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

![image](https://github.com/user-attachments/assets/9c08dd8d-564b-4f9a-9957-6dfc831f98be)


 

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

![image](https://github.com/user-attachments/assets/869e9b2a-3654-4454-af81-14374a3e13d8)



 
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
![image](https://github.com/user-attachments/assets/c9b6778c-0a99-43b6-b055-14944003daff)



      
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

![image](https://github.com/user-attachments/assets/9772bc72-1b07-45b1-8ab9-4b55f4059172)



      
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

![image](https://github.com/user-attachments/assets/3fa0ff45-0683-451c-99f5-07f49c0cae43)



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
![image](https://github.com/user-attachments/assets/13292b19-7209-4129-8674-a0d590a63b81)

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
![image](https://github.com/user-attachments/assets/af6fcf0d-eb1b-41ea-b36f-7b4cd42c6a0e)


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
![image](https://github.com/user-attachments/assets/fce06302-2222-4937-bb09-eb03c9463ecc)

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
![image](https://github.com/user-attachments/assets/44796180-8170-4a05-8227-aaa2db8a21ab).

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
![image](https://github.com/user-attachments/assets/81a369cd-6904-4f98-b9ec-3af5a4e045b2)


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
![image](https://github.com/user-attachments/assets/fcc176ba-3490-4d1d-92a6-f3ecbfb3f12c)

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
![image](https://github.com/user-attachments/assets/628ff900-c0ec-4948-af16-48342e5350c6)



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
![image](https://github.com/user-attachments/assets/13375c08-5d9c-4b72-a7df-5b1477636f71)



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
![image](https://github.com/user-attachments/assets/fda2d974-5c3d-4d2b-827c-ecf548e1fcbe)


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
![image](https://github.com/user-attachments/assets/edd640c1-b2b9-48b8-ac8c-33be8b8b22f8)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.


