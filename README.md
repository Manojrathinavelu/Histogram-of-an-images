# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and matplotlib.pyplot
<br>

### Step2:
Read and display the input images
<br>

### Step3:
Calculate the Histogram Values using calcHist()
<br>

### Step4:
Display the histograms
<br>

### Step5:
Calculate and display the equalized image using equalizeHist()
<br>

## Program:
```
# Developed By: NAVIN KUMAR J
# Register Number: 212222240071
import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 
gray_image = cv2.imread('grayscale.jpeg')
color_image = cv2.imread('color.jpeg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()



# Equalized Image
import cv2
Gray_image=cv2.imread('gray.jpeg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
Gray Scale Image
![314163539-94336f31-2f9f-4f16-a70a-06395a521c8b](https://github.com/Manojrathinavelu/Histogram-of-an-images/assets/119560395/8bf30e95-c54f-47f6-af10-dd31e17de306)



Color Image
![314163634-d2d07384-c553-474b-8c1f-c8c1b874d921](https://github.com/Manojrathinavelu/Histogram-of-an-images/assets/119560395/728b1742-5c60-4d78-8dce-5af1c554a7dc)



<br>

### Histogram of Grayscale Image and any channel of Color Image

Gray Scale Image
![314165711-2f9a2fc9-2bbb-4688-9851-f51ab9bc7733](https://github.com/Manojrathinavelu/Histogram-of-an-images/assets/119560395/dc643bd5-18ca-4591-96a5-1ec4adb3b050)
![314164232-fa94d1cc-c334-40d5-9824-5d6ad15342e6](https://github.com/Manojrathinavelu/Histogram-of-an-images/assets/119560395/576dfb5e-8987-4b5d-8369-cba39919168e)


Color Image
![314165751-95eba9a9-26b4-45fc-a57d-bbbb7cc4c62e](https://github.com/Manojrathinavelu/Histogram-of-an-images/assets/119560395/d9075655-eaea-42b4-8fb1-3a5773f8fd61)
![314164277-c52af793-a25f-4baa-bf4d-5fb94629cfa7](https://github.com/Manojrathinavelu/Histogram-of-an-images/assets/119560395/c433dfab-68a7-429b-8b9d-3863c892983d)


<br>

### Histogram Equalization of Grayscale Image

Original  & Equalized Image

![314165247-78f9146c-f2c9-4b67-92a6-e473ae44f117](https://github.com/Manojrathinavelu/Histogram-of-an-images/assets/119560395/476fbb6a-e6d8-488e-9203-35fdfefeddb6)

<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
