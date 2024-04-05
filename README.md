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
# Developed By: Gokularamanan k
# Register Number: 212222230040


## Gray Image and Color Image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("ajith.png")
color_image = cv2.imread("vijay.png",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

## Histogram of Grayscale Image
gray_img = cv2.imread('ajith.png')
color_img = cv2.imread('vijay.png')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

## Histogram of Color Image
gray_img = cv2.imread('ajith.png')
color_img = cv2.imread('vijay.png')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(color_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

## Histogram Equilization of GrayScale Image
gray_img = cv2.imread('ajith.png',0)
gray_img1 = cv2.resize(gray_img,(200,400))
cv2.imshow('Grey Scale Image',gray_img1)
equ = cv2.equalizeHist(gray_img1)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)







```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-04-05 085618](https://github.com/Gokulanbazhagan/Histogram-of-an-images/assets/119518996/5f33c675-ca67-401c-8a08-6e6cdc321a30)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-04-05 085733](https://github.com/Gokulanbazhagan/Histogram-of-an-images/assets/119518996/e8ee0365-2e2c-486d-84bd-d5be26256ebe)

![Screenshot 2024-04-05 085754](https://github.com/Gokulanbazhagan/Histogram-of-an-images/assets/119518996/2f08937c-6167-43db-ba07-ee13ba2b00f8)


![Screenshot 2024-04-05 085932](https://github.com/Gokulanbazhagan/Histogram-of-an-images/assets/119518996/d6b1c0ef-3f6d-4e58-96e8-7c367d386463)

![Screenshot 2024-04-05 085943](https://github.com/Gokulanbazhagan/Histogram-of-an-images/assets/119518996/9ffbd07a-625b-48fe-90eb-f5ae42f4cb2b)







### Histogram Equalization of Grayscale Image.
![Screenshot 2024-04-05 090306](https://github.com/Gokulanbazhagan/Histogram-of-an-images/assets/119518996/45c616ad-f38d-4b49-ae20-7e6bdb239f17)

![Screenshot 2024-04-05 090425](https://github.com/Gokulanbazhagan/Histogram-of-an-images/assets/119518996/efbfab79-661a-471a-897c-040290b43df6)






## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
