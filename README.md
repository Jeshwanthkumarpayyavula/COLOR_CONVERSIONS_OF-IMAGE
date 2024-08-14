# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1: Choose an image and save it as a filename.jpg ,
### Step2: Use imread(filename, flags) to read the file.
### Step3: Use imshow(window_name, image) to display the image.
### Step4: Use imwrite(filename, image) to write the image.
### Step5: End the program and close the output image windows.
### Step6: Convert BGR and RGB to HSV and GRAY
### Step7: Convert HSV to RGB and BGR
### Step8: Convert RGB and BGR to YCrCb
### Step9: Split and Merge RGB Image
### Step10: Split and merge HSV Image

##### Program:
```
Developed By: JESHWANTH KUMAR P
Register Number: 212223240114
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('jesko.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('JESHWANTH KUMAR',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

![image](https://github.com/user-attachments/assets/c05f7d9f-bda7-48a2-acfa-590bff17f172)
  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('jesko.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-23 091244]![image](https://github.com/user-attachments/assets/0d24cc83-f140-47f4-a0c9-cc0463cb33cd)


  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('jesko.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![image](https://github.com/user-attachments/assets/c0fd43aa-a791-4740-86e2-8a0116c90767)


  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
     import random
    import cv2
    image=cv2.imread('jesko.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

![image](https://github.com/user-attachments/assets/8be08c45-b62d-4f91-8060-e8f6c4df5e6f)


  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
    import cv2
   image=cv2.imread('jesko.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:

![image](https://github.com/user-attachments/assets/bb7e37ce-4a48-45de-b753-ff4e37170002)


  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('dipt1.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/user-attachments/assets/e2107a40-86bf-4a64-8835-44354d2ae9d1)

![image](https://github.com/user-attachments/assets/70168411-6d1e-498e-a07b-544a88d25879)

![image](https://github.com/user-attachments/assets/9b35ae7b-15a9-42a3-9eea-15b1098c166b)

![image](https://github.com/user-attachments/assets/71e1702c-d8f1-4abc-8ac5-b6e79f5be2c6)

![image](https://github.com/user-attachments/assets/13e56ce6-da71-4b57-9f35-f1595275abe2)




### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('jesko.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/user-attachments/assets/c9e40123-622c-49a9-8b5b-641ec026cc9b)

![image](https://github.com/user-attachments/assets/9fce32b0-888e-4303-94f1-0e8d46814f10)

![image](https://github.com/user-attachments/assets/bed9e7ff-c096-4da4-b947-a6c23148d18a)



### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('jesko.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/user-attachments/assets/5c2046d5-e938-455f-b6f4-45f44ce72202)

![image](https://github.com/user-attachments/assets/8d50a3c2-54ef-48d9-bedd-3dd3eb9e5c01)

![image](https://github.com/user-attachments/assets/297e2dc8-5de0-4ed4-99c5-7897995bcf7a)



### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('jesko.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/user-attachments/assets/26f456bf-5799-4551-a36e-f55c44a6c823)

![image](https://github.com/user-attachments/assets/573ddcf8-c72e-4db1-9987-e59791049ae5)

![image](https://github.com/user-attachments/assets/b42a5622-499d-4c73-8736-7a761f2eefb0)

![image](https://github.com/user-attachments/assets/905990af-a680-443e-ba69-81d23db20c64)




### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("jesko.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/user-attachments/assets/79d68598-1b41-4935-aa11-7cb4e6edf721)

![image](https://github.com/user-attachments/assets/3d11890e-bcf0-4a6b-a726-66c78183ba62)

![image](https://github.com/user-attachments/assets/b1bec7cf-0e0b-4ece-8640-f6fd39613bd9)

![image](https://github.com/user-attachments/assets/c7eefe55-9364-4f8a-a7ea-7c6519fc0835)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







