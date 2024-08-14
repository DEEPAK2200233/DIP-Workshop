# DIP-Workshop

## program
```
import cv2

# Read the image
image1 = cv2.imread('vijay.JPG')
image2= cv2.imread('loki2.JPG')
image1.shape

# Resize both images to the desired size (160,200)
new_size=(160,200) #(width,height)
image1_resized=cv2.resize(image1,new_size)
image2_resized=cv2.resize(image2,new_size)

image1_resized.shape



image2_resized.shape



height=200
width=160

# Define row and column coordinates for splitting
row_mid=100
col_mid=80

# Split the image into 4 regions using row and column coordinates
R1= image2_resized[0:row_mid,0:col_mid]
R2= image2_resized[0:row_mid,0:width]
R3= image2_resized[row_mid:height,0:col_mid]
R4= image2_resized[row_mid:height,col_mid:width]

# Split the image into 4 regions using row and column coordinates
R5= image1_resized[0:row_mid,0:col_mid]
R6= image1_resized[0:row_mid,0:width]
R7= image1_resized[row_mid:height,0:col_mid]
R8= image1_resized[row_mid:height,col_mid:width]

# Display the regions (optional)
cv2.imshow('Top-Left Region', R1)
cv2.imshow('Top-Right Region', R2)
cv2.imshow('Bottom-Left Region', R3)
cv2.imshow('Bottom-Right Region', R4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Display the regions (optional)
cv2.imshow('Top-Left Region', R5)
cv2.imshow('Top-Right Region', R6)
cv2.imshow('Bottom-Left Region', R7)
cv2.imshow('Bottom-Right Region', R8)
cv2.waitKey(0)
cv2.destroyAllWindows()

cv2.imwrite('R1.jpg',R1)
cv2.imwrite('R2.jpg',R2)
cv2.imwrite('R3.jpg',R3)
cv2.imwrite('R4.jpg',R4)

cv2.imwrite('R5.jpg',R5)
cv2.imwrite('R6.jpg',R6)
cv2.imwrite('R7.jpg',R7)
cv2.imwrite('R8.jpg',R8)

image1_resized[0:row_mid,0:col_mid] = R1
image2_resized[row_mid:height,col_mid:width] = R4

cv2.imshow('Image Window', image1_resized)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## output
![image](https://github.com/user-attachments/assets/7fa69cc2-ea5e-48d0-be3b-df7478ba0b3b)
