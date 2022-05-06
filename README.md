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
![e1](https://user-images.githubusercontent.com/93427286/167076217-7059475b-af4c-4e34-9711-79f91873842d.png)

<br>


### Histogram of Grayscale Image and any channel of Color Image
<br>

![e2](https://user-images.githubusercontent.com/93427286/167076247-2836e37c-e79f-4518-a01f-6568f497a588.png)

<br>

### Histogram Equalization of Grayscale Image
<br>
![e3](https://user-images.githubusercontent.com/93427286/167076273-1ec0ee2f-3bd2-429e-b259-d5e31d3100b3.png)
![e4](https://user-images.githubusercontent.com/93427286/167076282-b159d916-1361-4f9e-aa3e-3b8477aeb947.png)
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
