# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and any one channel of the color image.

### Step3:
Display the histograms.

### Step4:
Equalize the color image.

### Step5:
Display the equalized grayscale image.

## Program:
Developed By: Adhithya.S

Register Number: 212222240003
```python


import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('img_2.png')
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread('kratos.jpeg')
plt.imshow(Color_image)
plt.show()
```

### Write your code to find the histogram of gray scale image and color image channels.
```
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("gray_scale value")
plt.ylabel("pixel count")
plt.stem(hist)
plt.show()
```



### Display the histogram of gray scale image and any one channel histogram from color image
```
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("color_scale value")
plt.ylabel("pixel count")
plt.stem(hist1)
plt.show()
```


### Write the code to perform histogram equalization of the image. 
```
equ=cv2.equalizeHist(cv2.imread('color.jpg',0))
equ=cv2.cvtColor(equ,cv2.COLOR_BGR2RGB)
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ)
plt.show()
```



## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/s-adhithya/HISTOGRAM/assets/113497423/c3156905-adf6-4ae3-8ac1-14b43c11f1e0)
![image](https://github.com/s-adhithya/HISTOGRAM/assets/113497423/3e412284-a1f0-41a0-8459-0bd9cf9841bb)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/s-adhithya/HISTOGRAM/assets/113497423/85eb0c9c-512d-40e4-925e-92941ecbed36)
![image](https://github.com/s-adhithya/HISTOGRAM/assets/113497423/bedc99b0-65d1-4085-8909-6666f8a822c8)


### Histogram Equalization of Grayscale Image
![image](https://github.com/s-adhithya/HISTOGRAM/assets/113497423/065ec08c-797d-4f13-8d34-7736d8dc543b)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
