# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
```
## Developed By:KRISHNA PRAKAASH D M
##  Register Number: 212221230052
```

i) #To Read,display the image
```
 import cv2
from google.colab.patches import cv2_imshow
a = cv2.imread('/content/IMAGE-01.PNG',1)
cv2_imshow(a)
cv2.waitKey(0) 

```
ii) #To write the image
```

colorImage = cv2.imread('/content/IMAGE-01.PNG',1)
cv2.imwrite('written.jpg',colorImage)
writtenImage = cv2.imread('written.jpg',1)
cv2_imshow(writtenImage)
cv2.waitKey(0)



```
iii) #Find the shape of the Image
```python3

colorImage = cv2.imread('/content/IMAGE-01.PNG',1)
print(colorImage.shape)




```
iv) #To access rows and columns

```
import random
colorImage = cv2.imread('/content/IMAGE-01.PNG',1)
for i in range(100):
    for j in range(colorImage.shape[1]):
        colorImage[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2_imshow(colorImage)
cv2.waitKey(0)





```
v) #To cut and paste portion of image
```python3

color_img = cv2.imread('/content/IMAGE-01.PNG',1)
tag = color_img[100:200,200:400]
color_img[100:200,100:300] = tag
cv2_imshow(color_img)
cv2.waitKey(0)




```

## Output:

### i) Read and display the image

![OUTPUT-01](PIC-1.PNG)

### ii)Write the image

![OUTPUT-02](PIC-2.PNG)


### iii)Shape of the Image

![OUTPUT-03](PIC-5.PNG)


### iv)Access rows and columns
![OUTPUT-04](PIC-3.PNG)


### v)Cut and paste portion of image
![OUTPUT-03](PIC-4.PNG)

## Result:
Thus the images are read, displayed, and written successfully using the python program.


