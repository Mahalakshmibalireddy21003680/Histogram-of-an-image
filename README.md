# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:
Display the histograms with their respective images.
<br>

### Step4:
Equalize the grayscale image.
<br>

### Step5:
Display the grayscale image.
<br>

## Program:
```python
# Developed By:Balireddy mahalakshmi
# Register Number:212221240008
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
gray_image=cv2.imread('parachute.jpg')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()


# Display the histogram of gray scale image and any one channel histogram from color image
color_image=cv2.imread('parachute.jpg')
hist=cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('colorscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()




# Write the code to perform histogram equalization of the image. 

gray_image = cv2.imread('gray.jpg',0)
equ=cv2.equalizeHist(parachute_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()





```
## Output:
### Input Grayscale Image and Color Image
<br>
![e1](https://user-images.githubusercontent.com/93427286/167075885-46ac12d7-17c0-4f98-a31f-d20d68625a48.png)
<br>


### Histogram of Grayscale Image and any channel of Color Image
<br>
![e2](https://user-images.githubusercontent.com/93427286/167075924-4e42b3fe-8e3a-4507-9777-f320327daac8.png)

<br>

### Histogram Equalization of Grayscale Image
<br>
![e3](https://user-images.githubusercontent.com/93427286/167075937-cb2d7613-af31-40b6-8d22-63ee05e9b03e.png)

![e4](https://user-images.githubusercontent.com/93427286/167075989-6741ce3e-0e34-4b5c-86fa-ae39c26ec93c.png)
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
