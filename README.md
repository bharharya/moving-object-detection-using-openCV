# moving-object-detection-using-openCV
before using this code make sure your computer pre installed with openCV and imutiles library.

#image resize 

import cv2
import imutils
img = cv2.imread(‘sample2.jpg')
resizedImg = imutils.resize(img, width=500)
cv2.imwrite(‘resizedImage.jpg', resizedImg)

#Gaussian Blur - Smoothening!

import cv2
img = cv2.imread(‘sample2.jpg')
grayImg = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
#dst = cv2.GaussianBlur(src, (kernel),borderType)
gaussianImg = cv2.GaussianBlur(grayImg, (21, 21), 0)
cv2.imwrite(“GaussianBlur.jpg”, gaussianImg)

#threshold!

#dst = cv2.threshold(src, threshold, maxValueForThreshold,binary,type)[1] 
import cv2
img=cv2.imread("sample.jpg")
grayImg = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
gaussBlur = cv2.GaussianBlur(grayImg,(21,21),0)
thresholdImg = cv2.threshold(grayImg,150,255,cv2.THRESH_BINARY)[1]
cv2.imwrite("threshold.jpg",thresholdImg)


