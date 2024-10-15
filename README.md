# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program and Output:
```python
import cv2
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread('cute.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

![Screenshot 2024-10-15 180244](https://github.com/user-attachments/assets/29260c15-ed1d-47da-826d-923b3f0b7fc7)

### SOBEL EDGE DETECTOR
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined)
plt.title('sobel combined image')
plt.axis('off')
plt.show()
```

![Screenshot 2024-10-15 180255](https://github.com/user-attachments/assets/2846efcc-9e6e-4bc7-a12d-5840cda2cacd)



### LAPLACIAN EDGE DETECTOR
```python
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian)
plt.title('Laplacian image')
plt.axis('off')
plt.show()
```

![Screenshot 2024-10-15 180305](https://github.com/user-attachments/assets/0eca08d9-6c14-4de1-bb92-61ff4285845a)


### CANNY EDGE DETECTOR
```python
# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges)
plt.title('canny_edges Image')
plt.axis('off')
plt.show()
```

![Screenshot 2024-10-15 180313](https://github.com/user-attachments/assets/f8fae0b2-b0d9-419e-9cb4-17fcaf03e556)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

