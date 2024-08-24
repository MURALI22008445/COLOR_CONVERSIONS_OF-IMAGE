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
Developed By: MURALI S
Register Number: 212222230088
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('dipt1.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('ADHITHYA PERUMAL D',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-23 083710](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/57b30bba-72f7-4a90-8d8d-a8792c09332e)
  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('dipt1.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-23 091244](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/379f8574-d4ae-4b97-abd6-44cd836406f4)

  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('dict.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-23 091516](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/bb67af01-fbb9-4d0c-9dd9-ac291d63c658)

  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
     import random
    import cv2
    image=cv2.imread('dipt1.jpg',1)
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

![Screenshot 2024-02-23 084102](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/59308692-83b3-4f2b-a9a1-480b6836f567)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
    import cv2
   image=cv2.imread('dipt1.jpg',1)
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

![Screenshot 2024-02-23 084222](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/15da7645-5672-487e-8fbe-984ca6bfd9bd)

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
![Screenshot 2024-02-23 084608](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/16208cee-19e7-4594-bdfa-5b06890fb8c2)
![Screenshot 2024-02-23 084628](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/599ffe97-ee92-4e29-ad0e-8e9f5511791a)
![Screenshot 2024-02-23 084652](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/05aa0768-5f21-4eca-a117-b62cdd91d655)
![Screenshot 2024-02-23 084811](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/f4b2d14b-80fa-4f98-b210-1c62a0de1ccc)
![Screenshot 2024-02-23 084845](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/0cb2173e-1597-41be-bcc7-b6bce1c44c62)



### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('dipt1.jpg')
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
![Screenshot 2024-02-23 085017](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/0712c22e-318f-49fd-a956-e035ce6ecedb)
![Screenshot 2024-02-23 085039](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/0907c3a8-f581-45d7-9230-c6d3e032ae2f)
![Screenshot 2024-02-23 092944](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/184260e7-2404-46a5-90e4-71a5d388217b)


### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('dipt1.jpg')
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
![Screenshot 2024-02-23 085332](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/6fa30ea6-b8b9-44ab-83d6-edaa74ff973c)
![Screenshot 2024-02-23 085353](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/b11bac11-69f7-4b11-90ac-16c3f2d6c259)
![Screenshot 2024-02-23 085410](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/057b941a-79c3-44dc-a044-7d971e0992d7)


### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('dipt1.jpg',1)
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
![Screenshot 2024-02-23 085554](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/2fc409d0-21c6-4e58-a3b0-167cec12a6aa)
![Screenshot 2024-02-23 085619](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/e71bd410-cd12-45d9-92d1-5ff78a86d35f)
![Screenshot 2024-02-23 085635](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/c9f546f9-174b-40d0-99b2-a89f0d4db81b)
![Screenshot 2024-02-23 085717](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/3bf3d374-e4f9-448f-8231-10c153cb269f)



### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("dipt1.jpg",1)
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
![Screenshot 2024-02-23 085858](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/2a261e8d-f5fb-4a76-bb63-a09dcf09c76c)
![Screenshot 2024-02-23 085918](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/a6e533df-a3a6-4f2d-afe3-f76b77574bf6)
![Screenshot 2024-02-23 085933](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/a2c62f7a-e7bf-404e-8520-a399fa79f54d)
![Screenshot 2024-02-23 085947](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/5aee15ce-f5e8-485d-b50f-3db1a10d0671)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







