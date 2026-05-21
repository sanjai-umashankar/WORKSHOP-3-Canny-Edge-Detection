# WORKSHOP – Canny Edge Detection using OpenCV and Matplotlib
## Aim

To perform edge detection on an image using the Canny Edge Detection algorithm with OpenCV and display the output using Matplotlib.

## Requirements

Install the required libraries:

pip install opencv-python matplotlib
## Theory
Canny Edge Detection

Canny Edge Detection is one of the most popular edge detection techniques in image processing.

It is used to identify sharp changes in intensity in an image.

## The algorithm performs the following steps:

Noise Reduction using Gaussian Blur
Gradient Calculation
Non-Maximum Suppression
Double Thresholding
Edge Tracking by Hysteresis

## It is widely used in:

Image Processing
Computer Vision
Object Detection
Shape Recognition
Algorithm
Read the input image
Convert the image into grayscale
Apply the Canny Edge Detection algorithm
Display the original and edge-detected images
## Program
```
import cv2
import matplotlib.pyplot as plt

# Read image
img = cv2.imread("face.jpg")

# Convert image to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Apply Canny Edge Detection
edges = cv2.Canny(gray, 100, 200)

# Display images
plt.figure(figsize=(10,5))

# Original image
plt.subplot(1,2,1)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

# Edge detected image
plt.subplot(1,2,2)
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detection")
plt.axis("off")

plt.show()
```

## Output

<img width="942" height="565" alt="image" src="https://github.com/user-attachments/assets/24be1e29-ce91-42fd-946a-789318e9cbe6" />


## Result

Thus, Canny Edge Detection using OpenCV and Matplotlib was implemented successfully.
