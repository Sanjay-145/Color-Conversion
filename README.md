# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

Read an image using imread() and Convert BGR and RGB to HSV and GRAY
using:
cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)


### Step2:
Convert HSV to RGB and BGR
using:
cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)

### Step3:
Convert RGB and BGR to YCrCb
using:
cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)

### Step4:
Split and Merge RGB Image
using:
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.merge((blue,green,red))

### Step5:
Split and merge HSV Image
using:
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.merge((h,s,v))

## Program:
```python
# Developed By: P.Sanjay
# Register Number:212220230042
```
# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
image=cv2.imread("Eat.jpeg")
cv2.imshow("212220230042",image)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV image",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY image",BGR_GRAY)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV image",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY image",RGB_GRAY)
cv2.imshow("Eatz",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```


# ii)Convert HSV to RGB and BGR
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV image",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB image",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR image",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

```


# iii)Convert RGB and BGR to YCrCb
```
RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb image",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb image",BGR_YCrCb)
cv2.imshow("Eatz",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


# iv)Split and Merge RGB Image
```
blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged Image",merged)
cv2.imshow("Eatz",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

# v) Split and merge HSV Image
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV image",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()




```
## Output:
### i) BGR and RGB to HSV and GRAY
![1A](https://user-images.githubusercontent.com/75235426/163584657-020b82c9-fadc-4b47-9950-ee2523ea19ed.png)
![1B](https://user-images.githubusercontent.com/75235426/163584677-0b127ff4-c61a-476e-9ad8-1843fc842aa5.png)
![1C](https://user-images.githubusercontent.com/75235426/163584702-5ff861cd-fe84-4e89-b459-2b48673806d6.png)


### ii) HSV to RGB and BGR
![2A](https://user-images.githubusercontent.com/75235426/163584729-ecec2445-7d1d-4624-b0fc-07aa1d3046eb.png)
![2B](https://user-images.githubusercontent.com/75235426/163584751-615ee3c7-aa38-47f2-a5be-4a883fbd8a69.png)


### iii) RGB and BGR to YCrCb
![3A](https://user-images.githubusercontent.com/75235426/163584777-ef5db6dd-a495-4829-9578-1a4288338d1f.png)
![3B](https://user-images.githubusercontent.com/75235426/163584794-79eb3bb7-40b3-402f-8070-227039adb6d4.png)


### iv) Split and merge RGB Image
![4A](https://user-images.githubusercontent.com/75235426/163584816-d1792c6a-41c8-4548-be77-0b03cb869b51.png)
![4B](https://user-images.githubusercontent.com/75235426/163584831-844bfee0-808d-42c9-95f7-a2ae8cf881da.png)
![4C](https://user-images.githubusercontent.com/75235426/163584842-5a4babdf-016f-4ec2-9a48-9da8b1fdd186.png)


### v) Split and merge HSV Image
![5A](https://user-images.githubusercontent.com/75235426/163584858-a5cea744-7c90-4327-934d-c8149caf0a75.png)
![5B](https://user-images.githubusercontent.com/75235426/163584877-bf1fed30-63a5-4b02-afea-6c181b777679.png)
![5C](https://user-images.githubusercontent.com/75235426/163584894-09c09697-e245-4391-b100-4588834e8720.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
