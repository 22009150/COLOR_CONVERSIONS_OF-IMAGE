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
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:

### Developed By:Archana k
### Register Number: 212222240011


## Output:

### i) Read and display the image

    import cv2
    image=cv2.imread('flowers.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Archana',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    
![img1](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/aa3cc7bd-7ccb-4c21-94a3-6baa18c54fca)


### ii)Write the image

    import cv2
    image=cv2.imread('flowers.jpg',0)
    cv2.imwrite('demos.jpg',image)
    
![Screenshot (109)](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/9dbc2ae5-5022-44be-b238-f758e580c69c)


### iii)Shape of the Image

    import cv2
    image=cv2.imread('flowers.jpg',1)
    print(image.shape)
    

![img3](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/b6ce2549-6edc-4f10-91ab-25f377149262)



### iv)Access rows and columns

    import random
    import cv2
    image=cv2.imread('flowers.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/7bd8d0be-b7f0-4412-800e-0b60736d544a)

### v)Cut and paste portion of image
```
   import cv2
   
   image=cv2.imread('flowers.jpg',1)
   
   image=cv2.resize(image,(400,400))
   
   tag =image[150:200,110:160]
   
   image[110:160,150:200] = tag
   
   cv2.imshow('partimage1',image)
   
   cv2.waitKey(0)
   
   cv2.destroyAllWindows()
  ``` 
   ![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/4ba1e621-10e5-4edc-bb2c-7538e256fbeb)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('flowers.jpg',1)
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
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/86462163-2562-4d07-8abd-5967fbd5c7ab)
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/e32f90e4-e7f2-44b5-8ad2-915ead5ac454)
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/0fd5084b-cbc5-44f3-8baf-f0f727cebdab)

### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('flowers.jpg')
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
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/25d975fa-86ab-4c76-8c4a-12948ea2c379)
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/bc98ce7f-35fc-4828-8a8a-02173162cd31)
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/226e8b65-e732-4dda-a582-6b9106cb7927)

### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('flowers.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/4e210ce0-1b0b-4105-b397-74aa27d4cfcc)
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/d673661e-08eb-4b6d-90ed-bbdb1e4ddfbe)
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/76cf322a-8143-40d5-a4e0-15d8bec10223)

### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('flowers.jpg',1)
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
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/2228539d-2350-40c0-900f-778ed05a2c52)
![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/1e2fedd2-6031-4271-a740-782e160ca6e6)

### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("flowers.jpg",1)
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

![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/4b9a326f-c0d0-4100-a630-2c9ea0b94c07)

![image](https://github.com/22009150/COLOR_CONVERSIONS_OF-IMAGE/assets/118708624/254c68f7-1be5-4adc-a941-e0b0d26a517f)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







