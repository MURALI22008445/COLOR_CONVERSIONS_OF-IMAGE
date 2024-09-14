# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

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
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.


## Program:
### Developed By: KMURALIS
### Register Number: 212222230088


## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```
import cv2
image=cv2.imread('naturek.jpg',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('NATUREK',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```![BALL](https://github.com/user-attachments/assets/5052c197-529e-4f9f-8b5b-19ad48bc03ea)


### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("naturek.jpg")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![BALL](https://github.com/user-attachments/assets/d08573de-a26a-47f2-9a9d-aa6a3ae1da07)


2. Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("naturek.jpg")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![BALL](https://github.com/user-attachments/assets/119d22a2-20d9-40ac-afc4-7410187a54d7)


3.Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("naturek.jpg")
image = cv2.resize(image, (400, 300))
start = (150, 100)
stop = (300, 200)
color = (255, 255, 100)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('WINDOW', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![BALL](https://github.com/user-attachments/assets/15455866-2c0e-4db8-b9a6-fedf7604b2ee)



4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("naturek.jpg")
image = cv2.resize(image, (400, 300))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```![BALL](https://github.com/user-attachments/assets/68a9e004-10ee-4eb2-b690-06ef16e8bffa)

### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('naturek.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![BALL](https://github.com/user-attachments/assets/e2c5fb1e-7ef0-4ca8-8d88-444bde7f8c70)


(2) Convert the image from RGB to GRAY and display it.

```
import cv2
image = cv2.imread('naturek.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![BALL](https://github.com/user-attachments/assets/e02a21d3-bd79-4fd8-99c3-8bd529441629)



(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('naturek.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```![BALL](https://github.com/user-attachments/assets/33dd800a-5baf-421e-a875-120f90fe0cc3)


(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('naturek.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```![BALL](https://github.com/user-attachments/assets/0b9d9e33-2978-4aee-beec-8ab7842f37f1)


### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```![BALL](https://github.com/user-attachments/assets/26318bb5-c86c-4aee-900f-d135317a1284)

(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('naturek.jpg',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```![BALL](https://github.com/user-attachments/assets/8fc76a3c-076f-4018-9dad-6cc69dcde4d7)


### v)Image Resizing:
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![BALL](https://github.com/user-attachments/assets/c06aef26-73e1-43bf-b5a3-48b234e22506)
![BALL](https://github.com/user-attachments/assets/f280eded-2f84-4ecd-a838-ad2ba1695f3f)



### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('naturek.jpg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```![BALL](https://github.com/user-attachments/assets/38950230-ea00-4105-89a2-4eabe2ee3803)

### vii)Image Flipping:
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("naturek.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```![BALL](https://github.com/user-attachments/assets/4fabc495-9ad7-4e67-b313-31abd2b5977f)


(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("naturek.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```![BALL](https://github.com/user-attachments/assets/00e141a6-ebb1-4425-9912-df2195a33491)
![BALL](https://github.com/user-attachments/assets/b398e90a-8a13-4781-bf8a-b7d71b2d6427)


### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("naturek.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('nature_pic.jpg',img)
```
![BALL](https://github.com/user-attachments/assets/30e859c1-65b0-45cc-91bb-411bad7912d9)


## Result:

Thus the images are read, displayed, and written ,and color conversion was performed successfully using the python program.
