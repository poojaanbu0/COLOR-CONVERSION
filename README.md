# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

Import cv2 library and upload the image or capture an image.
</br>

### Step2:

Read the saved image using cv2.imread().


### Step3:

Convert the image into the given color transformation using cv2.cvtColor().<br>

### Step4:

Split and merge the image using cv2.split() and cv2.merge()<br>

### Step5:
Output the image using cv2.imshow()
<br>

## Program:
```python
# Developed By: POOJA A
# Register Number: 212222240072

# i) Convert BGR and RGB to HSV and GRAY

import cv2

myimage = cv2.imread('volcano640.png')
cv2.imshow('Original Image',myimage)


#BGR2HSV
myimage = cv2.cvtColor(myimage, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',myimage)

#RGB2HSV
myimage = cv2.cvtColor(myimage, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',myimage)

#BGR2Gray
myimage = cv2.cvtColor(myimage, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', myimage)

#RGB2Gray
grayimage = cv2.cvtColor(myimage, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', grayimage)

cv2.waitKey(0) 
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

myimage = cv2.imread("space.jpg")
image= cv2.resize(myimage, (465,324))

#BGR2HSV
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
cv2.imshow("HSV", hsv)

hsv_rgb = cv2.cvtColor(hsv, cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB", hsv_rgb)

hsv_bgr = cv2.cvtColor(hsv, cv2.COLOR_HSV2BGR)
cv2.imshow("HSV2BGR", hsv_bgr)

cv2.waitKey(0)
cv2.destroyAllWindows()




# iii)Convert RGB and BGR to YCrCb

import cv2

myimage = cv2.imread("nb.png")

cv2.imshow("Original_BGR", myimage)

img_ycrcb = cv2.cvtColor(myimage , cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR2YCrCb", img_ycrcb)

img_rgb = cv2.cvtColor(myimage, cv2.COLOR_BGR2RGB)
cv2.imshow("BGR2RGB", img_rgb)

img_bgr_y = cv2.cvtColor(img_rgb, cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB2YCrCb", img_bgr_y)

cv2.waitKey(0)
cv2.destroyAllWindows()


# iv)Split and Merge RGB Image

myimage = cv2.imread("b.png")


b,g,r = cv2.split(myimage)
cv2.imshow("red model", r)
cv2.imshow("green model", g)
cv2.imshow("blue model ", b)

merger = cv2.merge([b,g,r])
cv2.imshow("merged", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()


# v) Split and merge HSV Image

import cv2

myimage = cv2.imread("t.png")
hsv = cv2.cvtColor(myimage , cv2.COLOR_BGR2HSV)
cv2.imshow("initial hsv ", hsv)

h,s,v = cv2.split(hsv)
cv2.imshow("hue model", h)
cv2.imshow("saturation model", s)
cv2.imshow("value model ", v)

merger = cv2.merge([h,s,v])
cv2.imshow("merged image", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### i) BGR and RGB to HSV and GRAY

![WhatsApp Image 2023-11-14 at 02 50 43_ca38440c](https://github.com/poojaanbu0/COLOR-CONVERSION/assets/119390329/42cd10d5-5554-42f0-998d-b74c1f1ed56d)

### ii) HSV to RGB and BGR
![WhatsApp Image 2023-11-14 at 02 51 52_b22538bc](https://github.com/poojaanbu0/COLOR-CONVERSION/assets/119390329/85b482bf-77f8-4394-a87e-c9af17a0b2f6)
![WhatsApp Image 2023-11-14 at 02 52 11_de3d48ab](https://github.com/poojaanbu0/COLOR-CONVERSION/assets/119390329/c9cd8e07-f56d-45c0-b013-2c123a0ba9ac)


### iii) RGB and BGR to YCrCb
![WhatsApp Image 2023-11-14 at 02 52 43_18d73838](https://github.com/poojaanbu0/COLOR-CONVERSION/assets/119390329/05759b9d-eca1-49f0-b065-f0f763a5c76b)


### iv) Split and merge RGB Image
![WhatsApp Image 2023-11-14 at 02 53 08_d66fb61c](https://github.com/poojaanbu0/COLOR-CONVERSION/assets/119390329/0ab8df62-dc14-44dc-b339-03b9d915258f)

![WhatsApp Image 2023-11-14 at 02 53 31_205f2d20](https://github.com/poojaanbu0/COLOR-CONVERSION/assets/119390329/4e43a43c-a2fe-4a4f-9855-5f813a2430a8)

![WhatsApp Image 2023-11-14 at 02 53 55_c593c952](https://github.com/poojaanbu0/COLOR-CONVERSION/assets/119390329/8c776e6e-07d1-4b1c-9d02-ea1a8ec67d36)

### v) Split and merge HSV Image
![WhatsApp Image 2023-11-14 at 02 54 22_26b3481a](https://github.com/poojaanbu0/COLOR-CONVERSION/assets/119390329/5047b9d6-32ce-41c3-b818-716f6f48f34f)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
