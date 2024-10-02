# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: SUBASHINI S
# Register Number: 212222240106
## Input Grayscale Image and Color Image:
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("subii.jpg")
color_image = cv2.imread("sarann.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image

![sarann](https://github.com/user-attachments/assets/1f1370f3-34e5-45aa-b301-502858323f69)
![subii](https://github.com/user-attachments/assets/11bd0a2d-94ff-42a5-9dac-501a2adb4ed4)

### Histogram of Grayscale Image and any channel of Color Image
```
import cv2
Gray_image = cv2.imread("subii.jpg")
Color_image = cv2.imread("sarann.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
## Output:
![Screenshot 2024-10-02 223523](https://github.com/user-attachments/assets/cf17591c-9e16-48e6-8da9-cccb54cc4307)

![graph](https://github.com/user-attachments/assets/70fdbe59-1cb7-4594-9fec-9a27e00397ff)

```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
## Output:
![color image](https://github.com/user-attachments/assets/90370fa4-17ef-46af-8a7f-4a8f3133d218)

![graph2](https://github.com/user-attachments/assets/8986b226-7aaf-4ae7-bdf5-89598d3de482)

### Histogram Equalization of Grayscale Image.
```
import cv2
gray_image = cv2.imread("subii.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-10-02 223902](https://github.com/user-attachments/assets/46a884a5-9ce1-4617-9506-1df5e25fa281)

![Screenshot 2024-10-02 223851](https://github.com/user-attachments/assets/8802b3e6-85b8-4aac-ac33-7d01f8af7f80)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
