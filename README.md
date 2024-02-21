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
Developed By: ADHITHYA PERUMAL D
Register Number: 212222230007
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('dip.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Adhithya Perumal D',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-22 012924](https://github.com/Adhithya4116/COLOR_CONVERSIONS_OF-IMAGE/assets/118707079/0c5e4403-3ec0-457c-9853-01477e7ca538)
  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('dip.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-14 221949](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/5cb8fb8c-94c6-4824-a937-20133d07fd3b)

  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('dip.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-14 221959](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/01a1a274-5397-40b2-92cc-12f0461efdcb)

  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
    import random
    import cv2
    image=cv2.imread('dip.jpg',1)
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

![Screenshot 2024-02-14 215632](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/9713ec6a-cf5c-4ce6-ab4d-6bee498c55d9)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
    import cv2
    image=cv2.imread('dip.jpg',1)
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

![Screenshot 2024-02-14 215808](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/454ced9b-7c97-41e7-b6b4-b35ee60564e9)

  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('dip.jpg',1)
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
![Screenshot 2024-02-14 220108](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/974ea182-d59d-42f4-a279-2850dc2d1afb)
![Screenshot 2024-02-14 220148](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/911ebdd4-e022-4027-af9b-179ec45d5b15)
![Screenshot 2024-02-14 220124](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/240fd1d9-efc7-498e-8b52-c5a8c3906423)
![Screenshot 2024-02-14 220202](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/1bcf3378-c956-4616-b4dc-0f51c44e74a3)
![Screenshot 2024-02-14 220314](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/69216136-c0b6-4446-a913-b8968b754eb0)


### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('dip.jpg')
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
![Screenshot 2024-02-14 220548](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/dfef27a9-6079-4940-b452-5be127a51925)
![Screenshot 2024-02-14 220600](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/1d79530b-c5f4-47b8-a471-4c399cffc7ab)
![Screenshot 2024-02-14 220606](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/c0d1d7c3-9c91-4113-8aed-844e3c0bd7b7)


### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('dip.jpg')
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
![Screenshot 2024-02-14 220708](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/ed22d2d8-3c81-43d3-8146-54344ec5b53d)
![Screenshot 2024-02-14 220718](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/9f1518b4-290e-4c79-92ef-d137720f9113)
![Screenshot 2024-02-14 220726](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/bed29a97-9011-448f-8106-0c65c55b2660)


### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('dip.jpg',1)
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
```

### OUTPUT:
![Screenshot 2024-02-14 220808](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/ca007597-44df-4475-9e73-6ffc05cf045a)
![Screenshot 2024-02-14 220819](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/abecf7c3-a618-41b9-a063-9b83996847ea)
![Screenshot 2024-02-14 220828](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/287d17f0-1958-4ae1-8857-b7395809cbaf)
![Screenshot 2024-02-14 220837](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/fb5213a8-a084-4132-bce1-7fef7a6a7c7f)



### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("dip.jpg",1)
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
![Screenshot 2024-02-14 220939](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/d6d720ed-ee74-461a-82c8-5d50274e2a7a)
![Screenshot 2024-02-14 220947](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/9939f63c-2377-4d9d-9ca2-b1b65e49afa1)
![Screenshot 2024-02-14 220954](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/e5cfe648-6e58-45c2-a133-630263946496)
![Screenshot 2024-02-14 221004](https://github.com/DEVADARSHAN2/COLOR_CONVERSIONS_OF-IMAGE/assets/119432150/993407d3-23b3-426a-9a83-e6813b73ab42)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







