# Edge-Linking-using-Hough-Transform
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read image and convert it to grayscale image.

### Step2:
Find the edges in the image using canny detector and display.

### Step3:
Detect points that form a line using HoughLinesP.

### Step4:
Draw lines on the image.
### Step5:
Display the result.


## Program:
NAME : charumathi R
REF NO : 212222240021
```Python

# Read image and convert it to grayscale image
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('road.png',0)
img= cv2.GaussianBlur(image1,(3,3),0)
plt.imshow(img)


# Find the edges in the image using canny detector and display
edges1 = cv2.Canny(img,100,200)
plt.imshow(edges1,cmap = 'gray')
plt.title('Edge Image'), plt.xticks([]), plt.yticks([])
plt.show()



# Detect points that form a line using HoughLinesP
lines=cv2.HoughLinesP(edges1,1,np.pi/180, threshold=80, minLineLength=50,maxLineGap=250)

# Draw lines on the image
for line in lines:
    x1,y1,x2,y2=line[0]
    cv2.line(img_c,(x1,y1),(x2,y2),(255,0,0),3)

# Display the result

plt.imshow(edges1)


```
## Output

### Input image and grayscale output
![download](https://github.com/charumathiramesh/Edge-Linking-using-Hough-Transform/assets/120204455/0245d0f2-e545-48db-9964-62bc2d2bc5d0)

### Canny Edge detector output

![download](https://github.com/charumathiramesh/Edge-Linking-using-Hough-Transform/assets/120204455/81d74338-af22-4ee2-b375-28d2e90c5927)

### Display the result of Hough transform
![download](https://github.com/charumathiramesh/Edge-Linking-using-Hough-Transform/assets/120204455/f531dcdf-39b3-4254-827e-a2bc3d21998a)




## Result:
Thus the program is written with python and OpenCV to detect lines using Hough transform. 
