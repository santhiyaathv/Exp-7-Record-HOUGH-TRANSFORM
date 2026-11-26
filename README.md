# Exp-7-Record-HOUGH-TRANSFORM
## NAME: SANTHIYA B
## REG NO:212224230247


##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

## Learning Objective

* Understand each stage of image processing
* Learn how to build a complete computer vision pipeline
* Practice writing code in guided sections

**Important Instruction:**
👉 Write code **ONLY in places marked as `# Your Code Here`**
👉 Do NOT modify any other part of the code

---

##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Developed By

* **Name:** Abinaya A
* **Register No:** 212224230004

##  Algorithm & Explanation

```python 

import cv2

import numpy as np

import matplotlib.pyplot as plt

image = cv2.imread('Qno.1.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))

plt.title("Input Image")

plt.axis('off')

plt.imshow(gray_image, cmap='gray')

plt.title("Grayscale Image")

plt.axis('off')

edges = cv2.Canny(gray_image, 50, 150)

plt.imshow(edges, cmap='gray')

plt.title("Canny Edge Detector")

plt.axis('off')

lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)

for line in lines:
    x1, y1, x2, y2 = line[0]  
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))

plt.title("Result of Hough Transform")

plt.axis('off')

```

##  Expected Output

* Original image

<img width="355" height="507" alt="image" src="https://github.com/user-attachments/assets/818f0fca-3750-4904-8e3e-981057b11c75" />



* Grayscale image

<img width="362" height="507" alt="image" src="https://github.com/user-attachments/assets/f83adba3-dbb2-4697-a43a-b917dae4e6f7" />



* Canny Edge Detector

<img width="360" height="502" alt="image" src="https://github.com/user-attachments/assets/89460a2d-f9d9-43e7-ba81-234ab86dba35" />




* Final Hough Transform

<img width="367" height="503" alt="image" src="https://github.com/user-attachments/assets/5a44ed3d-b668-4130-88df-18913a75aabb" />




---


## Result

Thus, the Hough Transform  is successfully implemented by completing the missing code sections. The system detects and highlights hough transform effectively.

---
