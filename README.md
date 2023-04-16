# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.


### Step2:
Read the image and convert the bgr image to gray scale image.

### Step3:
Use any filters for smoothing the image to reduse the noise.

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow.

 
## Program:


# Import the packages
```
import cv2
import matplotlib.pyplot as plt
```
# Load the image, Convert to grayscale and remove noise
```
image = cv2.imread("ex7.jpg")
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image= cv2.GaussianBlur(gray_image,(3,3),0)
plt.axis("off")
```
# SOBEL EDGE DETECTOR
```
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.imshow(sobelx)
plt.title("SOBEL_X")
plt.xticks([])
plt.yticks([])
plt.show()
sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.imshow(sobely)
plt.title("SOBEL_Y")
plt.xticks([])
plt.yticks([])
plt.show()
sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.imshow(sobelxy)
plt.title("SOBEL_XY")
plt.xticks([])
plt.yticks([])
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.imshow(laplacian)
plt.title('LAPLACIAN')
plt.axis("off")
plt.show()
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.imshow(laplacian)
plt.title('LAPLACIAN')
plt.axis("off")
plt.show()
```
# CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(new_image, 120, 150)
plt.figure(figsize = (8,8))
plt.imshow(canny_edges)
plt.title('CANNY_EDGES')
plt.axis("off")
plt.show()
```
## Output:
### Convert to grayscale and remove noise
![image](https://user-images.githubusercontent.com/93992063/232273242-9ea8664d-588b-4b27-a19d-0e556b3d4a44.png)

### SOBEL EDGE DETECTOR
![image](https://user-images.githubusercontent.com/93992063/232273260-7196dcc3-b741-4871-bd1b-5bdb4cf58758.png)
![image](https://user-images.githubusercontent.com/93992063/232273268-833083be-2d24-419a-a7af-2578b64d70cf.png)



### LAPLACIAN EDGE DETECTOR
![image](https://user-images.githubusercontent.com/93992063/232273275-15abee60-7b65-4526-a053-6aa6bcf4bfa9.png)



### CANNY EDGE DETECTOR

![image](https://user-images.githubusercontent.com/93992063/232273307-1c577580-e0a3-4cce-b260-22a9791edc56.png)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
