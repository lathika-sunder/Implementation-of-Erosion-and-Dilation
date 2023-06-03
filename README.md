# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.

 
## Program:

``` Python
import cv2
import numpy
NameImage = numpy.zeros((100,1000),dtype='uint8')
font = cv2.FONT_ITALIC
cv2.putText(NameImage,'Lathika Sunder',(50,70),font,2,(255),5,cv2.LINE_4)
cv2.imshow("Name Image",NameImage)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
erodeImage = cv2.erode(NameImage,kernel1)
dilationImage = cv2.dilate(NameImage,kernel1)
cv2.imshow("Erode Image",erodeImage)
cv2.imshow("Dilated Image",dilationImage)
cv2.waitKey(0)

cv2.destroyAllWindows()

```
## Output:

### Display the input Image
![image](https://github.com/lathika-sunder/Implementation-of-Erosion-and-Dilation/assets/95066409/8c70f1fd-e55b-4ec2-a99e-ac1f1bc32a20)

### Display the Eroded Image
![image](https://github.com/lathika-sunder/Implementation-of-Erosion-and-Dilation/assets/95066409/f36b5e6b-9669-4469-ab2c-c52bc1c9a848)

### Display the Dilated Image
![image](https://github.com/lathika-sunder/Implementation-of-Erosion-and-Dilation/assets/95066409/9748ca4c-39ef-424a-a8b5-ceb9917a15d4)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
